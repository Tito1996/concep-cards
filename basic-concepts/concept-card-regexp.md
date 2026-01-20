**TARJETA DE ESTUDIO – Expresiones Regulares (RegExp)**
**Formato:** A6

---

## 📌 ¿Qué es una Expresión Regular?

Una **expresión regular (RegExp)** es un **patrón de texto** utilizado para **buscar, validar, extraer o reemplazar cadenas**.

Se usa ampliamente en:

* Validaciones
* Procesamiento de texto
* Formularios
* Logs y parsing

---

## 🧱 Elementos Básicos

### 🔤 Caracteres

* `a` → coincide con “a”
* `.` → cualquier carácter
* `\d` → dígito (0–9)
* `\w` → letra, número o `_`
* `\s` → espacio en blanco

---

### 📐 Cuantificadores

* `*` → 0 o más
* `+` → 1 o más
* `?` → 0 o 1
* `{n}` → exactamente n
* `{n,m}` → entre n y m

---

### 🎯 Anclas

* `^` → inicio de la cadena
* `$` → fin de la cadena

✔ Evitan coincidencias parciales

---

### 🧩 Grupos y Alternativas

* `(abc)` → grupo
* `|` → OR lógico
* `(?: )` → grupo no capturante

---

### 🔍 Clases de Caracteres

* `[abc]` → a, b o c
* `[a-z]` → rango
* `[^0-9]` → negación

---

## 🧪 Ejemplos Comunes

### 📧 Email

```regex
^[^\s@]+@[^\s@]+\.[^\s@]+$
```

---

### 🔢 Solo números

```regex
^[0-9]+$
```

---

### 🔐 Password fuerte

```regex
^(?=.*[A-Z])(?=.*\d).{8,}$
```

---

## ⚠️ Errores Comunes

* No escapar caracteres especiales
* RegExp demasiado complejas
* Validaciones muy restrictivas
* Falta de anclas (`^`, `$`)

---

## 🎯 Buenas Prácticas

* Mantener expresiones simples
* Comentar o documentar patrones complejos
* Probar con herramientas online
* Validar siempre también en backend

---

## 📝 Nota para Full Stack

* RegExp mejora la calidad de datos
* Primera capa de validación
* Complemento, no reemplazo, del backend

---

**Tip:**
Si una RegExp no se puede leer en 10 segundos, necesita simplificarse.
