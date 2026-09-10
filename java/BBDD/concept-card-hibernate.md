# **Hibernate**

---

## ¿Qué es?

**Hibernate** es un **framework ORM (Object–Relational Mapping)** para Java que **implementa la especificación JPA** y permite mapear objetos Java a tablas de bases de datos relacionales.

---

## Objetivo Principal

* Simplificar el acceso a datos.
* Evitar el uso excesivo de SQL.
* Persistir objetos Java de forma transparente.

---

## Idea Clave

> Hibernate permite trabajar con la base de datos **usando objetos**, no tablas.

---

## Componentes Principales

### Entidades

* Clases Java anotadas (`@Entity`).
* Representan tablas de la base de datos.

### Session / EntityManager

* Gestiona el ciclo de vida de las entidades.
* Ejecuta operaciones CRUD.

### SessionFactory

* Crea y gestiona sesiones.
* Costosa de crear, se reutiliza.

---

## Características Clave

* Implementación completa de **JPA**.
* Soporte de **HQL (Hibernate Query Language)**.
* Caché de primer y segundo nivel.
* Gestión automática de relaciones.

---

## Ventajas

* Reduce código repetitivo.
* Independiente del motor de base de datos.
* Alta productividad.
* Integración con Spring.

---

## Desventajas

* Curva de aprendizaje.
* Posibles problemas de rendimiento.
* SQL oculto al desarrollador.

---

## Cuándo Usar Hibernate

* Aplicaciones empresariales Java.
* Proyectos grandes o medianos.
* Sistemas orientados a dominio.

---

## Comparación Rápida

* **Hibernate**: ORM completo.
* **JPA**: especificación.
* **JDBC**: SQL directo.

---

## Idea Clave Final

> Hibernate acelera el desarrollo, pero debe usarse con **buen diseño y conocimiento**.
