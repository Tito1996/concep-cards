**TARJETA DE ESTUDIO – Servicios Compartidos en Angular**

---

## 📌 ¿Qué es un Servicio Compartido?

Un **servicio compartido** es una clase Angular que **centraliza lógica o estado** y puede ser **inyectada en múltiples componentes**.

Permite **comunicación y reutilización** sin acoplar componentes entre sí.

---

## 🎯 ¿Para qué se usan?

* Compartir datos entre componentes
* Llamadas HTTP a APIs
* Manejo de estado simple
* Lógica reutilizable
* Utilidades comunes

---

## 🧱 Características Clave

* Decorado con `@Injectable`
* Se inyecta mediante **Dependency Injection**
* Vive mientras viva su **scope** (app, módulo o componente)
* Puede usar **RxJS** para datos reactivos

---

## 🔄 Comunicación entre Componentes

### Componentes no relacionados

* Servicio actúa como intermediario
* Uso de:

  * `Subject`
  * `BehaviorSubject`
  * `Observable`

✔ Evita pasar datos por múltiples niveles
✔ Arquitectura limpia

---

## 🧠 Ejemplo de Uso Típico

* `AuthService` → usuario autenticado
* `SharedDataService` → estado compartido
* `NotificationService` → mensajes globales

---

## ⚙️ Scope del Servicio

* **Root (`providedIn: 'root'`)**
  → Singleton en toda la aplicación
* **Módulo o Componente**
  → Nueva instancia por contexto

📍 Elegir el scope correctamente es clave

---

## 🎯 Buenas Prácticas

* Una responsabilidad por servicio
* No poner lógica de UI
* Usar Observables para estado reactivo
* Evitar servicios “Dios”
* Nombrar claramente (`UserService`, `CartService`)

---

## 📝 Nota para Full Stack

* Equivalente a servicios en backend Java
* Facilitan consumo de APIs REST
* Base para aplicaciones Angular escalables

---

**Tip:** Si dos componentes necesitan la misma información, probablemente necesitas un servicio compartido.
