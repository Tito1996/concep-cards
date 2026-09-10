# TARJETA DE ESTUDIO – Manejo de Errores y Códigos HTTP en Backend Java


## 📌 ¿Por qué es importante el manejo de errores?

Un buen **manejo de errores** en backend Java:

* Comunica claramente qué salió mal
* Facilita el consumo de la API
* Mejora la seguridad y el debugging
* Define un **contrato claro** con el frontend

📍 Errores mal gestionados = APIs difíciles de usar

---

## 🧱 Principio Clave

👉 **La API debe fallar de forma controlada y predecible**

* Mensajes claros
* Códigos HTTP correctos
* Estructura de error consistente

---

## 🔁 Códigos HTTP más Usados

### ✅ Éxito

* `200 OK` → operación correcta
* `201 Created` → recurso creado
* `204 No Content` → éxito sin cuerpo

---

### ❌ Errores del Cliente (4xx)

* `400 Bad Request` → datos inválidos
* `401 Unauthorized` → no autenticado
* `403 Forbidden` → sin permisos
* `404 Not Found` → recurso inexistente
* `409 Conflict` → conflicto de estado

📍 El cliente envió algo incorrecto

---

### 🔥 Errores del Servidor (5xx)

* `500 Internal Server Error` → error no controlado
* `503 Service Unavailable` → servicio no disponible

📍 Responsabilidad del backend

---

## 🛠️ Manejo de Errores en Java (Spring)

* Uso de **excepciones**
* Centralización con `@ControllerAdvice`
* Mapeo excepción → código HTTP

✔ Código limpio
✔ Respuestas consistentes
✔ Fácil mantenimiento

---

## 🧩 Estructura de Respuesta de Error (Ejemplo)

```json
{
  "timestamp": "2026-01-22T10:30:00",
  "status": 400,
  "error": "Bad Request",
  "message": "El email es inválido",
  "path": "/api/usuarios"
}
```

📍 El frontend depende de esta estructura

---

## ⚠️ Errores Comunes

* Devolver siempre `200 OK`
* Exponer errores internos o stack traces
* Mensajes poco claros
* No diferenciar errores 4xx y 5xx
* Manejar errores en cada controlador

---

## 🎯 Buenas Prácticas

* Centralizar manejo de errores
* Usar códigos HTTP semánticos
* Mensajes claros y orientados al cliente
* No exponer detalles internos
* Documentar errores de la API

---

## 📝 Nota para Full Stack

* Angular reacciona según el código HTTP
* Un mal código rompe flujos de UI
* Backend Java define el comportamiento del cliente

---

**Tip:**
Si el frontend no sabe cómo reaccionar ante un error, el problema no es Angular: es un **mal manejo de errores en el backend**.
