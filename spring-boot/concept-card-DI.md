# TARJETA DE ESTUDIO – Inyección de Dependencias en Spring Boot


## 📌 ¿Qué es la Inyección de Dependencias?

La **Inyección de Dependencias (DI)** es un patrón donde **Spring Boot crea y gestiona los objetos** y los **inyecta automáticamente** donde se necesitan.

✔ Bajo acoplamiento
✔ Código mantenible
✔ Testing sencillo

---

## 🧱 Contenedor de Spring

Spring Boot usa un **IoC Container (Inversion of Control)** que:

* Crea los beans
* Gestiona su ciclo de vida
* Resuelve dependencias

📍 El desarrollador **no usa `new`**

---

## 🧩 ¿Qué es un Bean?

Un **Bean** es un objeto gestionado por Spring.

Se define con anotaciones como:

* `@Component`
* `@Service`
* `@Repository`
* `@Controller`
* `@RestController`

✔ Spring los detecta automáticamente

---

## 🔄 Formas de Inyección

### ✅ Inyección por Constructor (RECOMENDADA)

* Dependencias obligatorias
* Inmutabilidad
* Mejor testing

📍 Estándar profesional en Spring Boot

---

### ⚠️ Inyección por Campo (`@Autowired`)

* Menos clara
* Difícil de testear
* No recomendada en proyectos serios

---

### ⚠️ Inyección por Setter

* Útil solo para dependencias opcionales

---

## 📦 Scopes de Beans

* **Singleton (default)** → una instancia por aplicación
* **Prototype** → nueva instancia cada vez
* **Request / Session** → web

📍 Elegir mal el scope genera bugs de concurrencia

---

## 🎯 Beneficios Clave

* Separación de responsabilidades
* Sustitución fácil de implementaciones
* Código desacoplado
* Facilita mocks y tests unitarios

---

## ⚠️ Errores Comunes

* Usar `new` en lugar de DI
* Beans con demasiadas responsabilidades
* Dependencias circulares
* Usar mal los scopes
* Abusar de `@Autowired`

---

## 🎯 Buenas Prácticas

* Preferir **inyección por constructor**
* Programar contra **interfaces**
* Mantener beans pequeños y cohesionados
* Un bean = una responsabilidad
* Dejar que Spring gestione todo

---

## 📝 Nota para Backend Java

* DI es el corazón de Spring Boot
* Base de aplicaciones escalables
* Sin DI, Spring pierde sentido

---

**Tip:**
Si una clase en Spring Boot crea sus dependencias con `new`, **estás rompiendo la arquitectura** y desaprovechando el framework.
