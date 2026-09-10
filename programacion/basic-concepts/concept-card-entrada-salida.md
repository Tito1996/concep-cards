## 🧠 TARJETA DE ESTUDIO – ENTRADA Y SALIDA DE DATOS

### ¿Qué es la entrada y salida de datos?

Es la forma en que un programa **recibe información** del exterior y **devuelve resultados**.

En simple:
👉 *entrada = datos que llegan*
👉 *salida = datos que el programa produce*

---

### Ejemplos de **entrada**

* Datos del usuario (formularios, consola)
* Requests HTTP (JSON, parámetros)
* Archivos
* Base de datos
* APIs externas

---

### Ejemplos de **salida**

* Respuestas HTTP
* Mensajes por consola
* Archivos generados
* Datos guardados en una base de datos

---

### Idea clave para entrevistas

> La entrada y salida conectan la **lógica del sistema con el mundo real**.

La lógica sola no sirve si no:

* recibe datos correctamente
* devuelve resultados claros

---

### Validación de entrada (muy importante)

Nunca confiar en los datos que entran:

* Pueden ser inválidos
* Incompletos
* Maliciosos

Buena práctica:
👉 validar **antes** de procesar.

---

### Formato y consistencia de salida

La salida debe ser:

* Clara
* Predecible
* Bien estructurada

Ejemplo conceptual:

> “Si una API devuelve siempre el mismo formato, es más fácil de usar y mantener.”

---

### Errores comunes en entrevistas

* Asumir que la entrada siempre es correcta
* Mezclar lógica con entrada/salida
* Devolver datos inconsistentes
* No manejar errores de entrada

---

### Buena práctica clave

Separar:

* **Entrada / salida**
* **Lógica de negocio**

Esto mejora testeo y mantenimiento.

---

### Frase que suma puntos

> “La entrada se valida, la lógica procesa y la salida se controla.”

---
