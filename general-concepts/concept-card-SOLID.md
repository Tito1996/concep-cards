**TARJETA DE ESTUDIO – Principios SOLID**

---

### 📌 ¿Qué son los Principios SOLID?

Conjunto de **5 principios de diseño de software** orientados a crear código **mantenible, escalable y flexible**, especialmente en programación orientada a objetos.

---

### 🧩 S – Single Responsibility Principle (SRP)

**Una clase debe tener una sola responsabilidad.**
✔ Un único motivo para cambiar.
❌ Clases con múltiples funciones.

**Ejemplo:**

* `UsuarioService` → lógica de negocio
* `UsuarioRepository` → acceso a datos

---

### 🧩 O – Open/Closed Principle (OCP)

**Abierto para extensión, cerrado para modificación.**
✔ Agregar comportamiento sin modificar código existente.
✔ Uso de interfaces y herencia.

---

### 🧩 L – Liskov Substitution Principle (LSP)

**Una subclase debe poder reemplazar a su clase base sin romper el sistema.**
✔ Las subclases respetan el contrato de la clase padre.
❌ Métodos sobrescritos con comportamientos incompatibles.

---

### 🧩 I – Interface Segregation Principle (ISP)

**Mejor muchas interfaces pequeñas que una grande.**
✔ Evita depender de métodos que no se usan.
✔ Interfaces específicas y cohesionadas.

---

### 🧩 D – Dependency Inversion Principle (DIP)

**Depender de abstracciones, no de implementaciones.**
✔ Uso de interfaces
✔ Inyección de dependencias
✔ Bajo acoplamiento

---

### 🎯 Beneficios de SOLID

* Código más limpio y entendible
* Facilita testing y mantenimiento
* Reduce efectos colaterales
* Base para arquitecturas profesionales

---

### 📝 Nota para Full Stack (Java / Angular)

* Java: servicios, repositorios, controladores
* Angular: servicios, componentes desacoplados
* Esencial para proyectos escalables y trabajo en equipo

---

**Tip:** Si una clase viola SOLID, probablemente crecerá descontroladamente y será difícil de mantener.
