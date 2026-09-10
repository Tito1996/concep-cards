# TARJETA DE ESTUDIO – Seguridad Básica en Backend Java (JWT)


## 📌 ¿Qué es la Seguridad en Backend?

La **seguridad en backend Java** protege los **recursos de la API** asegurando que:

* El usuario sea quien dice ser (**autenticación**)
* El usuario tenga permisos para actuar (**autorización**)

📍 Es responsabilidad **exclusiva del backend**

---

## 🔐 Autenticación

Proceso de **verificar la identidad** del usuario.

Ejemplo:

* Usuario + contraseña
* Token válido (JWT)

✔ Responde a la pregunta:
👉 *¿Quién eres?*

---

## 🛂 Autorización

Proceso de **verificar permisos** sobre un recurso.

Ejemplo:

* Roles (`ADMIN`, `USER`)
* Permisos (`READ_USERS`, `DELETE_ORDER`)

✔ Responde a la pregunta:
👉 *¿Qué puedes hacer?*

---

## 🪪 JWT – JSON Web Token

Un **JWT** es un token **firmado** que contiene información del usuario.

### Estructura

* **Header** → tipo y algoritmo
* **Payload** → datos (id, roles)
* **Signature** → garantiza integridad

📍 El backend **firma** y **valida** el token

---

## 🔄 Flujo de Autenticación con JWT

1. Usuario envía credenciales
2. Backend valida credenciales
3. Backend genera JWT
4. Cliente envía JWT en cada request
5. Backend valida el JWT

📍 El backend es **stateless**

---

## 🛠️ Seguridad en Java (Spring)

* Filtros de seguridad
* Validación de JWT en cada request
* Contexto de seguridad por petición
* Protección de endpoints

✔ Centralizada
✔ Escalable
✔ Transparente

---

## ⚠️ Errores Comunes

* Guardar JWT en backend (rompe stateless)
* JWT sin expiración
* Exponer información sensible en el token
* No validar firma
* Mezclar autenticación con autorización

---

## 🎯 Buenas Prácticas

* Usar HTTPS siempre
* JWT con expiración corta
* Separar roles y permisos
* Proteger endpoints sensibles
* Manejar correctamente `401` y `403`
* Rotar claves de firma

---

## 📝 Nota para Full Stack

* Angular solo **consume** el JWT
* Java **genera, valida y protege**
* La seguridad real vive en el backend

---

**Tip:**
Si un endpoint solo está protegido en el frontend, **no está protegido**. La seguridad siempre debe estar en el **backend Java**.
