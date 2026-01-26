# 📘 TypeScript — Inmutabilidad (A5)

La **inmutabilidad** implica que un valor **no se modifica después de ser creado**.
En lugar de cambiarlo, se crea una **nueva versión**.

---

### Ejemplo mutable (evitar)
```ts
usuario.nombre = "Luis";
````

### Ejemplo inmutable

```ts
const usuarioActualizado = {
  ...usuario,
  nombre: "Luis"
};
```

### En arrays

```ts
const numeros = [1, 2, 3];

const nuevosNumeros = [...numeros, 4];
```

---

### Beneficios

* Menos efectos colaterales
* Código más predecible
* Facilita testing y debugging
* Base para programación reactiva (Angular, RxJS)

---

### Uso común

* Estado de aplicaciones
* Reducers
* Flujos reactivos

### Regla práctica

> Si un dato cambia, crea uno nuevo
