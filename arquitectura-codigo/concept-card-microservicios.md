# **Arquitectura de Microservicios**

---

## ¿Qué es?

La **arquitectura de microservicios** divide una aplicación en **servicios pequeños, autónomos y desplegables de forma independiente**, que se comunican entre sí mediante APIs.

---

## Objetivo Principal

* Escalar y desplegar partes del sistema de forma independiente.
* Reducir el acoplamiento entre componentes.
* Acelerar la evolución del software.

---

## Idea Clave

> Cada microservicio es **dueño de su lógica y sus datos**.

---

## Características Principales

* Servicios pequeños y especializados.
* Despliegue independiente.
* Comunicación por red (HTTP/REST, gRPC, mensajería).
* Base de datos **por servicio**.
* Tolerancia a fallos.

---

## Componentes Comunes

* **API Gateway**: punto de entrada único.
* **Service Discovery**: localización de servicios.
* **Balanceo de carga**.
* **Mensajería** (eventos).
* **Observabilidad** (logs, métricas, tracing).

---

## Ventajas

* Escalabilidad independiente.
* Flexibilidad tecnológica.
* Equipos autónomos.
* Despliegues frecuentes.

---

## Desventajas

* Alta complejidad operativa.
* Comunicación distribuida.
* Gestión de datos compleja.
* Requiere madurez del equipo.

---

## Cuándo Usarla

* Sistemas grandes y distribuidos.
* Equipos múltiples.
* Alta demanda de escalabilidad.

---

## Comparación Rápida

* **Microservicios**: servicios independientes.
* **Monolítica**: una sola aplicación.
* **Capas**: separación lógica interna.

---

## Idea Clave Final

> Microservicios ofrecen **flexibilidad y escalabilidad**, a costa de mayor complejidad.
