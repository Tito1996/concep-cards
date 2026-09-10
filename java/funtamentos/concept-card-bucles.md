## 🧠 TARJETA DE ESTUDIO – BUCLES EN JAVA (`for`, `while`, `do-while`) (A6)

### ¿Qué es un bucle?

Un bucle permite **ejecutar un bloque de código repetidamente** mientras se cumpla una condición o para recorrer una colección.

En simple:
👉 *repetir sin copiar código.*

---

### `for`

Se usa cuando:

* **Sabes cuántas veces** vas a iterar
* Recorres arrays o listas
* Hay un inicio, una condición y un avance claros

Idea clave:
👉 el `for` es el bucle más común para recorrer colecciones.

---

### `while`

Se usa cuando:

* **No sabes cuántas veces** se va a ejecutar
* La repetición depende de una condición dinámica

Riesgo:
🚨 bucle infinito si la condición nunca cambia.

---

### `do-while`

Se usa cuando:

* Necesitas que el bloque se ejecute **al menos una vez**
* La condición se evalúa **al final**

Diferencia clave:
👉 el `do-while` siempre se ejecuta una vez.

---

### Recorrer arrays o listas (entrevista)

Un junior debe saber:

* Acceder a cada elemento
* No salirse de los límites
* Entender cuántas veces se ejecuta el bucle

Error típico:
👉 índices mal calculados.

---

### Evitar bucles infinitos

Un bucle infinito ocurre cuando:

* La condición nunca se vuelve falsa
* El contador no cambia

Buena práctica:

> Preguntarse siempre: **¿cuándo termina este bucle?**

---

### Errores comunes en entrevistas

* No saber cuántas veces itera el bucle
* Usar `while` cuando un `for` es más claro
* Olvidar actualizar el contador
* Bucles difíciles de entender

---

### Buena práctica

* Elegir el bucle según el problema
* Mantener condiciones claras
* Priorizar legibilidad sobre “trucos”

---

### Frase que suma puntos

> “Uso `for` cuando conozco la iteración y `while` cuando depende de una condición.”

---
