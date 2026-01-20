**TARJETA DE ESTUDIO – Decoradores en Angular / TypeScript**

---

## 📌 ¿Qué es un Decorador?

Un **decorador** es una función especial que **añade metadatos o modifica el comportamiento** de clases, métodos, propiedades o parámetros.

Angular los usa para **definir y configurar la aplicación**.

---

## 🧩 Decoradores de Clase (Angular)

### 🧱 `@Component`

Define un **componente** Angular.

* Selector
* Template (HTML)
* Estilos
* Lógica asociada

📍 Base de la UI

---

### 🧰 `@NgModule`

Define un **módulo**.

* Declara componentes
* Importa módulos
* Provee servicios

📍 Organización y escalabilidad

---

### 🔧 `@Injectable`

Marca una clase como **inyectable**.

* Usado en servicios
* Permite Dependency Injection

📍 Lógica de negocio y servicios compartidos

---

## 🧩 Decoradores de Propiedad

### 🔁 `@Input()`

* Recibe datos desde el componente padre

### 📤 `@Output()`

* Emite eventos al componente padre

📍 Comunicación entre componentes

---

## 🧩 Decoradores de Angular Comunes

* `@ViewChild()` → acceso a elementos de la vista
* `@HostListener()` → escucha eventos del DOM
* `@HostBinding()` → enlaza propiedades del host

---

## 🎯 ¿Para qué sirven los Decoradores?

* Declarar roles (componente, servicio, módulo)
* Configurar comportamiento sin lógica adicional
* Hacer el código declarativo y legible
* Separar configuración de implementación

---

## 📝 Nota para Full Stack

* Decoradores = configuración estructural
* Facilitan la inyección de dependencias
* Clave para entender Angular internamente

---

**Tip:** Si algo en Angular “funciona por arte de magia”, probablemente es gracias a un decorador.
