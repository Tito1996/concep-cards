# 📘 TypeScript — type vs interface

Ambos se usan para **definir la forma de los datos**, pero tienen
diferencias conceptuales y prácticas importantes.

---

### `interface`
- Pensada para **objetos**
- Puede **extenderse**
- Puede **declararse varias veces** (declaration merging)

```ts
interface Usuario {
  id: number;
  nombre: string;
}

interface Usuario {
  activo: boolean;
}
````

### `type`

* Más **flexible**
* Soporta union, intersection y tipos primitivos
* No permite redeclaración

```ts
type ID = number | string;
```

---

### Extensión

```ts
interface Admin extends Usuario {
  rol: string;
}

type AdminType = Usuario & { rol: string };
```

---

### Cuándo usar cada uno

✅ `interface` → modelos de dominio, APIs, Angular
✅ `type` → unions, aliases, composiciones complejas

### Regla práctica

> Usa `interface` por defecto, `type` cuando lo necesites
