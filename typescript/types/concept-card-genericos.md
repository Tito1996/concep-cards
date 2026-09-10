# 📘 TypeScript — Generics básicos (A5)

Los **generics** permiten crear código **reutilizable**
sin perder información de tipo.

---

### Problema sin generics
```ts
function envolver(valor: any): any {
  return valor;
}
````

### Solución con generics

```ts
function envolver<T>(valor: T): T {
  return valor;
}
```

---

### Uso

```ts
envolver<string>("hola");
envolver<number>(10);
```

### Inferencia automática

```ts
const resultado = envolver("texto"); // T = string
```

---

### Generics con interfaces

```ts
interface Respuesta<T> {
  data: T;
  error?: string;
}
```

---

### Beneficios

* Evita `any`
* Tipado preciso
* Código flexible y seguro

### Regla práctica

> Usa generics cuando el tipo depende del uso
