## 🧠 TARJETA DE ESTUDIO – OPERADORES Y EXPRESIONES (JAVA) (A6)

### ¿Qué es un operador?

Un operador es un **símbolo que permite realizar una operación** sobre uno o más valores.

En Java, los operadores se combinan para formar **expresiones**.

---

### ¿Qué es una expresión?

Una expresión es cualquier combinación de:

* valores
* variables
* operadores

que **produce un resultado**.

Idea clave:
👉 *toda expresión en Java devuelve un valor.*

---

### 1️⃣ Operadores aritméticos

Se usan para cálculos numéricos:

* `+` suma
* `-` resta
* `*` multiplicación
* `/` división
* `%` resto

Resultado:
👉 normalmente un número.

---

### 2️⃣ Operadores relacionales

Comparan valores.

* `==` igual
* `!=` distinto
* `<`, `>`, `<=`, `>=`

Resultado:
👉 **siempre devuelven `boolean`**.

Muy usados en:

* `if`
* `while`
* `for`

---

### 3️⃣ Operadores lógicos

Trabajan con valores booleanos:

* `&&` AND
* `||` OR
* `!` NOT

Permiten **combinar condiciones**.

Ejemplo conceptual:
👉 validar permisos, estados, reglas de negocio.

---

### Clave en Java (MUY IMPORTANTE)

> Muchas expresiones terminan evaluando a `boolean`.

Eso significa que:

* Java no acepta números como condiciones
* La condición debe ser **explícitamente booleana**

Ejemplo mental:
👉 “esto tiene que ser verdadero o falso, nada más”.

---

### Precedencia (idea práctica)

Orden típico:

1. Aritméticos
2. Relacionales
3. Lógicos

Cuando hay duda:
👉 **usar paréntesis** para claridad.

---

### Errores comunes en entrevistas

* Confundir `=` con `==`
* Asumir que una expresión devuelve número cuando devuelve `boolean`
* Condiciones confusas sin paréntesis
* Comparar objetos incorrectamente

---

### Buena práctica

Priorizar **expresiones claras**, no “compactas”.

---

### Frase que suma puntos

> “En Java, las condiciones siempre son expresiones booleanas.”

---
