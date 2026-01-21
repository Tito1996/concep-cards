**TARJETA DE ESTUDIO – Arquitectura de Microservicios**

---

## 📌 ¿Qué son los Microservicios?

Estilo de arquitectura donde una aplicación se divide en **servicios pequeños, independientes y autónomos**, que se comunican entre sí mediante **APIs**.

Cada microservicio:

* Tiene una **responsabilidad específica**
* Se desarrolla, despliega y escala de forma independiente

---

## 🧩 Características Clave

* Servicios desacoplados
* Comunicación vía HTTP/REST o mensajería
* Cada servicio puede tener su propia base de datos
* Despliegue independiente
* Alta escalabilidad

---

## 🏗️ Ejemplo en un Sistema

* Servicio de Usuarios
* Servicio de Autenticación
* Servicio de Productos
* Servicio de Órdenes

Cada uno:

* API propia
* Lógica de negocio aislada
* Posible base de datos independiente

---

## ✅ Ventajas

* Escala solo lo necesario
* Facilita equipos grandes
* Menor impacto ante fallos
* Permite usar distintas tecnologías

---

## ❌ Desventajas

* Mayor complejidad técnica
* Comunicación distribuida
* Requiere monitoreo y DevOps
* Testing más complejo

---

## 🧱 Comparación Rápida

* **Monolito:** simple, rápido de iniciar
* **Microservicios:** complejo, escalable y robusto

---

## 📝 Nota para Full Stack

* Backend Java: servicios REST independientes
* Frontend Angular: consume múltiples APIs
* PostgreSQL: una DB por servicio (ideal)

---

**Tip:** No empieces con microservicios sin necesidad. Son una solución a problemas de escala, no un punto de partida obligatorio.
