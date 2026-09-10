# TARJETA DE ESTUDIO – Stateless en Backend Java

---

## 📌 ¿Qué significa Stateless?

Un backend **stateless** no guarda **estado de sesión del cliente** entre peticiones.
Cada request contiene **toda la información necesaria** para ser procesada.

✔ Peticiones independientes
✔ Sin memoria de sesión en el servidor

---

## 🧱 Stateless en APIs REST (Java)

En APIs REST:

* El servidor **no almacena sesiones**
* La autenticación viaja en cada request (ej. JWT)
* El backend puede atender cualquier petición sin contexto previo

📍 Principio fundamental de REST

---

## 🔄 Comparación: Stateful vs Stateless

### ❌ Stateful

* Sesión en memoria del servidor
* Escala mal
* Dependencia del servidor

### ✅ Stateless

* Sin sesión en servidor
* Escalabilidad horizontal
* Fácil balanceo de carga

---

## 🪪 Relación con JWT

JWT es ideal para arquitecturas stateless:

* El token contiene identidad y roles
* El backend **valida**, no guarda
* No hay sesión persistida

📍 Stateless + JWT = patrón estándar moderno

---

## 🛠️ Stateless en Java (Spring)

* Controllers sin estado
* Servicios sin variables de sesión
* Seguridad basada en tokens
* Contexto de seguridad por request

✔ Diseño limpio
✔ Alta concurrencia
✔ Cloud-ready

---

## ⚠️ Errores Comunes

* Guardar usuario en memoria
* Usar sesiones HTTP
* Mantener estado en servicios singleton
* Depender del orden de llamadas
* Usar stateless solo “a medias”

---

## 🎯 Buenas Prácticas

* Diseñar APIs idempotentes
* Incluir autenticación en cada request
* No almacenar datos de sesión
* Externalizar estado (DB, cache)
* Pensar cada request como independiente

---

## 📝 Nota para Backend Java

* Stateless facilita microservicios
* Permite escalar sin complejidad
* Reduce errores de concurrencia
* Base para arquitecturas modernas

---

**Tip:**
Si tu backend necesita “recordar” al usuario entre peticiones, el diseño **no es stateless**. El estado debe viajar con la request o vivir fuera del servidor.
