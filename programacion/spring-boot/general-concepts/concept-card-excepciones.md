## 🧠 TARJETA DE ESTUDIO – MANEJO DE EXCEPCIONES (SPRING BOOT) (A6)

### ¿Qué es el manejo de excepciones?
Es la forma de **capturar errores** y **responder correctamente** sin romper la aplicación ni exponer detalles internos.

En simple:
👉 *cuando algo falla, la API responde de forma controlada.*

---

### ¿Por qué es tan importante? (entrevista 🚨)
- Evita caídas del sistema
- Devuelve **códigos HTTP correctos**
- Centraliza la lógica de errores
- Mejora la experiencia del cliente

Un perfil mid **siempre** maneja excepciones.

---

### `@ExceptionHandler`
Permite manejar **una excepción concreta**.

Se usa para:
- Capturar una excepción específica
- Devolver una response personalizada

Idea clave:
👉 asocia **una excepción → una respuesta HTTP**.

---

### `@ControllerAdvice`
Permite manejar excepciones **de forma global**.

Ventajas:
- No repetir código en cada controller
- Centralizar errores
- Mantener controllers limpios

Regla práctica:
> Usar `@ControllerAdvice` para errores comunes del sistema.

---

### Errores HTTP correctos (MUY preguntado)

Códigos típicos:
- `400 Bad Request` → datos inválidos
- `404 Not Found` → recurso inexistente
- `409 Conflict` → conflicto de estado
- `500 Internal Server Error` → error inesperado

Idea clave:
👉 el **código HTTP comunica el resultado**, no solo el mensaje.

---

### Regla de oro (entrevista 🚨)
> **No devolver siempre `200 OK`.**

Un error debe reflejarse:
- en el código HTTP
- en el mensaje
- en el formato consistente

---

### Errores comunes en entrevistas
- Try/catch en todos lados
- Controllers llenos de manejo de errores
- Devolver siempre `200`
- Exponer mensajes técnicos o stacktrace

---

### Buena práctica
- Lanzar excepciones en el service
- Capturarlas en `@ControllerAdvice`
- Devolver respuestas claras y consistentes

---

### Frase que suma muchos puntos
> “Las excepciones no se esconden: se manejan y se comunican correctamente.”

---
