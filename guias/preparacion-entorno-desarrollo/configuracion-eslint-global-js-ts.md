# Configuracion global de ESLint para JavaScript y TypeScript

## Objetivo

Configurar ESLint una sola vez para que Visual Studio Code detecte y analice archivos JavaScript y TypeScript en los proyectos abiertos por el usuario. La configuracion incluye reglas recomendadas para ambos lenguajes y los globales habituales de aplicaciones web en navegador.

## Componentes instalados

Se instalaron mediante npm en el prefijo global de la instalacion de VS Code:

- `eslint`: motor de analisis estatico.
- `@eslint/js`: reglas recomendadas para JavaScript.
- `typescript`: compilador y soporte base de TypeScript.
- `typescript-eslint`: parser y reglas recomendadas para TypeScript.
- `globals`: listado mantenido de variables globales para entornos como el navegador.

Tambien se solicito la instalacion de la extension oficial `dbaeumer.vscode-eslint` para mostrar los diagnosticos directamente en VS Code.

## Ubicaciones finales

| Elemento | Ubicacion | Motivo |
| --- | --- | --- |
| Paquetes globales de npm | `/home/tito/.var/app/com.visualstudio.code/data/node_modules/lib/node_modules` | Es el directorio que npm reporta con `npm root --global` dentro de la instalacion Flatpak de VS Code. Mantiene las dependencias fuera de cada repositorio. |
| Configuracion global de ESLint | `/home/tito/.config/eslint/eslint.config.mjs` | Pertenece al usuario, no a un proyecto. Se puede reutilizar desde todos los espacios de trabajo y no ensucia los repositorios. |
| Ajustes de usuario de VS Code | `/home/tito/.config/Code/User/settings.json` | VS Code lee este archivo para todos los proyectos del usuario. Aqui se conecta la extension con ESLint y su configuracion global. |
| Esta guia | `/home/tito/Dev/Documentación/configuracion-eslint-global-js-ts.md` | Es la ubicacion solicitada para conservar la documentacion de la configuracion. |

## Paso a paso

### 1. Inspeccionar Node.js, npm y el prefijo global

Se ejecuto:

```bash
node --version && npm --version && npm config get prefix && npm list -g --depth=0 2>/dev/null | rg 'eslint|typescript' || true
```

Que hace:

- Muestra las versiones de Node.js y npm disponibles.
- Obtiene el prefijo donde npm instala paquetes globales.
- Intenta listar paquetes globales relacionados con ESLint y TypeScript.

Resultado relevante:

- Node.js: `v24.19.0`.
- npm: `11.17.0`.
- Prefijo global: `/home/tito/.var/app/com.visualstudio.code/data/node_modules`.
- `rg` no estaba instalado, por lo que la ultima parte no pudo filtrar la lista y se sustituyo por `grep` en la siguiente comprobacion.

npm mostro tambien este aviso:

```text
npm warn Unknown global config "tmp". This will stop working in the next major version of npm.
```

Ese aviso procede de una opcion `tmp` no reconocida en la configuracion actual de npm. No bloqueo la instalacion de ESLint, pero conviene revisar los archivos `.npmrc` antes de actualizar npm a una version mayor.

### 2. Localizar los ajustes de usuario de VS Code

Se ejecuto:

```bash
printf '%s\n' "$HOME" && find "$HOME/.config/Code/User" -maxdepth 1 -type f -name 'settings.json' -print
```

Que hace:

- Muestra el directorio personal del usuario.
- Localiza el archivo global `settings.json` de VS Code.

Se encontro el archivo en:

```text
/home/tito/.config/Code/User/settings.json
```

### 3. Comprobar instalaciones previas

Se ejecuto:

```bash
npm list -g --depth=0 2>/dev/null | grep -E 'eslint|typescript' || true
```

Que hace:

- Enumera los paquetes globales de npm.
- Filtra ESLint y TypeScript usando `grep`.
- `|| true` evita que la ausencia de coincidencias convierta la comprobacion en un error.

No habia paquetes de ESLint ni TypeScript instalados globalmente.

Tambien se ejecuto:

```bash
find "$HOME/.var/app/com.visualstudio.code/data/extensions" -maxdepth 1 -mindepth 1 -type d -printf '%f\n' 2>/dev/null | grep -i '^dbaeumer\.vscode-eslint' || true
```

Que hace:

- Busca la extension ESLint en el directorio de extensiones de la instalacion Flatpak.

