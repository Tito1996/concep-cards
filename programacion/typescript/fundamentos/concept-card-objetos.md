# 📘 TypeScript — Objetos tipados (A5)

TypeScript permite definir la **forma exacta** que debe tener un objeto,
especificando tipos para cada propiedad.

---

### Tipado inline
```ts
let usuario: {
  id: number;
  nombre: string;
  activo: boolean;
} = {
  id: 1,
  nombre: "Ana",
  activo: true
};
````

---

### Propiedades obligatorias

Todas las propiedades definidas deben existir y tener el tipo correcto.

```ts
usuario.activo = false; // válido
usuario.edad = 30;      // error
```

### Propiedades opcionales

```ts
let producto: {
  nombre: string;
  precio?: number;
};
```

---

### Ventajas

* Previene objetos incompletos o mal formados
* Documenta claramente el modelo de datos
* Mejora autocompletado y refactors

---

### Limitación

❌ Tipos inline grandes reducen legibilidad
✅ Usar interfaces o types para reutilizar
