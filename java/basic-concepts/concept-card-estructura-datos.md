## TARJETA DE ESTUDIO – Estructuras de Datos Básicas en Java**

---

## 📌 ¿Por qué importan las Estructuras de Datos?

No basta con saber usarlas. Un perfil mid entiende **cuándo elegir cada una** según:
- Tipo de acceso
- Frecuencia de búsquedas
- Lecturas vs escrituras

---

## 🧱 Estructuras Comunes en Java

### 📋 List (`ArrayList`)
- Mantiene orden
- Permite duplicados
- Acceso por índice

✔ Ideal para recorrer  
❌ Búsquedas lentas por contenido

---

### 🗂️ Set (`HashSet`)
- No permite duplicados
- No garantiza orden

✔ Validar unicidad  
❌ No acceso por índice

---

### 🧾 Map (`HashMap`)
- Pares clave → valor
- Acceso rápido por clave

✔ Búsquedas eficientes  
❌ No mantiene orden (por defecto)

---

## ⚠️ Errores Comunes

- Usar `List` cuando se necesita búsqueda por clave
- Usar `Map` cuando solo se recorre
- Ignorar costos de inserción o búsqueda

---

## 🎯 Buenas Prácticas (Nivel Mid)

- Elegir estructura según el **caso de uso**
- Pensar en acceso, no solo en almacenamiento
- Preferir interfaces (`List`, `Map`) sobre implementaciones

---

## 🧪 Señal de Entrevista

> “Uso esta estructura porque optimiza este caso específico.”

---

## 🧠 Regla Mental

**La estructura correcta simplifica el código**
