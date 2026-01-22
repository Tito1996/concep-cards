## TARJETA DE ESTUDIO – Concurrencia en Java**

---

## 📌 ¿Qué es la Concurrencia?

La **concurrencia** es la capacidad de un programa para **ejecutar múltiples tareas al mismo tiempo** o de forma intercalada, compartiendo recursos.

En Java se utiliza para:
- Mejorar rendimiento
- Aprovechar múltiples núcleos
- Manejar tareas paralelas o asíncronas

---

## 🧱 Conceptos Clave

### 🧵 Hilos (Threads)
- Unidad básica de ejecución
- Varios hilos pueden correr en paralelo

```java
Thread t = new Thread(() -> doWork());
t.start();
````

---

### 🔒 Recursos Compartidos

* Variables u objetos usados por varios hilos
* Fuente principal de bugs en concurrencia

---

### ⚠️ Problemas Comunes

* **Race conditions**: resultados impredecibles
* **Deadlocks**: hilos bloqueados entre sí
* **Inconsistencia de datos**
* Bugs difíciles de reproducir

---

## 🛠️ Herramientas Básicas en Java

* `synchronized`
* `volatile`
* `ExecutorService`
* Clases thread-safe (`ConcurrentHashMap`)

---

## 🎯 Buenas Prácticas (Nivel Mid)

* Preferir **inmutabilidad**
* Minimizar estado compartido
* Usar abstracciones de alto nivel (`Executors`)
* Evitar manejo manual de hilos si no es necesario

---

## 🧪 Señal de Entrevista

> “¿Qué pasa si dos hilos acceden a esto al mismo tiempo?”

---

## 🧠 Regla Mental

**Concurrencia no es velocidad, es coordinación**
