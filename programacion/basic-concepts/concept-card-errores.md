## 🧠 TARJETA DE ESTUDIO – MANEJO BÁSICO DE ERRORES

### ¿Qué es manejar errores?

Es **anticipar, detectar y responder** a situaciones donde algo puede salir mal, sin que el sistema falle de forma descontrolada.

En simple:
👉 *el sistema no asume que todo va a salir bien.*

---

### Tipos de errores comunes

* Datos de entrada inválidos
* Recursos inexistentes (no encontrado)
* Estados inesperados
* Errores de sistema (DB, red, servicios externos)

No todos los errores son bugs:
👉 muchos son **escenarios normales**.

---

### Objetivo del manejo de errores

* Evitar caídas del sistema
* Mantener consistencia de datos
* Dar respuestas claras
* Facilitar el debug

---

### Manejo básico (conceptual)

* **Detectar el error** lo antes posible
* **Interrumpir el flujo** si no se puede continuar
* **Comunicar el error** de forma clara

Ejemplo mental:

> “Si no puedo continuar de forma segura, corto y aviso.”

---

### Errores vs Excepciones

* **Error:** el problema en sí
* **Excepción:** el mecanismo para manejarlo

No todas las excepciones deben atraparse:
👉 algunas deben propagarse.

---

### Errores comunes en entrevistas

* Ignorar errores
* Capturar todo “por las dudas”
* Ocultar errores reales
* Devolver siempre éxito aunque falle algo

---

### Buena práctica clave

Manejar el error **donde tenga sentido**, no donde aparezca.

Ejemplo:
👉 validar entrada antes de procesar
👉 manejar reglas de negocio en la lógica
👉 dejar errores técnicos al framework

---

### Frase que suma puntos

> “Un error bien manejado es parte del flujo normal del sistema.”

---
