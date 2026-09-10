# 📘 TypeScript — Intersection types (A5)

Los **intersection types** combinan **varios tipos en uno solo**.
Un valor debe cumplir **todos** los tipos involucrados.

---

### Sintaxis
Se utiliza el operador `&` (AND).

```ts
type Persona = {
  nombre: string;
};

type Empleado = {
  id: number;
};

type EmpleadoPersona = Persona & Empleado;
````

---

### Uso

```ts
const empleado: EmpleadoPersona = {
  nombre: "Ana",
  id: 1
};
```

---

### Diferencia con Union

* `A | B` → uno u otro
* `A & B` → ambos

---

### Uso común

* Composición de modelos
* Extender tipos existentes
* Mezclar responsabilidades claras

---

### Con interfaces

```ts
type Admin = Usuario & {
  permisos: string[];
};
```

---

### Precaución

❌ Tipos muy grandes y difíciles de leer
✅ Composición clara y simple
