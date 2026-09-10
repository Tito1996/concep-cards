## 🧠 TARJETA DE ESTUDIO – CONTROLADORES REST (SPRING BOOT)

### ¿Qué es un controlador REST?
Un controlador REST es la **capa de entrada** de una aplicación backend.  
Se encarga de **recibir peticiones HTTP** y **devolver respuestas HTTP**.

En simple:
👉 *conecta el mundo externo (HTTP) con la lógica interna.*

---

### `@RestController`
- Marca una clase como controlador REST
- Combina:
  - `@Controller`
  - `@ResponseBody`

Resultado:
👉 los métodos devuelven **datos (JSON)**, no vistas HTML.

---

### Mappings más comunes
Se usan para mapear **endpoints HTTP**:

- `@GetMapping` → obtener datos  
- `@PostMapping` → crear datos  
- `@PutMapping` → actualizar datos  
- `@DeleteMapping` → eliminar datos  

Idea clave:
👉 cada mapping representa una **acción REST**.

---

### Requests (entrada)
Un controller puede recibir datos desde:
- **Path** → `@PathVariable`
- **Query params** → `@RequestParam`
- **Body (JSON)** → `@RequestBody`

Buena práctica:
👉 validar la entrada antes de procesar.

---

### Responses (salida)
El controller:
- Devuelve datos (DTOs)
- Define códigos HTTP (`200`, `201`, `400`, `404`, etc.)

Idea clave:
👉 el código HTTP **comunica el resultado**, no solo el body.

---

### Regla de oro (entrevista 🚨)
> **El controller NO contiene lógica de negocio.**

Su responsabilidad es:
- recibir
- delegar al service
- responder

Nada más.

---

### Errores comunes en entrevistas
- Lógica de negocio en el controller
- Devolver entidades JPA directamente
- No manejar códigos HTTP correctos
- Controllers demasiado grandes

---

### Buena práctica
- Controllers finos
- Services con la lógica
- DTOs para requests y responses

---

### Frase que suma puntos
> “El controller orquesta la request; la lógica vive en el service.”

---
