**TARJETA DE ESTUDIO – Módulos, Componentes y Servicios (Angular)**

---

## 📌 Conceptos Clave en Angular

Angular organiza una aplicación usando **módulos**, **componentes** y **servicios**, cada uno con una **responsabilidad clara**.

---

## 🧱 Módulos (NgModule)

Agrupan funcionalidades relacionadas.

* Declaran componentes, directivas y pipes
* Importan otros módulos
* Permiten **Lazy Loading**

**Ejemplos:**

* `AppModule` → módulo raíz
* `AuthModule`, `UserModule` → módulos de funcionalidad

✔ Organización
✔ Escalabilidad
✔ Mejor rendimiento

---

## 🧩 Componentes

Unidad básica de la interfaz de usuario.

* Combinan **HTML + CSS + TypeScript**
* Controlan la vista
* Responden a eventos del usuario

**Responsabilidad:**
👉 Mostrar datos y manejar interacción, **no lógica de negocio**

✔ Reutilizables
✔ Aislados
✔ Basados en ciclo de vida

---

## 🔧 Servicios

Contienen la **lógica de negocio** y operaciones compartidas.

* Llamadas HTTP
* Manejo de estado
* Utilidades comunes

Se inyectan mediante **Dependency Injection**.

✔ Desacoplamiento
✔ Reutilización
✔ Fácil testing

---

## 🔄 Relación entre ellos

Componente → usa → Servicio
Módulo → organiza → Componentes y Servicios

---

## 🎯 Buenas Prácticas

* Componentes simples y livianos
* Lógica en servicios
* Módulos por funcionalidad
* Servicios reutilizables y desacoplados

---

## 📝 Nota para Full Stack

* Angular sigue principios similares al backend Java
* Facilita integración con APIs REST
* Base para aplicaciones SPA profesionales

---

**Tip:** Si un componente “piensa demasiado”, muévelo a un servicio.
