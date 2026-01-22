**TARJETA DE ESTUDIO – APIs REST**
**Formato:** A6

---

## 📌 ¿Qué es una API REST?

Una **API REST (Representational State Transfer)** es un estilo de arquitectura para **comunicación entre sistemas** a través de **HTTP**, usando recursos identificados por URLs.

✔ Simple
✔ Escalable
✔ Independiente de plataforma

---

## 🧱 Conceptos Fundamentales

* **Recurso:** entidad expuesta (usuarios, productos, pedidos)
* **URI:** identificador del recurso
  `/api/usuarios/1`
* **Representación:** formato de intercambio (JSON)
* **Stateless:** cada petición es independiente

---

## 🔁 Métodos HTTP

* **GET** → obtener datos
* **POST** → crear recurso
* **PUT / PATCH** → actualizar
* **DELETE** → eliminar

📍 El verbo define la acción, no la URL

---

## 📊 Códigos de Estado HTTP

* `200 OK` → éxito
* `201 Created` → recurso creado
* `400 Bad Request` → error del cliente
* `401 Unauthorized` → no autenticado
* `403 Forbidden` → sin permisos
* `404 Not Found` → no existe
* `500 Internal Server Error` → error servidor

---

## 🧠 Buenas Prácticas REST

* Usar **nombres en plural** (`/usuarios`)
* No usar verbos en la URL
* Usar códigos HTTP correctos
* Versionar la API (`/api/v1`)
* Mantener la API stateless

---

## 🔐 Seguridad Básica

* Autenticación (JWT, OAuth)
* Autorización por roles
* HTTPS obligatorio
* Validación de entrada

---

## 🎯 Ventajas

* Separación frontend / backend
* Fácil integración con Angular, móviles, terceros
* Escala horizontalmente
* Base de arquitecturas modernas

---

## 📝 Nota para Full Stack

* Angular consume APIs REST
* Java suele exponer APIs REST
* Contrato clave entre capas del sistema

---

**Tip:**
En REST, **la URL representa el recurso** y **el método HTTP la acción**.
