**TARJETA DE ESTUDIO – Reactive Forms en Angular**

---

## 📌 ¿Qué son los Reactive Forms?

Los **Reactive Forms** son un enfoque para crear formularios **controlados desde TypeScript**, con un **modelo explícito y reactivo**.

Se basan en **Observables**, lo que permite mayor control, escalabilidad y testeo.

---

## 🧱 Elementos Principales

* **FormControl** → controla un campo individual
* **FormGroup** → agrupa controles
* **FormArray** → listas dinámicas de controles
* **Validators** → validaciones síncronas y asíncronas

📍 Requiere importar `ReactiveFormsModule`

---

## 🔄 Flujo de Datos

TypeScript → Modelo del formulario → HTML
✔ Flujo unidireccional
✔ Estado siempre sincronizado

---

## 🧠 Características Clave

* Modelo explícito
* Validaciones declarativas
* Control total del estado (`valid`, `invalid`, `touched`, `dirty`)
* Fácil testing
* Integración nativa con RxJS

---

## 🛡️ Validaciones

### Built-in

* `required`
* `minLength`
* `email`
* `pattern`

### Custom

* Funciones propias
* Validaciones asíncronas (API)

✔ Manejo avanzado de reglas de negocio

---

## 🎯 ¿Cuándo usar Reactive Forms?

* Formularios complejos
* Validaciones avanzadas
* Formularios dinámicos
* Proyectos empresariales
* Necesidad de testing

---

## ⚠️ Buenas Prácticas

* Definir el formulario en `ngOnInit`
* Usar getters para acceder a controles
* Centralizar validaciones
* Evitar lógica en el template
* Usar `valueChanges` con moderación

---

## 📝 Nota para Full Stack

* Reactive Forms se alinean con backend Java
* Facilitan mapeo a DTOs
* Reducen errores de validación cliente–servidor

---

**Tip:**
Si el formulario tiene lógica o va a crecer, **Reactive Forms no son opcionales, son obligatorios**.
