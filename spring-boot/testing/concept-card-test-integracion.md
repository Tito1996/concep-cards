# Tema: Integración y comportamiento real del sistema


## 📌 ¿Qué es el Testing de Integración?

El **testing de integración** verifica que **varios componentes trabajen correctamente juntos** dentro de la aplicación.

✔ Componentes reales
✔ Flujo completo
✔ Configuración real o cercana a producción

---

## ☕ Testing de Integración en Spring Boot

En Spring Boot, los tests de integración:

* **Levantan el contexto de Spring**
* Usan beans reales
* Validan la interacción entre capas

📍 Más lentos que los unitarios, pero más realistas.

---

## 🧱 ¿Qué se Testea?

* Controladores REST
* Servicios + repositorios
* Validaciones
* Serialización / deserialización
* Configuración de seguridad

✔ Flujo end-to-end dentro del backend

---

## 🛠️ Herramientas y Anotaciones Clave

* `@SpringBootTest`
* `@AutoConfigureMockMvc`
* `@ActiveProfiles("test")`
* `@Test`
* **MockMvc** → simula llamadas HTTP

📍 Spring levanta el ApplicationContext completo.

---

## 🌐 Testing de Controladores (REST)

Se prueban endpoints como si fueran llamados por un cliente.

Aspectos validados:

* Código HTTP
* Request / Response
* JSON devuelto
* Validaciones y errores

📍 Sin necesidad de levantar servidor real.

---

## 🗄️ Base de Datos en Tests

Opciones comunes:

* Base en memoria (H2)
* Contenedores (Testcontainers)
* Base real aislada para tests

📍 Nunca usar la base de producción.

---

## ⚠️ Errores Comunes

* Confundir test unitario con integración
* No aislar entorno de test
* Tests frágiles y lentos
* Compartir estado entre tests
* No limpiar datos

---

## 🎯 Buenas Prácticas

* Separar tests unitarios e integración
* Usar perfiles de configuración (`test`)
* Mantener tests independientes
* Probar flujos críticos, no todo
* Ejecutarlos en CI/CD

---

## 📝 Nota para Backend Java

* Detectan errores de configuración
* Validan contratos reales de la API
* Complementan al testing unitario
* Aumentan confianza en despliegues

---

**Tip:**
Si un test levanta Spring y prueba varias capas juntas, **no es unitario**: es un **test de integración**, y eso está bien.
