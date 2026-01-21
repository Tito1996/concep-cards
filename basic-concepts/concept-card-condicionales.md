## 🧠 TARJETA DE ESTUDIO – CONDICIONALES (A6)

### ¿Qué son los condicionales?

Los condicionales permiten que el programa **tome decisiones** según si una condición es verdadera o falsa.

En simple:
👉 *“Si pasa esto, hacé esto otro.”*

---

### Estructuras más comunes

* `if`
* `if / else`
* `if / else if / else`
* `switch` (para valores discretos)

Todas se basan en **expresiones booleanas**.

---

### ¿Qué es una condición?

Es una expresión que **siempre evalúa a `true` o `false`**.

Ejemplos conceptuales:

* Comparaciones (`edad > 18`)
* Estados (`usuarioActivo`)
* Combinaciones lógicas (`tienePermiso && noEstaBloqueado`)

---

### Uso correcto de `if`

Buenas prácticas:

* Condiciones claras y legibles
* Una decisión por `if`
* Evitar lógica compleja dentro de la condición

Si la condición necesita explicación:
👉 probablemente está mal escrita.

---

### `switch`: cuándo usarlo

Usar `switch` cuando:

* Comparas **un solo valor**
* Contra **opciones conocidas**
* Quieres código más limpio que muchos `if`

No usarlo para lógica compleja.

---

### Errores comunes en entrevistas

* Condiciones siempre verdaderas o siempre falsas
* Comparar cosas incorrectas (ej: strings mal comparados)
* `if` anidados innecesariamente
* No cubrir todos los casos posibles

---

### Buena práctica clave

Preferir **return temprano** para evitar `else` profundos y mejorar legibilidad.

---

### Frase que suma puntos

> “Una buena condición se entiende sin comentarios.”

---
