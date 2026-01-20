**TARJETA DE ESTUDIO – Flujos de Trabajo en Git**
**Formato:** A6

---

## 📌 ¿Qué es un flujo de trabajo en Git?

Conjunto de **reglas y prácticas** que definen **cómo se crean, usan y fusionan las ramas** en un proyecto para trabajar en equipo de forma ordenada y segura.

---

## 🌊 Git Flow

Flujo estructurado basado en **múltiples ramas permanentes**.

### Ramas principales

* `main` → código en producción
* `develop` → integración de funcionalidades

### Ramas de apoyo

* `feature/*` → nuevas funcionalidades
* `release/*` → preparación de versiones
* `hotfix/*` → correcciones urgentes en producción

### Ventajas

✔ Muy organizado
✔ Ideal para proyectos grandes
✔ Control claro de versiones

### Desventajas

❌ Más complejo
❌ Más lento para despliegues frecuentes

📍 Usado en equipos tradicionales y proyectos con releases planificados

---

## 🚆 Trunk-Based Development

Flujo simple basado en **una rama principal (`main`)**.

### Características

* Commits pequeños y frecuentes
* Ramas muy cortas o inexistentes
* Integración continua constante

### Ventajas

✔ Historial simple
✔ Despliegues rápidos
✔ Ideal para CI/CD

### Desventajas

❌ Requiere alta disciplina
❌ Tests automatizados obligatorios

📍 Usado en equipos ágiles y DevOps maduros

---

## 🧠 Comparación Rápida

* **Git Flow:** control y estabilidad
* **Trunk-Based:** velocidad y simplicidad

---

## 📝 Nota para Full Stack

* Proyectos empresariales → Git Flow
* Startups / CI-CD → Trunk-Based
* Ambos requieren buenas prácticas de commits y code reviews

---

**Tip:** El mejor flujo no es el más complejo, sino el que el equipo puede cumplir consistentemente.
