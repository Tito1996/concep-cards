# 📘 TypeScript — Literal types

Los **literal types** permiten restringir un valor
a **valores exactos**, no solo al tipo general.

---

### Ejemplo básico
```ts
let estado: "activo" | "inactivo";
estado = "activo";   // válido
estado = "pendiente"; // error
````

---

### Uso con funciones

```ts
function setModo(modo: "light" | "dark") {}
```

### Uso con números

```ts
type Dado = 1 | 2 | 3 | 4 | 5 | 6;
```

---

### Combinación con interfaces

```ts
interface Respuesta {
  status: "ok" | "error";
  mensaje: string;
}
```

---

### Beneficios

* Mayor seguridad
* Modela reglas del dominio
* Reduce estados inválidos

---

### Uso común

✅ Estados
✅ Flags
✅ Configuraciones limitadas

### Error común

❌ Usar `string` cuando los valores son finitos
