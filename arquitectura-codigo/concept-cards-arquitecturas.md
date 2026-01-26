# **Arquitecturas de Código**

---

## ¿Qué es una arquitectura de código?

Es la **organización estructural del software**: cómo se dividen responsabilidades, cómo se comunican los componentes y cómo evoluciona el sistema.

---

## Arquitectura Monolítica

### Descripción

Toda la aplicación se despliega como **una sola unidad**.

### Ventajas

* Simplicidad inicial.
* Despliegue sencillo.

### Desventajas

* Escalado limitado.
* Difícil mantenimiento a largo plazo.

### Uso Típico

Aplicaciones pequeñas o MVP.

---

## Arquitectura en Capas (Layered)

### Descripción

Separación por **capas lógicas** (UI, Negocio, Datos).

### Ventajas

* Código organizado.
* Fácil de entender.

### Desventajas

* Dependencias rígidas.
* Menor flexibilidad.

### Uso Típico

Aplicaciones empresariales clásicas.

---

## Arquitectura Cliente–Servidor

### Descripción

Separación entre **cliente** (frontend) y **servidor** (backend).

### Ventajas

* Separación clara de responsabilidades.
* Reutilización del backend.

### Desventajas

* Dependencia de red.

### Uso Típico

Aplicaciones web y móviles.

---

## Arquitectura MVC

### Descripción

Divide la aplicación en **Modelo, Vista y Controlador**.

### Ventajas

* Separación de responsabilidades.
* Facilita mantenimiento.

### Desventajas

* Puede crecer en complejidad.

### Uso Típico

Frameworks web (Spring MVC, ASP.NET MVC).

---

## Arquitectura Hexagonal (Ports & Adapters)

### Descripción

El dominio es el centro; el resto son **adaptadores externos**.

### Ventajas

* Alto desacoplamiento.
* Fácil testeo.

### Desventajas

* Curva de aprendizaje.

### Uso Típico

Sistemas mantenibles y orientados a dominio.

---

## Arquitectura Clean Architecture

### Descripción

Evolución de la hexagonal; reglas estrictas de **dependencias hacia el dominio**.

### Ventajas

* Independencia de frameworks.
* Alta mantenibilidad.

### Desventajas

* Mayor complejidad inicial.

### Uso Típico

Aplicaciones grandes y de larga vida.

---

## Arquitectura de Microservicios

### Descripción

Sistema dividido en **servicios pequeños e independientes**.

### Ventajas

* Escalabilidad independiente.
* Despliegue autónomo.

### Desventajas

* Complejidad operativa.
* Comunicación distribuida.

### Uso Típico

Sistemas distribuidos a gran escala.

---

## Comparación Rápida

| Arquitectura   | Escalabilidad | Complejidad | Mantenibilidad |
| -------------- | ------------- | ----------- | -------------- |
| Monolítica     | Baja          | Baja        | Baja           |
| Capas          | Media         | Media       | Media          |
| MVC            | Media         | Media       | Media          |
| Hexagonal      | Alta          | Alta        | Alta           |
| Clean          | Alta          | Alta        | Muy Alta       |
| Microservicios | Muy Alta      | Muy Alta    | Alta           |

---

## Idea Clave

> No existe una arquitectura perfecta: **la mejor depende del tamaño, equipo y objetivos del sistema**.
