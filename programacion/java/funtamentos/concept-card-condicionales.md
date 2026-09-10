## 🧠 TARJETA DE ESTUDIO – CONDICIONALES EN JAVA (`if`, `switch`) (A6)

### ¿Qué son los condicionales?

Permiten que el programa **tome decisiones** según si una condición es verdadera o falsa.

En simple:
👉 *“Si se cumple esto, ejecutá esto otro.”*

---

### `if` / `else`

Se usa cuando:

* La decisión depende de **condiciones lógicas**
* Hay comparaciones (`>`, `<`, `==`, `.equals()`)

La condición:
👉 **SIEMPRE debe ser booleana** (`true` o `false`).

---

### Condiciones bien escritas (entrevista)

Una buena condición:

* Tiene sentido lógico
* Es fácil de leer
* No mezcla conceptos incompatibles

Ejemplo conceptual:
👉 comparar estados, permisos o valores relacionados.

---

### Error crítico en Java 🚨

❌ **Nunca comparar `String` con `==`**

`==` compara **referencias en memoria**, no el contenido.

✅ Usar siempre:
👉 `.equals()` para comparar texto.

Este error **descarta candidatos**.

---

### `switch`

Se usa cuando:

* Comparas **un solo valor**
* Contra **opciones discretas y conocidas**
* Buscas código más claro que muchos `if`

Ejemplos típicos:

* Estados
* Tipos
* Roles
* Códigos

---

### Cuándo NO usar `switch`

* Condiciones complejas
* Comparaciones con rangos
* Lógica con múltiples variables

Ahí:
👉 `if` es más claro.

---

### Errores comunes en entrevistas

* Comparar `String` con `==`
* Condiciones que siempre dan true/false
* Usar `if` en cadena cuando un `switch` es más claro
* `switch` para lógica compleja

---

### Buena práctica

* Preferir condiciones claras
* Usar `switch` solo para valores discretos
* Usar `return` temprano para evitar `else` profundos

---

### Frase que suma puntos

> “En Java, los `String` se comparan con `.equals()`, no con `==`.”

---
