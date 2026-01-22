## TARJETA DE ESTUDIO – Modelos de Concurrencia en Java

---

## 📌 No toda concurrencia es igual

Java permite distintos **modelos mentales**, cada uno con trade-offs.

---

## 🧱 Modelos Principales

### 🧵 Shared State + Locks
- `synchronized`, `Lock`
- Riesgo alto
- Control explícito

---

### 🔁 Inmutabilidad + Mensajes
- Copias, eventos, colas
- Más seguro
- Más memoria

---

### ⚛️ Atomics / Lock-Free
- `AtomicInteger`, CAS
- Alto rendimiento
- Alta complejidad mental

---

## 🎯 Buenas Prácticas Senior

- Preferir modelos simples
- Evitar locks cuando sea posible
- No mezclar modelos sin entenderlos

---

## 🧠 Regla Mental

**Elige el modelo antes de escribir código**
