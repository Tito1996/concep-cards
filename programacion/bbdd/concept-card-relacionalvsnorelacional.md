# BBDD **Relacional** vs **No Relacional** (NoSQL)

---

## Base de Datos Relacional

### ¿Qué es?

Organiza la información en **tablas** con filas y columnas, usando **relaciones** entre ellas mediante claves primarias y foráneas.

### Características Clave

* Esquema **estructurado y fijo**.
* Uso de **SQL**.
* Soporta **ACID** (Atomicidad, Consistencia, Aislamiento, Durabilidad).

### Ejemplos

* MySQL
* PostgreSQL
* Oracle
* SQL Server

---

## Base de Datos No Relacional (NoSQL)

### ¿Qué es?

Almacena datos de forma **flexible**, sin necesidad de un esquema rígido. Está diseñada para **alta escalabilidad y rendimiento**.

### Características Clave

* Esquema **dinámico o inexistente**.
* No siempre usa SQL.
* Prioriza **disponibilidad y escalabilidad** (BASE).

### Tipos Comunes

* **Documentos**: MongoDB
* **Clave–Valor**: Redis
* **Columnas**: Cassandra
* **Grafos**: Neo4j

---

## Diferencias Principales

| Relacional        | No Relacional                     |
| ----------------- | --------------------------------- |
| Tablas            | Documentos / Clave-Valor / Grafos |
| Esquema fijo      | Esquema flexible                  |
| SQL               | Consultas propias                 |
| ACID              | BASE                              |
| Escalado vertical | Escalado horizontal               |

---

## Cuándo Usar Cada Una

### Relacional

* Datos altamente estructurados.
* Transacciones complejas.
* Sistemas financieros o administrativos.

### No Relacional

* Grandes volúmenes de datos.
* Aplicaciones distribuidas.
* Sistemas en tiempo real o Big Data.

---

## Idea Clave

> **Relacional** = consistencia y estructura.
> **No Relacional** = flexibilidad y escalabilidad.
