## 🧠 TARJETA DE ESTUDIO – ARRAYS vs `ArrayList` (JAVA) (A6)

### ¿Qué es un array?

Un array es una **estructura de datos de tamaño fijo** que almacena elementos **del mismo tipo**.

Características clave:

* Tamaño definido al crearse
* Acceso por índice
* Más simple y más eficiente en memoria

👉 Una vez creado, **no puede crecer ni reducirse**.

---

### ¿Qué es un `ArrayList`?

`ArrayList` es una **lista dinámica** que puede **crecer o reducirse** automáticamente.

Características clave:

* Tamaño dinámico
* Permite agregar y eliminar elementos
* Forma parte de las **colecciones de Java**

Internamente:
👉 usa un array, pero gestiona el tamaño por ti.

---

### Diferencia clave (entrevista)

* **Array:** tamaño fijo, más básico
* **ArrayList:** tamaño dinámico, más flexible

Regla práctica:

> “Si el tamaño cambia, uso `ArrayList`. Si es fijo, array.”

---

### Acceso a elementos

Ambos permiten:

* Acceso rápido por índice (`posición`)

Pero:

* `ArrayList` tiene métodos útiles (`add`, `remove`, `contains`)
* El array no tiene lógica asociada

---

### Cuándo usar cada uno

**Usar array cuando:**

* El tamaño es conocido y fijo
* Necesitas simplicidad
* Buscas eficiencia básica

**Usar `ArrayList` cuando:**

* El tamaño puede cambiar
* Necesitas agregar o quitar elementos
* Trabajas con colecciones dinámicas

---

### Error común de junior

Usar arrays para:

* Listas que crecen
* Datos que se modifican mucho

Eso genera código complejo e innecesario.

---

### Buena práctica

* Preferir `ArrayList` en lógica de negocio
* Usar arrays solo cuando el tamaño es realmente fijo

---

### Frase que suma puntos

> “`ArrayList` me da flexibilidad; el array me da simplicidad.”

---
