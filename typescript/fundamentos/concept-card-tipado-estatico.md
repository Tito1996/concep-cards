**TARJETA DE ESTUDIO – TypeScript: Tipado Estático**

---

## 📌 ¿Qué es el Tipado Estático?

El **tipado estático** permite definir el **tipo de las variables, parámetros y retornos** en tiempo de desarrollo.

TypeScript detecta errores **antes de ejecutar** la aplicación.

---

## 🧱 Tipos Básicos

* `string`
* `number`
* `boolean`
* `any` (evitarlo)
* `void`
* `null` / `undefined`

**Ejemplo:**

```ts
let nombre: string;
let edad: number;
```

---

## 🧩 Tipado en Funciones

* Tipos en parámetros
* Tipo de retorno explícito

```ts
function sumar(a: number, b: number): number {
  return a + b;
}
```

✔ Código más claro
✔ Menos errores

---

## 🧠 Inferencia de Tipos

TypeScript puede **inferir el tipo automáticamente**:

```ts
let activo = true; // boolean
```

✔ Menos código
✔ Tipado seguro

---

## 🧰 Tipos Avanzados (Clave)

* `interface`
* `type`
* `enum`
* `union types`
* `optional properties ( ? )`

📍 Muy usados en modelos y DTOs

---

## 🎯 Beneficios del Tipado Estático

* Detección temprana de errores
* Autocompletado y refactorización
* Código más legible y mantenible
* Mejor trabajo en equipo

---

## ⚠️ Buenas Prácticas

* Evitar `any`
* Tipar siempre APIs y modelos
* Usar interfaces para contratos de datos
* Ser explícito en lógica crítica

---

## 📝 Nota para Full Stack

* Angular depende fuertemente de TypeScript
* Facilita integración con APIs Java
* Reduce errores entre frontend y backend

---

**Tip:** Si TypeScript se queja, normalmente tiene razón.
