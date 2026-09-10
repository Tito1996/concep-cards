# 📘 TypeScript — Tipado de variables

## Tipado de variables

En TypeScript, las variables pueden declararse con un **tipo explícito**
para definir qué valores son válidos.

### Sintaxis básica
```ts
let edad: number = 30;
let nombre: string = "Ana";
let activo: boolean = true;
````

---

### Tipos primitivos comunes

* `string`
* `number`
* `boolean`
* `null`
* `undefined`

---

### Variables sin inicializar

```ts
let contador: number;
contador = 5;
```

---

### Tipado vs JavaScript

JavaScript permite:

```js
let valor = 10;
valor = "texto"; // permitido
```

TypeScript lo evita:

```ts
let valor: number = 10;
valor = "texto"; // error
```

---

### Beneficios

* Prevención temprana de errores
* Código más legible
* Mejor autocompletado

### Regla práctica

> Tipar variables que representan datos importantes del dominio
