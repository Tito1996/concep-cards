# **Arquitectura en Capas**

---

## ¿Qué es?

La **arquitectura en capas** organiza una aplicación dividiéndola en **niveles jerárquicos**, donde cada capa tiene una responsabilidad específica y se comunica con la capa adyacente.

---

## Capas Típicas

1. **Presentación**

   * Interfaz de usuario.
   * Controladores.

2. **Aplicación / Servicios**

   * Orquesta casos de uso.
   * Coordina la lógica.

3. **Negocio / Dominio**

   * Reglas de negocio.
   * Entidades y lógica central.

4. **Persistencia / Datos**

   * Acceso a bases de datos.
   * Repositorios.

---

## Características Principales

* Separación clara de responsabilidades.
* Dependencias de arriba hacia abajo.
* Capas intercambiables.

---

## Ventajas

* Código organizado y legible.
* Fácil mantenimiento.
* Permite trabajo en equipo.

---

## Desventajas

* Dependencias rígidas entre capas.
* Menor flexibilidad para cambios grandes.
* Riesgo de lógica duplicada.

---

## Cuándo Usarla

* Aplicaciones empresariales.
* Sistemas medianos.
* Proyectos con requisitos estables.

---

## Ejemplos de Uso

* Aplicaciones Java EE / Spring.
* Aplicaciones .NET.
* Sistemas CRUD.

---

## Comparación Rápida

* **Capas**: separación lógica clara.
* **Monolítica**: una sola unidad.
* **Hexagonal**: dominio como centro.

---

## Idea Clave

> Cada capa tiene una responsabilidad clara y **no conoce los detalles internos** de las demás.
