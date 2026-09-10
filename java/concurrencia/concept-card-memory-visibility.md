## TARJETA DE ESTUDIO – Memory Visibility y Happens-Before

---

## 📌 Problema Real

En concurrencia, **no basta con que el código sea correcto**:
otros hilos deben **ver los cambios**.

---

## 🧠 Concepto Clave: Happens-Before

Garantiza que:
- Un hilo vea los cambios de otro
- El orden de ejecución sea consistente

---

## 🧱 Mecanismos que crean Happens-Before

- `synchronized`
- `volatile`
- `Lock`
- `Thread.start()` / `join()`
- Clases concurrentes

---

## ⚠️ Error Común

- Asumir visibilidad sin sincronización
- Bugs que solo aparecen en producción

---

## 🎯 Buenas Prácticas Senior

- No confiar en el orden “aparente”
- Usar primitivas del lenguaje
- Diseñar visibilidad explícita

---

## 🧠 Regla Mental

**Si no hay happens-before, no hay garantías**
