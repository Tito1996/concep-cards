# TARJETA DE ESTUDIO – ORM y Mapeo Objeto-Relacional (Spring Boot)

---

## 📌 ¿Qué es ORM?

El **ORM (Object–Relational Mapping)** es una técnica que permite **mapear objetos Java a tablas de base de datos** y viceversa.

✔ Objetos ↔ Tablas
✔ Atributos ↔ Columnas
✔ Clases ↔ Entidades

📍 El desarrollador trabaja con **objetos**, no con SQL directo.

---

## ☕ ORM en Spring Boot

En Spring Boot, el ORM se implementa principalmente con:

* **JPA (Jakarta Persistence API)** → estándar
* **Hibernate** → implementación más usada

📍 Spring Boot abstrae la complejidad de configuración.

---

## 🧱 Entidades (Entities)

Una **entidad** es una clase Java que representa una tabla.

Características:

* Anotada con `@Entity`
* Tiene una clave primaria (`@Id`)
* Debe tener constructor vacío

📍 Cada instancia = una fila en la tabla

---

## 🔑 Mapeo Básico

* `@Entity` → clase persistente
* `@Table` → tabla
* `@Id` → clave primaria
* `@GeneratedValue` → autogeneración
* `@Column` → columna

✔ Declarativo
✔ Legible
✔ Estándar JPA

---

## 🔗 Relaciones entre Entidades

ORM gestiona relaciones automáticamente:

* **OneToOne**
* **OneToMany**
* **ManyToOne**
* **ManyToMany**

📍 Se definen con anotaciones y claves foráneas.

---

## 🗄️ Repositorios (Spring Data JPA)

Spring Boot usa **repositories** para acceder a datos.

Características:

* Interfaces, no clases
* CRUD automático
* Queries derivadas por nombre

✔ Menos código
✔ Más productividad
✔ Menos errores

---

## 🔄 Ciclo de Vida de Entidades

Una entidad puede estar:

* **Transient** → no persistida
* **Managed** → controlada por el ORM
* **Detached** → fuera del contexto
* **Removed** → marcada para borrar

📍 El ORM gestiona automáticamente este ciclo.

---

## ⚠️ Errores Comunes

* Exponer entidades directamente en la API
* No entender `fetch = LAZY / EAGER`
* Relaciones mal diseñadas
* Abusar de `cascade`
* Ignorar el impacto en performance

---

## 🎯 Buenas Prácticas

* Usar **DTOs**, no entidades en controllers
* Mantener entidades simples
* Controlar bien las relaciones
* Entender lazy loading
* Diseñar el modelo pensando en consultas

---

## 📝 Nota para Backend Java

* ORM acelera el desarrollo
* Reduce código repetitivo
* Mal usado, genera problemas de rendimiento
* Bien entendido, es una gran ventaja

---

**Tip:**
ORM no elimina la necesidad de entender SQL.
Si no sabes cómo se consulta la base, **no sabes realmente qué hace tu ORM**.
