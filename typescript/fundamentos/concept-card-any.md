# 📘 TypeScript — any

### `any`

El tipo **`any`** desactiva el sistema de tipos de TypeScript para una variable.
Es equivalente a decir: “confía en mí”.

### Ejemplo
```ts
let valor: any = 10;
valor = "texto";
valor.metodoInexistente(); // No error en compilación
````

---

### Por qué existe

* Migraciones desde JavaScript
* Casos muy dinámicos o desconocidos

---

### Problemas de `any`

❌ No hay verificación de tipos
❌ Se pierden autocompletado y refactors
❌ Errores aparecen recién en runtime
❌ Oculta bugs

---

### Alternativas recomendadas

* `unknown`
* Tipos específicos
* Union types
* Generics

```ts
let valor: unknown;

if (typeof valor === "string") {
  valor.toUpperCase();
}
```

---

### Regla práctica

> Si usas `any`, TypeScript deja de ayudarte

### Buenas prácticas

✅ Usar `any` solo como último recurso
✅ Documentar su uso cuando sea inevitable
