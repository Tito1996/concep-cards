# 📘 TypeScript — Tipado de funciones

En TypeScript se pueden tipar **parámetros** y **valores de retorno**
para garantizar el uso correcto de las funciones.

--- 

### Sintaxis básica
```ts
function sumar(a: number, b: number): number {
  return a + b;
}
````

### Funciones sin retorno

```ts
function logMensaje(msg: string): void {
  console.log(msg);
}
```

### Funciones flecha

```ts
const multiplicar = (a: number, b: number): number => a * b;
```

---

### Parámetros opcionales

```ts
function saludar(nombre?: string): string {
  return nombre ? `Hola ${nombre}` : "Hola";
}
```

---

### Beneficios

* Evita llamadas incorrectas
* Documentación implícita
* Mejora la refactorización

---

### Error común

❌ No tipar el retorno

✅ Dejar que TypeScript valide lo que se devuelve
