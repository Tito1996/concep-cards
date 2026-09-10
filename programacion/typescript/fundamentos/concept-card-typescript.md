# 📘 TypeScript — ¿Qué es y para qué sirve?

### ¿Qué es TypeScript?

**TypeScript** es un **superset de JavaScript** que añade **tipado estático**
y herramientas de desarrollo avanzadas, manteniendo compatibilidad total con JS.

> Todo código JavaScript válido es también TypeScript válido.

---

### ¿Para qué sirve?
- Detectar errores **en tiempo de compilación**
- Mejorar la **legibilidad** y **mantenibilidad**
- Facilitar el trabajo en **equipos grandes**
- Hacer el código más **predecible y seguro**

---

### Qué añade sobre JavaScript
- Tipos (`string`, `number`, `boolean`, etc.)
- Interfaces y tipos personalizados
- Autocompletado y refactorización confiable
- Mejor documentación implícita

---

### Ejemplo
```ts
function saludar(nombre: string): string {
  return `Hola ${nombre}`;
}
````

---

### Flujo de trabajo

TypeScript → **compila a JavaScript** → navegador / Node.js

### Cuándo usarlo

✅ Proyectos medianos o grandes
✅ Código mantenido en el tiempo
❌ Scripts pequeños y desechables
