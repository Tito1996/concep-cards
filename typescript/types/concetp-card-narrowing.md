# 📘 TypeScript — Narrowing (A5)

El **narrowing** es el proceso mediante el cual TypeScript
**reduce un tipo amplio** a uno más específico
según el flujo del programa.

---

### Ejemplo con union type
```ts
function procesar(valor: string | number) {
  if (typeof valor === "string") {
    valor.toUpperCase(); // string
  } else {
    valor.toFixed(2);    // number
  }
}
````

---

### Técnicas de narrowing

* `typeof`
* `instanceof`
* Comparaciones literales
* Chequeos de existencia

---

### Con valores literales

```ts
function manejarEstado(estado: "ok" | "error") {
  if (estado === "ok") {
    // estado es "ok"
  }
}
```

---

### Beneficios

* Acceso seguro a métodos
* Menos castings
* Código más expresivo

### Error común

❌ Asumir el tipo sin validarlo
✅ Dejar que el control de flujo haga el narrowing
