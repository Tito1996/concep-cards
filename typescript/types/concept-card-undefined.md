# 📘 TypeScript — Manejo de undefined (A5)

`undefined` representa la **ausencia de valor**.
En TypeScript debe manejarse explícitamente para evitar errores en runtime.

### Ejemplo común
```ts
let nombre: string | undefined;
````

---

### Error típico

```ts
nombre.toUpperCase(); // error
```

### Validación explícita

```ts
if (nombre !== undefined) {
  nombre.toUpperCase();
}
```

---

### Operador de coalescencia nula

```ts
const valor = nombre ?? "por defecto";
```

### Optional chaining

```ts
usuario.direccion?.ciudad;
```

---

### Buenas prácticas

✅ Usar `undefined` de forma explícita

✅ Validar antes de acceder

❌ Ignorar advertencias del compilador

### Regla práctica

> Si TypeScript avisa, probablemente tenga razón
