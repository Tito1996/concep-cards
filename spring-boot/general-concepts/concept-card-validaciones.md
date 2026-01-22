## 🧠 TARJETA DE ESTUDIO – VALIDACIONES (SPRING BOOT) (A6)

### ¿Qué son las validaciones?
Las validaciones aseguran que **los datos de entrada sean correctos** antes de ejecutar la lógica del sistema.

En simple:
👉 *no confiar en lo que llega desde afuera.*

Esto demuestra **pensamiento defensivo**, muy valorado en entrevistas.

---

### `@Valid`
`@Valid` le indica a Spring que:
- valide automáticamente el objeto recibido
- antes de que llegue al método del controller

Uso típico:
👉 en parámetros anotados con `@RequestBody`.

Idea clave:
> Si la validación falla, **el método no se ejecuta**.

---

### Anotaciones más comunes (MUY preguntadas)

#### `@NotNull`
- El valor **no puede ser null**
- Se usa para campos obligatorios

---

#### `@NotEmpty` / `@NotBlank`
- Evitan valores vacíos
- Muy usadas en strings y colecciones

---

#### `@Size`
- Define tamaño mínimo y/o máximo
- Se usa en strings, listas, arrays

Ejemplo mental:
👉 nombre con mínimo 3 caracteres.

---

### ¿Dónde se aplican?
Normalmente en:
- DTOs de request
- Objetos de entrada

👉 **No en entidades JPA** para reglas de API.

---

### Regla de oro (entrevista 🚨)
> **Validar siempre antes de procesar.**

Nunca:
- asumir que los datos son correctos
- validar después de ejecutar lógica

---

### ¿Qué pasa si la validación falla?
Spring:
- lanza una excepción
- devuelve `400 Bad Request`
- evita ejecutar la lógica de negocio

Esto protege al sistema automáticamente.

---

### Errores comunes en entrevistas
- No usar `@Valid`
- Validar “a mano” todo
- Mezclar validaciones con lógica de negocio
- Confiar en la entrada del cliente

---

### Buena práctica
- Validar en el controller (entrada)
- Aplicar reglas de negocio en el service
- Usar mensajes claros de error

---

### Frase que suma muchos puntos
> “Valido los datos apenas entran para proteger la lógica del sistema.”

---
