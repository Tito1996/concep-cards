# 📘 TypeScript — Inferencia de tipos (A5)

La **inferencia de tipos** es la capacidad de TypeScript para
**deducir automáticamente el tipo** de una variable o expresión
sin que sea declarado explícitamente.

### Ejemplo básico
```ts
let edad = 30;        // number
let nombre = "Ana";  // string
````

---

TypeScript infiere el tipo según el valor inicial.

### En funciones

```ts
function sumar(a: number, b: number) {
  return a + b; // retorna number (inferido)
}
```

### En arrays

```ts
const numeros = [1, 2, 3]; // number[]
```

---

### Ventajas

* Menos código repetitivo
* Tipado fuerte sin sobreespecificar
* Código más limpio

---

### Cuándo confiar en la inferencia

✅ Valores simples y claros 

✅ Retornos evidentes

### Cuándo tipar explícitamente

❌ APIs públicas 

❌ Datos críticos del dominio 

❌ Inicializaciones ambiguas

---

### Regla práctica

> Usa inferencia por defecto, tipa cuando aporte claridad
