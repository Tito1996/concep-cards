# 📘 TypeScript — Interfaces básicas

Una **interface** define la **estructura que debe cumplir un objeto**.
Se usa para describir contratos claros en el código.

---

### Definición de una interface
```ts
interface Usuario {
  id: number;
  nombre: string;
  activo: boolean;
}
````

### Uso

```ts
const usuario: Usuario = {
  id: 1,
  nombre: "Ana",
  activo: true
};
```

---

### Propiedades opcionales

```ts
interface Producto {
  nombre: string;
  precio?: number;
}
```

---

### Ventajas

* Reutilización de tipos
* Código más legible
* Contratos claros entre componentes
* Muy usadas en Angular y APIs

---

### Buenas prácticas

✅ Usar `interface` para objetos
✅ Nombrar con sustantivos
❌ Usar interfaces como diccionarios genéricos

### Diferencia clave

> Las interfaces describen **forma**, no implementación
