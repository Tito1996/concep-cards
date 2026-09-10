# 📘 TypeScript — Modo strict (A5)

El **modo `strict`** activa el conjunto más completo de reglas
de verificación de tipos en TypeScript.

### Activación
```json
{
  "compilerOptions": {
    "strict": true
  }
}
````

---

### Qué incluye

* `noImplicitAny`
* `strictNullChecks`
* `strictFunctionTypes`
* `strictPropertyInitialization`
* `noImplicitThis`

### Ejemplo

```ts
function saludar(nombre) {
  // error: parámetro implícitamente any
}
```

---

### Con `strictNullChecks`

```ts
let nombre: string;
// nombre.toUpperCase(); // error
```

---

### Beneficios

* Detecta errores reales
* Código más robusto
* Menos bugs en producción

### Mito común

❌ “strict es muy molesto”

✅ Es molesto solo al principio

### Regla práctica

> `strict` no es opcional en proyectos profesionales
Confírmame y comenzamos con **🅰️ Angular — Nivel Junior: Qué es Angular**.
```
