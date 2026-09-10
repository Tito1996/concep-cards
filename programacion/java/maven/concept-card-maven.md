# **Maven**

---

## ¿Qué es?

**Apache Maven** es una herramienta de **gestión y automatización de proyectos Java** que facilita la **compilación, pruebas, empaquetado y gestión de dependencias**.

---

## Idea Clave

> Maven estandariza **cómo se construye y gestiona** un proyecto Java.

---

## Problemas que Resuelve

* Gestión manual de librerías.
* Builds inconsistentes.
* Dependencias faltantes o incompatibles.

---

## Archivo Principal: `pom.xml`

El **POM (Project Object Model)** define:

* Información del proyecto.
* Dependencias.
* Plugins.
* Ciclo de vida del build.

---

## Estructura Estándar

```
src/
 ├─ main/java
 ├─ main/resources
 ├─ test/java
 └─ test/resources
```

---

## Gestión de Dependencias

* Las dependencias se descargan automáticamente.
* Se almacenan en el **repositorio local** (`.m2`).

Ejemplo:

```xml
<dependency>
  <groupId>org.springframework</groupId>
  <artifactId>spring-core</artifactId>
  <version>6.0.0</version>
</dependency>
```

---

## Ciclo de Vida de Maven

### Fases Principales

* **clean** → limpia el proyecto
* **compile** → compila el código
* **test** → ejecuta pruebas
* **package** → genera JAR/WAR
* **install** → instala en repo local
* **deploy** → publica el artefacto

---

## Ventajas

* Gestión automática de dependencias.
* Estructura estándar.
* Integración con IDEs y CI/CD.

---

## Desventajas

* Curva de aprendizaje.
* Configuración extensa en XML.

---

## Cuándo Usar Maven

* Proyectos Java medianos y grandes.
* Equipos de desarrollo.
* Integración continua.

---

## Comparación Rápida

* **Maven**: declarativo, XML.
* **Gradle**: más flexible, DSL.

---

## Idea Clave Final

> Maven automatiza el build y dependencias para proyectos Java de forma **estándar y reproducible**.
