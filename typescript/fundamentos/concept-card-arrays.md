# 📘 TypeScript — Arrays tipados

En TypeScript, los arrays pueden declararse indicando **qué tipo de elementos**
pueden contener, evitando mezclas incorrectas.

---

### Sintaxis básica
```ts
let numeros: number[] = [1, 2, 3];
let nombres: string[] = ["Ana", "Luis"];
````

### Sintaxis alternativa (genérica)

```ts
let valores: Array<number> = [10, 20, 30];
```

---

---

### Inferencia en arrays

```ts
const edades = [18, 25, 40]; // number[]
```

---

### Arrays con múltiples tipos

```ts
let datos: (string | number)[] = ["ID", 123];
```

---

### Operaciones seguras

```ts
numeros.push(4);      // válido
numeros.push("cinco"); // error
```

---

### Beneficios

* Evita errores de tipo en runtime
* Autocompletado confiable
* Código más predecible

### Error común

❌ Usar `any[]`
✅ Usar union types si es necesario
