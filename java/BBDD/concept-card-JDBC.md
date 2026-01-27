# **JDBC (Java Database Connectivity)**

---

## ¿Qué es?

**JDBC** es una **API estándar de Java** que permite **conectarse y comunicarse directamente con bases de datos relacionales** mediante SQL.

---

## Objetivo Principal

* Ejecutar consultas SQL desde Java.
* Gestionar conexiones, sentencias y resultados.
* Tener control total sobre el acceso a datos.

---

## Idea Clave

> Con JDBC, el desarrollador **escribe y controla el SQL directamente**.

---

## Componentes Principales

### Driver JDBC

* Implementación específica del motor de BD.
* Traduce llamadas JDBC a comandos del DB.

### Connection

* Representa la conexión a la base de datos.

### Statement / PreparedStatement

* Ejecutan sentencias SQL.
* `PreparedStatement` previene SQL Injection.

### ResultSet

* Contiene los resultados de una consulta.

---

## Flujo Básico

1. Cargar el **driver**.
2. Crear una **Connection**.
3. Preparar y ejecutar la **consulta SQL**.
4. Procesar el **ResultSet**.
5. Cerrar recursos.

---

## Ejemplo (Java)

```java
Connection conn = DriverManager.getConnection(url, user, pass);
PreparedStatement ps = conn.prepareStatement(
    "SELECT * FROM usuarios WHERE id = ?"
);
ps.setInt(1, 1);
ResultSet rs = ps.executeQuery();
```

---

## Ventajas

* Control total sobre SQL.
* Alto rendimiento.
* Sin abstracciones adicionales.

---

## Desventajas

* Código verboso.
* Mayor riesgo de errores.
* Difícil mantenimiento en proyectos grandes.

---

## Cuándo Usar JDBC

* Consultas complejas y optimizadas.
* Aplicaciones pequeñas o scripts.
* Cuando se requiere máximo control.

---

## Comparación Rápida

* **JDBC**: SQL directo.
* **JPA/Hibernate**: ORM con abstracción.

---

## Idea Clave Final

> JDBC ofrece **máximo control y rendimiento**, a costa de mayor complejidad.
