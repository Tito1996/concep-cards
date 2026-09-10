# 📘 TypeScript — Union types

Los **union types** permiten que una variable, parámetro o retorno
pueda tener **más de un tipo posible**.

---

### Sintaxis
Se utiliza el operador `|` (OR).

```ts
let id: number | string;
````

### Ejemplo práctico

```ts
function imprimirId(id: number | string) {
  console.log(id);
}
```

---

### Uso con lógica de control

```ts
function procesar(valor: number | string) {
  if (typeof valor === "string") {
    return valor.toUpperCase();
  }
  return valor * 2;
}
```

---

### Union en arrays

```ts
let datos: (string | number)[] = [1, "dos", 3];
```

---

### Beneficios

* Modela escenarios reales
* Evita `any`
* Hace el código más expresivo

### Error común

❌ Asumir un tipo sin validarlo

✅ Usar checks (`typeof`, `instanceof`)
Confírmame y continuamos con **📘 TypeScript — Nivel Mid: Diferencias entre `type` e `interface`**.
