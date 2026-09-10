# 📘 TypeScript — Propiedades opcionales (A5)

Las **propiedades opcionales** permiten que un objeto
**pueda o no incluir una propiedad** específica.

### Sintaxis
Se utiliza `?` después del nombre.

```ts
interface Usuario {
  nombre: string;
  edad?: number;
}
````

---

### Uso

```ts
const u1: Usuario = { nombre: "Ana" };
const u2: Usuario = { nombre: "Luis", edad: 30 };
```

---

### Acceso seguro

```ts
if (usuario.edad !== undefined) {
  console.log(usuario.edad);
}
```

---

### Con optional chaining

```ts
usuario.edad?.toFixed(0);
```

---

### Casos de uso

* Datos parciales
* Respuestas de API
* Formularios progresivos

### Error común

❌ Asumir que la propiedad siempre existe
✅ Validar antes de usar
