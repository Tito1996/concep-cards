# 📘 TypeScript — readonly

La palabra clave **`readonly`** impide que una propiedad
sea modificada después de su inicialización.

---

### Uso en interfaces
```ts
interface Usuario {
  readonly id: number;
  nombre: string;
}
````

```ts
usuario.id = 2; // error
usuario.nombre = "Luis"; // válido
```

### Uso en arrays

```ts
const numeros: ReadonlyArray<number> = [1, 2, 3];
numeros.push(4); // error
```

### Uso en clases

```ts
class Producto {
  constructor(
    public readonly codigo: string
  ) {}
}
```

---

### Beneficios

* Refuerza inmutabilidad
* Evita modificaciones accidentales
* Documenta intención

### Regla práctica

> Si no debe cambiar, márcalo como `readonly`
