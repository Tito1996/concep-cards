## TARJETA DE ESTUDIO – Inmutabilidad y Concurrencia**

---

## 📌 Relación Clave

Los objetos **inmutables** son **thread-safe por diseño**.

No requieren sincronización porque:
- Su estado no cambia
- No hay condiciones de carrera

---

## 🧱 Ejemplos Inmutables

- `String`
- `Integer`
- `LocalDate`
- Clases propias sin setters

---

## ⚠️ Problemas con Objetos Mutables

- Estado compartido
- Cambios inesperados
- Bugs difíciles de reproducir

---

## 🎯 Buenas Prácticas (Nivel Mid)

- Diseñar objetos inmutables por defecto
- Usar `final` en campos
- Copiar datos en lugar de compartir referencias
- Reducir estado compartido al mínimo

---

## 🧪 Señal de Entrevista

> “¿Este objeto necesita ser mutable en un entorno concurrente?”

---

## 🧠 Regla Mental

**Inmutabilidad = concurrencia segura**
