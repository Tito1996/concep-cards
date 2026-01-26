# 📘 TypeScript — Manejo de errores con tipos

TypeScript permite **modelar errores explícitamente** usando tipos,
en lugar de depender solo de excepciones en runtime.

---

### Problema común
```ts
function obtenerUsuario(): Usuario {
  // puede fallar
}
````

No es evidente cuándo falla.

### Solución con union types

```ts
type Resultado =
  | { ok: true; data: Usuario }
  | { ok: false; error: string };
```

---

### Uso

```ts
function obtenerUsuario(): Resultado {
  if (error) {
    return { ok: false, error: "No encontrado" };
  }
  return { ok: true, data: usuario };
}
```

---

### Consumo seguro

```ts
const resultado = obtenerUsuario();

if (resultado.ok) {
  resultado.data.nombre;
} else {
  console.error(resultado.error);
}
```

---

### Beneficios

* Errores visibles en el tipo
* Flujos controlados
* Menos excepciones inesperadas

### Regla práctica

> Si puede fallar, refléjalo en el tipo
