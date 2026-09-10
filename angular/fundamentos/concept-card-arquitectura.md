**TARJETA DE ESTUDIO – Arquitectura de Angular**

---

## 📌 ¿Qué es la Arquitectura de Angular?

Angular es un **framework frontend basado en componentes**, diseñado para crear **Single Page Applications (SPA)** escalables, mantenibles y estructuradas.

Se apoya en **TypeScript**, **inyección de dependencias** y una arquitectura modular.

---

## 🧩 Componentes Principales

### 🧱 Componentes

* Unidad básica de la UI
* Combinan **HTML + CSS + TypeScript**
* Manejan la lógica de la vista

✔ Reutilizables
✔ Aislados
✔ Basados en ciclo de vida

---

### 🧰 Módulos (NgModule)

Agrupan funcionalidades relacionadas.

* `AppModule` → módulo raíz
* Módulos de funcionalidades
* Módulos compartidos

✔ Organización
✔ Lazy loading
✔ Escalabilidad

---

### 🔧 Servicios

* Contienen **lógica de negocio**
* Manejan llamadas HTTP y estado compartido
* Se inyectan en componentes

✔ Desacoplamiento
✔ Reutilización
✔ Testeables

---

### 🔄 Data Binding

Conecta vista y lógica:

* One-way binding
* Two-way binding
* Event binding

✔ Sincronización automática UI–estado

---

### 🧭 Routing

* Navegación entre vistas
* Soporte para Lazy Loading
* Guards para seguridad

---

## 🏗️ Flujo Básico

Usuario → Componente → Servicio → API Backend
Respuesta → Servicio → Componente → Vista

---

## 🎯 Beneficios

* Separación clara de responsabilidades
* Código mantenible
* Ideal para aplicaciones grandes
* Compatible con buenas prácticas (SOLID)

---

## 📝 Nota para Full Stack

* Angular = Capa de presentación
* Consume APIs REST (Java)
* Arquitectura alineada con backend en capas

---

**Tip:** Si un componente tiene demasiada lógica, probablemente debería estar en un servicio.
