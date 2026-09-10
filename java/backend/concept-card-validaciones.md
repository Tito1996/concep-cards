# TARJETA DE ESTUDIO – Validaciones en Backend Java


## 📌 ¿Qué son las Validaciones?

Las **validaciones en backend Java** garantizan que los **datos recibidos cumplen reglas de negocio y consistencia** antes de ser procesados o persistidos.

✔ Protegen la aplicación
✔ Evitan datos inválidos
✔ Refuerzan la seguridad

---

## 🧱 ¿Dónde se Validan los Datos?

* **Entrada de la API** (requests)
* **DTOs**
* **Servicios (reglas de negocio)**
* **Persistencia (última línea de defensa)**

📍 El backend **siempre valida**, aunque el frontend también lo haga

---

## 🛠️ Bean Validation (Jakarta Validation)

Estándar de Java para validaciones declarativas.

### Anotaciones Comunes

* `@NotNull`
* `@NotBlank`
* `@Size`
* `@Min` / `@Max`
* `@Email`
* `@Pattern`

✔ Claras
✔ Reutilizables
✔ Declarativas

---

## 🧩 Validación en APIs REST (Spring)

* Uso de `@Valid` o `@Validated`
* Se aplica automáticamente al recibir `@RequestBody`

📍 Si falla → `400 Bad Request`

---

## 🧠 Validaciones de Negocio

No todo se valida con anotaciones.

Ejemplos:

* Usuario ya existe
* Stock disponible
* Estado permitido para una operación

📍 Se implementan en la **capa de servicio**

---

## ⚠️ Errores Comunes

* Confiar solo en validaciones frontend
* No validar DTOs
* Mezclar validación técnica con lógica de negocio
* Mensajes de error poco claros
* No manejar excepciones de validación

---

## 🎯 Buenas Prácticas

* Validar **entrada**, no entidades directamente
* Usar DTOs específicos por caso
* Separar validación técnica y de negocio
* Centralizar manejo de errores
* Devolver mensajes claros al cliente

---

## 📝 Nota para Full Stack

* Backend Java es la autoridad final de los datos
* Angular valida UX, Java valida integridad
* Validaciones bien hechas reducen bugs y soporte

---

**Tip:**
Si un dato inválido llega a la base de datos, el fallo no fue del usuario: fue una **validación mal diseñada en el backend**.
