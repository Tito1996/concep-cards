## TARJETA DE ESTUDIO – ExecutorService en Java**
**Formato:** A6

---

## 📌 ¿Qué es ExecutorService?

Es una abstracción de alto nivel para **gestionar y reutilizar hilos**, evitando crearlos manualmente.

---

## 🧱 ¿Qué Problema Resuelve?

- Creación excesiva de hilos
- Gestión manual compleja
- Falta de control sobre ejecución

---

## 🛠️ Uso Básico

```java
ExecutorService executor = Executors.newFixedThreadPool(4);
executor.submit(() -> doWork());
executor.shutdown();
````

---

## ⚠️ Errores Comunes

* No cerrar el executor (`shutdown`)
* Usar pools incorrectos
* Lanzar tareas infinitas

---

## 🎯 Buenas Prácticas (Nivel Mid)

* Preferir `ExecutorService` sobre `Thread`
* Elegir el pool según el tipo de tarea
* Controlar el ciclo de vida

---

## 🧪 Señal de Entrevista

> “No manejo hilos directamente; uso abstracciones.”

---

## 🧠 Regla Mental

**No gestiones hilos, gestiona tareas**
