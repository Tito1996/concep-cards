## 🧠 TARJETA DE ESTUDIO – TIPOS DE DATOS

---

### ¿Qué es un tipo de dato?

Un tipo de dato define **qué clase de información** puede almacenar una variable y **qué operaciones tienen sentido** sobre ella.

En otras palabras:
👉 el tipo le dice al programa **cómo tratar ese valor**.

---

### Tipos de datos más comunes

* **Numéricos:** enteros y decimales
* **Texto:** cadenas de caracteres
* **Booleanos:** verdadero / falso

Estos existen en casi todos los lenguajes.

---

### ¿Por qué son importantes?

* Previenen errores (ej: sumar texto con números)
* Ayudan al compilador/intérprete a validar el código
* Mejoran la legibilidad y el mantenimiento
* Permiten optimizar memoria y performance

---

### Tipos primitivos vs referencias (conceptual)

* **Primitivos:** guardan el valor directamente
* **Referencias:** apuntan a un objeto en memoria

👉 Copiar un primitivo copia el valor
👉 Copiar una referencia copia el “puntero”

Esto explica muchos bugs de junior.

---

### Tipado fuerte vs débil (idea general)

* **Fuerte:** no permite mezclar tipos sin conversión
* **Débil:** permite conversiones implícitas

Frase clave:

> “Cuanto más fuerte el tipado, más errores se detectan antes.”

---

### Errores comunes en entrevistas

* Usar texto cuando debería ser número
* No convertir tipos explícitamente
* Asumir que dos tipos compatibles son iguales
* Ignorar `null / undefined`

---

### Buena práctica

Elegir el tipo **más específico posible**, no el más cómodo.

---

### Frase que suma puntos

> “El tipo correcto es la primera validación del sistema.”

---
