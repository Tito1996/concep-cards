# **JPA (Java Persistence API)**

---

## ¿Qué es?

**JPA** es una **especificación de Java** que define cómo **mapear objetos Java a bases de datos relacionales** (ORM: Object–Relational Mapping).

---

## Objetivo Principal

* Facilitar la persistencia de datos en Java.
* Reducir el uso directo de SQL.
* Trabajar con la base de datos usando **objetos**.

---

## Idea Clave

> JPA permite trabajar con la base de datos **como si fueran objetos Java**.

---

## Componentes Principales

### Entidad (@Entity)

* Clase Java que representa una tabla.
* Cada objeto es una fila.

### EntityManager

* Gestiona el ciclo de vida de las entidades.
* Realiza operaciones CRUD.

### Persistence Unit

* Configuración de conexión y entidades.

---

## Operaciones Básicas (CRUD)

* **persist()** → crear
* **find()** → leer
* **merge()** → actualizar
* **remove()** → eliminar

---

## Anotaciones Comunes

* `@Entity`
* `@Id`
* `@GeneratedValue`
* `@Column`
* `@OneToMany`, `@ManyToOne`

---

## Proveedores JPA

JPA es una especificación; se implementa con:

* **Hibernate** (más usado)
* EclipseLink
* OpenJPA

---

## Ventajas

* Menos código SQL.
* Independencia del proveedor.
* Código más limpio y mantenible.

---

## Desventajas

* Curva de aprendizaje.
* Puede ocultar consultas ineficientes.
* Impacto en rendimiento si se usa mal.

---

## Cuándo Usar JPA

* Aplicaciones Java empresariales.
* Sistemas con bases de datos relacionales.
* Proyectos que priorizan mantenibilidad.

---

## Comparación Rápida

* **JPA**: especificación ORM.
* **Hibernate**: implementación JPA.
* **JDBC**: acceso directo con SQL.

---

## Idea Clave Final

> JPA abstrae la persistencia para que el desarrollador se enfoque en el **dominio**, no en SQL.
