## TARJETA DE ESTUDIO – Pensamiento de Diseño

---

## 📌 Enfoque Senior

Un perfil senior **no piensa primero en hilos**, piensa en:

- Dominio del problema
- Estado compartido
- Garantías de consistencia
- Coste real del paralelismo

---

## 🧠 Preguntas Clave Antes de Paralelizar

- ¿Realmente necesito concurrencia?
- ¿Dónde está el estado mutable?
- ¿Qué nivel de consistencia es aceptable?
- ¿Qué pasa si una tarea falla?

---

## ⚠️ Errores de Nivel Medio

- Paralelizar por defecto
- Compartir estado innecesariamente
- Optimizar antes de medir
- Pensar que más hilos = más rendimiento

---

## 🎯 Buenas Prácticas Senior

- Diseñar primero sin concurrencia
- Introducir concurrencia de forma incremental
- Medir antes y después
- Documentar invariantes de concurrencia

---

## 🧠 Regla Mental

**La concurrencia es una decisión de arquitectura**
