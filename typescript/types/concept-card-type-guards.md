# 📘 TypeScript — Type guards

Los **type guards** son funciones o expresiones que permiten
**determinar explícitamente el tipo** de una variable en tiempo de ejecución,
ayudando a TypeScript a hacer narrowing.

---

### `typeof`
```ts
function procesar(valor: string | number) {
  if (typeof valor === "string") {
    valor.toUpperCase();
  }
}
````

### `instanceof`

```ts
class ErrorPersonalizado {}

function manejar(error: Error | ErrorPersonalizado) {
  if (error instanceof ErrorPersonalizado) {
    // error específico
  }
}
```

---

### Type guard personalizado

```ts
interface Usuario {
  nombre: string;
}

function esUsuario(obj: any): obj is Usuario {
  return obj && typeof obj.nombre === "string";
}
```

---

### Uso

```ts
if (esUsuario(valor)) {
  valor.nombre; // Usuario
}
```

---

### Beneficios

* Lógica clara
* Tipado seguro
* Ideal para datos externos (APIs)

### Regla práctica

> Usa type guards cuando `typeof` no sea suficiente
