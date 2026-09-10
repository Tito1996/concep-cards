## 🧠 TARJETA DE ESTUDIO – RESPONSES HTTP (SPRING BOOT) (A6)

### ¿Qué es una response?
Una response HTTP es la **salida de datos** de una API.  
Representa **la respuesta del servidor al cliente** después de procesar una request.

En simple:
👉 *la response dice qué pasó y devuelve el resultado.*

---

### Partes clave de una response

#### 1️⃣ Código de estado HTTP
Indica **el resultado de la operación**, incluso antes de leer el body.

Códigos más comunes (entrevista 🚨):
- `200 OK` → operación exitosa
- `201 Created` → recurso creado
- `400 Bad Request` → datos inválidos
- `404 Not Found` → recurso inexistente
- `409 Conflict` → conflicto de estado
- `500 Internal Server Error` → error del servidor

Idea clave:
> El código HTTP **comunica el resultado**, no solo el body.

---

#### 2️⃣ Body (cuerpo de la response)
Contiene los **datos devueltos** por la API, normalmente en **JSON**.

Buenas prácticas:
- Devolver DTOs
- Estructura clara y consistente
- No exponer entidades JPA

Ejemplo conceptual:
👉 datos, mensajes o errores bien definidos.

---

#### 3️⃣ Headers
Aportan **información adicional**:
- Tipo de contenido (`Content-Type`)
- Metadatos de la respuesta
- Control de caché, etc.

No suelen ser el foco, pero existen.

---

### `ResponseEntity`
`ResponseEntity` permite:
- Definir el **código HTTP**
- Controlar el **body**
- Configurar **headers**

Idea clave:
👉 da control total sobre la response.

---

### Regla de oro (entrevista 🚨)
> **La response debe ser clara, predecible y coherente.**

El cliente debe poder entender:
- si fue exitoso
- qué salió mal
- qué datos se devuelven

---

### Manejo de errores en responses
Buenas prácticas:
- Usar códigos HTTP correctos
- Devolver mensajes claros
- Mantener formato consistente

Ejemplo mental:
👉 errores también son responses válidas.

---

### Errores comunes en entrevistas
- Devolver siempre `200`
- Usar códigos incorrectos
- Exponer entidades JPA
- Responses inconsistentes entre endpoints

---

### Frase que suma puntos
> “Una buena response comunica claramente el resultado de la operación.”

---
