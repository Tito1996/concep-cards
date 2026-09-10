## TARJETA DE ESTUDIO – synchronized vs Lock en Java**

---

## 📌 ¿Qué problema resuelven?

Ambos mecanismos permiten **controlar el acceso concurrente** a recursos compartidos para evitar inconsistencias.

---

## 🧱 synchronized

- Bloquea automáticamente al entrar/salir del bloque
- Manejo simple
- Menos flexible

```java
synchronized (this) {
    // sección crítica
}
````

✔ Fácil de usar
❌ No control fino del bloqueo

---

## 🧱 Lock (`ReentrantLock`)

* Bloqueo explícito
* Mayor control
* Requiere liberación manual

```java
lock.lock();
try {
    // sección crítica
} finally {
    lock.unlock();
}
```

✔ Más flexible
❌ Más propenso a errores si se usa mal

---

## 🎯 Buenas Prácticas (Nivel Mid)

* Usar `synchronized` por defecto
* Usar `Lock` solo si necesitas:

  * timeout
  * bloqueo no bloqueante
  * mayor control

---

## 🧠 Regla Mental

**Simple primero, flexible solo si es necesario**