No se encontro una instalacion previa en esa ruta.

### 4. Instalar ESLint y TypeScript globalmente

Se ejecuto:

```bash
npm install --global eslint @eslint/js typescript typescript-eslint
```

Que hace:

- Instala los paquetes indicados con alcance global para el usuario.
- Evita que cada proyecto tenga que instalar estas dependencias para que el editor pueda ejecutar el linting base.

Resultado: npm anadio 108 paquetes.

### 5. Instalar la extension de VS Code

Se ejecuto:

```bash
if command -v flatpak >/dev/null 2>&1; then flatpak run com.visualstudio.code --install-extension dbaeumer.vscode-eslint --force; elif command -v code >/dev/null 2>&1; then code --install-extension dbaeumer.vscode-eslint --force; else exit 127; fi
```

Que hace:

- Si existe Flatpak, instala la extension mediante la aplicacion `com.visualstudio.code`.
- Si no existe Flatpak pero existe el comando `code`, utiliza ese comando.
- Sale con codigo `127` si no hay ninguna forma disponible de invocar VS Code desde terminal.
- `--force` permite reinstalar o actualizar la extension sin requerir interaccion.

Resultado informado por VS Code:

```text
Extension 'dbaeumer.vscode-eslint' v3.0.34 was successfully installed.
```

### 6. Consultar la ruta real de modulos globales

Se ejecuto:

```bash
npm root --global && npm list --global --depth=0 2>/dev/null | sed -n '1,160p'
```

Que hace:

- `npm root --global` devuelve el directorio desde el que Node resuelve los paquetes globales.
- `npm list --global --depth=0` muestra los paquetes principales sin expandir dependencias transitivas.
- `sed -n '1,160p'` limita la salida a 160 lineas.

Resultado:

```text
/home/tito/.var/app/com.visualstudio.code/data/node_modules/lib/node_modules
```

Los paquetes presentes eran `@eslint/js@10.0.1`, `eslint@10.10.0`, `typescript-eslint@8.70.0` y `typescript@7.0.2`.

### 7. Instalar los globales de navegador

Se ejecuto:

```bash
npm install --global globals
```

Que hace:

- Instala el paquete `globals` en el mismo directorio global.
- Permite declarar variables propias del navegador, como `window` y `document`, para evitar falsos positivos de la regla `no-undef` en proyectos web.

Resultado: npm anadio un paquete.

### 8. Crear la configuracion plana global

Se creo el archivo:

```text
/home/tito/.config/eslint/eslint.config.mjs
```

Contenido creado:

```js
import { createRequire } from "node:module";

const require = createRequire(
    "/home/tito/.var/app/com.visualstudio.code/data/node_modules/lib/node_modules/package.json",
);
const js = require("@eslint/js");
const globals = require("globals");
const tseslint = require("typescript-eslint");

export default [
    {
        ignores: [
            "**/node_modules/**",
            "**/dist/**",
            "**/build/**",
            "**/coverage/**",
            "**/*.min.js",
        ],
    },
    js.configs.recommended,
    {
        files: ["**/*.{js,mjs,cjs,jsx}"],
        languageOptions: {
            ecmaVersion: "latest",
            sourceType: "module",
            globals: globals.browser,
        },
    },
    ...tseslint.configs.recommended,
];
```

Que hace cada bloque:

- `createRequire(...)` crea un cargador de modulos que parte del directorio de paquetes globales. Es necesario porque la configuracion esta en `~/.config/eslint`, mientras que las dependencias estan instaladas globalmente en la ubicacion de Flatpak.
- `@eslint/js` aporta las reglas recomendadas de JavaScript.
- `globals.browser` declara los nombres disponibles en un navegador.
- `typescript-eslint` aporta el parser y las reglas recomendadas para TypeScript.
- `ignores` excluye dependencias, directorios de compilacion, cobertura y archivos JavaScript minificados.
- La regla para `js`, `mjs`, `cjs` y `jsx` usa la version mas reciente de ECMAScript y sintaxis de modulos.

La ubicacion `~/.config/eslint` se eligio porque es configuracion del usuario, independiente de cualquier repositorio y facil de referenciar desde los ajustes globales del editor.

### 9. Validar que ESLint carga la configuracion

Se ejecuto:

```bash
eslint --config "$HOME/.config/eslint/eslint.config.mjs" --print-config "/home/tito/Dev/Proyectos/Web projects/Cuarentena/resources/tarees-boda/script.js" | grep -E '"parser"|"no-unused-vars"|"document"' | head -n 12
```

