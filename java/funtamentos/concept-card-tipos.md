## 🧠 TARJETA DE ESTUDIO – TIPOS PRIMITIVOS Y `String` (JAVA)

### Tipos primitivos en Java

Los tipos primitivos almacenan **valores simples directamente en memoria**.

Los más comunes:

* `int` → números enteros
* `double` → decimales
* `boolean` → verdadero / falso
* `char` → un carácter

Idea clave:
👉 **no son objetos** y no tienen métodos.

---

### ¿Qué es `String`?

`String` **NO es un tipo primitivo**.
Es una **clase**, es decir, un **objeto**.

Esto implica que:

* Tiene métodos (`length()`, `toLowerCase()`, etc.)
* Se maneja por **referencia**
* Es **inmutable**

---

### Diferencia clave (entrevista)

* **Primitivo:** guarda el valor
* **String:** guarda una referencia a un objeto

Por eso:
👉 los primitivos se comparan con `==`
👉 los `String` se comparan con `.equals()`

---

### Inmutabilidad de `String`

Un `String` **no cambia** una vez creado.

Si “modificas” un `String`:
👉 en realidad se crea **uno nuevo**.

Esto evita bugs, pero puede impactar performance si se usa mal.

---

### Conversiones comunes (muy preguntado)

* `int` → `String`
  → cuando necesitas mostrar o concatenar texto

* `String` → `int`
  → cuando lees datos de entrada (formularios, consola, requests)

Idea clave:
👉 **la conversión no es automática**, debe ser explícita.

---

### Errores comunes de junior

* Comparar `String` con `==`
* Pensar que `String` es primitivo
* No entender por qué un `String` “no cambia”
* Olvidar convertir tipos antes de operar

---

### Buena práctica

* Usar primitivos para datos simples
* Usar `String` para texto
* Convertir tipos de forma explícita y consciente

---

### Frase que suma puntos

> “`String` es un objeto inmutable; por eso se compara con `.equals()` y no con `==`.”

---
