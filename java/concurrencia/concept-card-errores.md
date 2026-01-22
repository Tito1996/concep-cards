## TARJETA DE ESTUDIO – Errores Clásicos de Concurrencia (Entrevistas)

---

## 📌 ¿Por qué se preguntan?

Porque la concurrencia falla **en producción**, no en tests simples.

---

## ❌ Errores Más Comunes

- Acceder a variables compartidas sin sincronización
- Usar `sleep` para sincronizar
- Olvidar liberar locks
- Asumir orden de ejecución
- Modificar colecciones no thread-safe

---

## ⚠️ Casos Típicos

- `HashMap` compartido entre hilos
- Contadores sin sincronizar
- Deadlocks por múltiples locks

---

## 🎯 Buenas Prácticas (Nivel Mid)

- Pensar en escenarios negativos
- Preferir estructuras thread-safe
- Minimizar estado compartido
- Diseñar antes de paralelizar

---

## 🧪 Frase Clave de Entrevista

> “El problema no es que falle, es que falla de forma impredecible.”

---

## 🧠 Regla Mental

**Si es difícil de explicar, es peligroso**
