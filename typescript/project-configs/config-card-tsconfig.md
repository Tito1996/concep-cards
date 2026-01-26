# 📘 TypeScript — tsconfig (A5)

El archivo **`tsconfig.json`** define **cómo se compila el proyecto TypeScript**.
Es el núcleo de la configuración del compilador.

---

### Qué controla
- Nivel de tipado
- Salida de compilación
- Compatibilidad con JavaScript
- Reglas de verificación

### Ejemplo básico
```json
{
  "compilerOptions": {
    "target": "ES2020",
    "module": "ESNext",
    "outDir": "dist",
    "strict": true
  }
}
````

---

### Opciones comunes

* `target` → versión de JS
* `module` → sistema de módulos
* `outDir` → carpeta de salida
* `rootDir` → carpeta fuente

---

### Archivos incluidos

```json
"include": ["src"]
```

---

### Beneficios

* Consistencia del proyecto
* Control del nivel de seguridad
* Evita configuraciones implícitas

### Regla práctica

> Un buen `tsconfig` es parte del diseño
