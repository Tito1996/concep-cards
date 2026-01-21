**TARJETA DE ESTUDIO – Patrones de Diseño**

---

### 📌 ¿Qué son los Patrones de Diseño?

Soluciones **probadas y reutilizables** a problemas comunes de diseño de software.
No son código listo, sino **estructuras y buenas prácticas**.

---

## 🧩 Patrones Clave en Full Stack

### 🏗️ MVC – Model View Controller

**Separa responsabilidades en tres capas:**

* **Model:** lógica de negocio y datos
* **View:** interfaz de usuario
* **Controller:** gestiona peticiones y coordina

✔ Organización clara
✔ Fácil mantenimiento
📍 Usado en Angular y frameworks Java

---

### 🗄️ Repository

**Encapsula el acceso a datos.**

* Separa la lógica de negocio de la persistencia
* Centraliza consultas a la base de datos

✔ Código desacoplado
✔ Facilita testing
📍 Muy usado con ORM en Java

---

### 🔒 Singleton

**Garantiza una única instancia de una clase.**

* Acceso global controlado
* Ideal para recursos compartidos

✔ Ahorro de recursos
❌ Usar con cuidado (puede generar acoplamiento)

**Ejemplo:** gestor de configuración o logging

---

### 🏭 Factory

**Centraliza la creación de objetos.**

* Decide qué implementación instanciar
* Evita dependencias directas

✔ Flexibilidad
✔ Cumple Open/Closed Principle
📍 Muy usado con interfaces

---

## 🎯 Beneficios Generales

* Código más limpio y estructurado
* Reutilización de soluciones
* Escalabilidad y mantenibilidad
* Base para arquitecturas profesionales

---

### 📝 Nota para Full Stack

* Backend Java: MVC, Repository, Factory
* Frontend Angular: MVC/MVVM, servicios
* Claves para trabajar en equipo y proyectos grandes

---

**Tip:** No memorices los patrones. Entiende **cuándo** y **por qué** usarlos.
