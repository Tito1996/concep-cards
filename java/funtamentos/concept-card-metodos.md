## 🧠 TARJETA DE ESTUDIO – MÉTODOS (JAVA) (A6)

### ¿Qué es un método?

Un método es un **bloque de código con nombre** que:

* recibe datos (parámetros),
* realiza una tarea concreta,
* y puede devolver un resultado.

En simple:
👉 *un método es una acción con responsabilidad clara.*

---

### Parámetros

Son los **datos de entrada** del método.

Buenas prácticas:

* Usar solo los **necesarios**
* Tipos claros
* Evitar demasiados parámetros

Regla práctica:
👉 más de 3–4 parámetros suele indicar mal diseño.

---

### Valor de retorno

Es el **resultado** que devuelve el método.

* Puede devolver un valor (`int`, `String`, objeto, etc.)
* O no devolver nada (`void`)

Idea clave:
👉 el retorno debe ser **claro y predecible**.

---

### Métodos `void`

Un método `void`:

* **no devuelve valor**
* suele ejecutar una acción (guardar, imprimir, modificar estado)

Buena práctica:
👉 si no devuelve nada, que el nombre lo deje claro (`guardarPedido`, `enviarEmail`).

---

### Regla de oro (entrevista)

> **Un método debe hacer una sola cosa y hacerla bien.**

Si hace:

* validar
* calcular
* guardar
* formatear

todo junto 👉 🚨 mala señal.

---

### Señales de mal método

* Muy largo
* Nombre genérico (`process`, `handle`)
* Muchos `if`
* Mezcla lógica distinta
* Difícil de testear

---

### Buena práctica

* Nombres descriptivos
* Métodos cortos
* Responsabilidad única
* Retornos claros
* Fácil de explicar en una frase

---

### Frase que suma puntos

> “Si no puedo explicar qué hace un método en una frase, está mal diseñado.”

---
