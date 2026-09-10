**TARJETA DE ESTUDIO – Formularios en Angular**
**Formato:** A6
**Tema:** Template-driven vs Reactive Forms

---

## 📌 ¿Para qué sirven los Formularios?

Permiten **capturar, validar y procesar datos del usuario**.
Angular ofrece **dos enfoques distintos**, cada uno con casos de uso claros.

---

## 🧩 Template-driven Forms

Formulario **controlado desde el HTML**.

### Características

* Usa directivas (`ngModel`, `ngForm`)
* Lógica implícita
* Menos código TypeScript
* Basado en *two-way binding*

✔ Fácil de aprender
✔ Ideal para formularios simples
❌ Poco escalable
❌ Difícil de testear

📍 Requiere `FormsModule`

---

## 🧱 Reactive Forms

Formulario **controlado desde TypeScript**.

### Características

* Modelo explícito (`FormGroup`, `FormControl`)
* Validaciones declarativas
* Manejo reactivo con RxJS
* Flujo de datos predecible

✔ Escalable
✔ Testeable
✔ Mayor control
❌ Más código inicial

📍 Requiere `ReactiveFormsModule`

---

## 🧠 Comparación Rápida

* **Template-driven:**
  → Simple, rápido, poco control

* **Reactive Forms:**
  → Complejo, robusto, profesional

---

## 🎯 Validaciones

* **Built-in:** `required`, `minLength`, `email`
* **Custom:** funciones propias
* **Async:** validaciones con API

✔ Reactive Forms facilita validaciones complejas

---

## 📝 ¿Cuál usar?

* Formularios pequeños → **Template-driven**
* Formularios complejos / empresariales → **Reactive Forms**
* Proyectos profesionales → **Reactive Forms (recomendado)**

---

## 📝 Nota para Full Stack

* Formularios = punto crítico de UX
* Conectan directamente con APIs backend
* Reactive Forms se alinean mejor con arquitecturas Java

---

**Tip:**
Si el formulario tiene lógica, validaciones o crecimiento futuro, **usa Reactive Forms desde el inicio**.
