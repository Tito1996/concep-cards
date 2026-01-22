## 🧠 TARJETA DE ESTUDIO – REQUESTS HTTP (SPRING BOOT)

### ¿Qué es una request?
Una request HTTP es la **entrada de datos** a una API.  
Representa **lo que el cliente le pide al servidor**.

En simple:
👉 *la request describe qué quiere el cliente y con qué datos.*

---

### Partes principales de una request

#### 1️⃣ Método HTTP
Indica la **intención** de la acción:
- `GET` → obtener datos
- `POST` → crear datos
- `PUT` / `PATCH` → modificar datos
- `DELETE` → eliminar datos

Clave de entrevista:
👉 el método comunica **qué tipo de operación** se quiere hacer.

---

#### 2️⃣ URL
Identifica el **recurso**.

Ejemplo mental:
- `/users` → colección
- `/users/10` → recurso específico

Idea REST:
👉 la URL representa **qué**, no **cómo**.

---

#### 3️⃣ Parámetros de la request

##### `@PathVariable`
- Viene en la URL
- Identifica un recurso concreto

Ejemplo:
👉 `/orders/25`

---

##### `@RequestParam`
- Viene como parámetro en la URL
- Se usa para filtros u opciones

Ejemplo:
👉 `/orders?status=PAID&page=1`

---

##### `@RequestBody`
- Viene en el cuerpo de la request
- Normalmente en **JSON**
- Se usa para enviar datos complejos

Ejemplo:
👉 crear o actualizar un recurso

---

### Mapeo a Java
Spring Boot:
- Convierte la request a un **objeto Java**
- Usa DTOs
- Aplica validaciones si se configuran

Idea clave:
> La request **no debe mapearse a entidades JPA**.

---

### Validación de requests (MUY importante)
Nunca confiar en los datos entrantes:
- Pueden ser inválidos
- Incompletos
- Maliciosos

Buena práctica:
👉 validar antes de procesar.

---

### Errores comunes en entrevistas
- No saber de dónde viene cada dato
- Usar `@RequestBody` para todo
- No diferenciar `PathVariable` y `RequestParam`
- Asumir que la request siempre es correcta

---

### Frase que suma puntos
> “La request define la intención del cliente; el backend valida y decide cómo responder.”

---