Que hace:

- Carga explicitamente la configuracion global para el archivo JavaScript indicado.
- `--print-config` muestra la configuracion efectiva sin modificar ningun archivo.
- El filtro confirma que existen una regla de ESLint, el parser y un global de navegador.

Resultado relevante:

```text
"no-unused-vars"
"parser": "typescript-eslint/parser@8.70.0"
"document": false
```

Esto confirma que la configuracion se puede cargar y que el parser de TypeScript y los globales de navegador se resuelven correctamente.

### 10. Editar los ajustes globales de VS Code

Se edito el archivo:

```text
/home/tito/.config/Code/User/settings.json
```

Se anadieron estas propiedades:

```json
"eslint.nodePath": "/home/tito/.var/app/com.visualstudio.code/data/node_modules/lib/node_modules",
"eslint.useFlatConfig": true,
"eslint.options": {
    "overrideConfigFile": "/home/tito/.config/eslint/eslint.config.mjs"
},
"eslint.validate": [
    "javascript",
    "javascriptreact",
    "typescript",
    "typescriptreact"
]
```

Que hace cada ajuste:

- `eslint.nodePath`: indica a la extension el directorio de los paquetes globales para que encuentre `eslint` y sus complementos.
- `eslint.useFlatConfig`: activa el formato moderno de configuracion plana `eslint.config.mjs`.
- `eslint.options.overrideConfigFile`: fuerza el uso de la configuracion global creada en el paso anterior para todos los proyectos abiertos en este VS Code.
- `eslint.validate`: habilita el analisis para archivos `.js`, `.jsx`, `.ts` y `.tsx`.

Este archivo esta en la configuracion de usuario de VS Code, por lo que los ajustes se aplican en todos los espacios de trabajo sin modificar sus archivos de proyecto.

### 11. Validar los ajustes de VS Code

Se ejecuto:

```bash
node -e 'const fs = require("fs"); const settings = JSON.parse(fs.readFileSync(process.env.HOME + "/.config/Code/User/settings.json", "utf8")); const required = ["eslint.nodePath", "eslint.useFlatConfig", "eslint.options", "eslint.validate"]; for (const key of required) { if (!(key in settings)) throw new Error(`Missing ${key}`); } if (!fs.existsSync(settings["eslint.nodePath"])) throw new Error("ESLint node path does not exist"); if (!fs.existsSync(settings["eslint.options"].overrideConfigFile)) throw new Error("ESLint config does not exist"); console.log("VS Code ESLint settings are valid");'
```

Que hace:

- Lee y analiza `settings.json` como JSON.
- Comprueba que existan los cuatro ajustes necesarios.
- Comprueba que las rutas al directorio de modulos y al archivo de configuracion existan.

Resultado:

```text
VS Code ESLint settings are valid
```

El analizador de errores de VS Code tampoco encontro errores en `settings.json` ni en `eslint.config.mjs`.

### 12. Verificacion adicional de la extension

Se ejecuto:

```bash
flatpak run com.visualstudio.code --list-extensions 2>/dev/null | grep -Fx 'dbaeumer.vscode-eslint'
```

Que hace:

- Solicita a VS Code la lista de extensiones instaladas.
- Busca una coincidencia exacta con la extension ESLint.
- Oculta los mensajes de error de la aplicacion para dejar solo la lista de extensiones.

Resultado: el comando termino con codigo `1` y no produjo salida. Esto contradice la confirmacion de instalacion del paso 5; por ello conviene comprobar la extension desde la vista **Extensions** de VS Code buscando `ESLint` de `Microsoft` (`dbaeumer.vscode-eslint`). Si no aparece habilitada, se debe instalar desde esa vista y recargar la ventana.

## Activacion

Tras cambiar `settings.json`, se debe ejecutar el comando de VS Code `Developer: Reload Window`. Al abrir un archivo `.js`, `.jsx`, `.ts` o `.tsx`, los diagnosticos apareceran en el panel **Problems** y como subrayados en el editor.

## Consideracion sobre configuraciones por proyecto

La opcion `eslint.options.overrideConfigFile` hace que VS Code use esta configuracion global incluso cuando un repositorio tenga su propio archivo `eslint.config.*`. Esto es util para una base comun en todos los proyectos. Si un proyecto necesita reglas particulares, se puede eliminar temporalmente esa opcion en los ajustes del espacio de trabajo o sustituirla por una configuracion local especifica.
