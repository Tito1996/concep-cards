#TARJETA DE ESTUDIO – Testing Unitario en Spring Boot


## 📌 ¿Qué es el Testing Unitario?

El **testing unitario** verifica el **comportamiento de una unidad de código** (clase o método) de forma **aislada**, sin depender de base de datos, red o framework completo.

✔ Rápido
✔ Automático
✔ Aislado

---

## ☕ Testing Unitario en Spring Boot

En Spring Boot, el testing unitario se centra en:

* **Servicios**
* **Lógica de negocio**
* **Clases independientes**

📍 No levanta el contexto completo de Spring.

---

## 🧪 Herramientas Principales

* **JUnit 5** → framework de testing
* **Mockito** → mocks y stubs
* **AssertJ / Hamcrest** → aserciones expresivas

📍 Spring Boot las incluye por defecto.

---

## 🧱 ¿Qué se Testea?

* Métodos de servicios
* Reglas de negocio
* Casos límite
* Excepciones esperadas

❌ No controladores
❌ No repositorios reales
❌ No base de datos

---

## 🧩 Mocks (Concepto Clave)

Un **mock** simula dependencias externas.

Ejemplos:

* Repositorios
* Clientes HTTP
* Servicios externos

✔ Permiten aislar la unidad
✔ Evitan efectos colaterales

---

## 🛠️ Anotaciones Comunes

* `@ExtendWith(MockitoExtension.class)`
* `@Mock`
* `@InjectMocks`
* `@BeforeEach`
* `@Test`

📍 Testing sin levantar Spring Context

---

## ⚠️ Errores Comunes

* Testear demasiadas cosas juntas
* No usar mocks
* Tests dependientes entre sí
* Nombres de tests poco claros
* Confundir test unitario con integración

---

## 🎯 Buenas Prácticas

* Un test = un comportamiento
* Nombres descriptivos (`shouldReturnErrorWhenUserNotFound`)
* Tests rápidos y deterministas
* Mockear solo dependencias externas
* Mantener tests simples y legibles

---

## 📝 Nota para Backend Java

* Tests unitarios detectan bugs temprano
* Facilitan refactorización
* Reducen miedo al cambio
* Son la base de CI/CD confiable

---

**Tip:**
Si un test necesita base de datos o levantar Spring completo, **no es unitario**: es un test de integración.
