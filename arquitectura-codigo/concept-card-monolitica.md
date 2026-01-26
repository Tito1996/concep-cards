# **Arquitectura Monolítica**

---

## ¿Qué es?

La **arquitectura monolítica** es un estilo donde **toda la aplicación se desarrolla, despliega y ejecuta como una sola unidad**. Todos los módulos están fuertemente integrados.

---

## Características Principales

* Un único proyecto y despliegue.
* Componentes altamente acoplados.
* Una sola base de código.
* Comunicación interna directa (sin red).

---

## Estructura Típica

* Capa de presentación (UI / Controllers)
* Lógica de negocio
* Acceso a datos
* Base de datos compartida

---

## Ventajas

* Simplicidad de desarrollo inicial.
* Despliegue sencillo.
* Fácil de depurar.
* Buen rendimiento interno.

---

## Desventajas

* Difícil escalado (se escala todo o nada).
* Mantenimiento complejo en sistemas grandes.
* Cambios pequeños requieren desplegar todo.
* Menor flexibilidad tecnológica.

---

## Cuándo Usarla

* Aplicaciones pequeñas o medianas.
* MVP (Producto Mínimo Viable).
* Equipos pequeños.
* Requisitos bien definidos.

---

## Ejemplos de Uso

* Aplicaciones empresariales tradicionales.
* Sistemas internos.
* Proyectos académicos.

---

## Comparación Rápida

* **Monolítica**: una sola aplicación.
* **Microservicios**: múltiples servicios independientes.

---

## Idea Clave

> La arquitectura monolítica es **simple y efectiva al inicio**, pero puede volverse rígida a gran escala.
