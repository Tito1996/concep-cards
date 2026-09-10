## 🧠 TARJETA DE ESTUDIO – ABSTRACCIÓN BÁSICA (A6)

### ¿Qué es la abstracción?

La abstracción consiste en **ocultar los detalles innecesarios** y mostrar solo **lo que importa para usar algo**.

En simple:
👉 *usar algo sin necesitar saber cómo funciona por dentro.*

---

### ¿Para qué sirve?

* Reducir complejidad
* Facilitar el uso del código
* Mejorar mantenibilidad
* Evitar acoplamiento innecesario

La abstracción permite pensar en **qué hace algo**, no en **cómo lo hace**.

---

### Ejemplo mental (sin código)

Cuando usas un servicio:

* Sabes qué recibe
* Sabes qué devuelve
* **No te importa** cómo obtiene el resultado

Eso es abstracción.

---

### Abstracción en programación

Se aplica mediante:

* Funciones con responsabilidades claras
* Interfaces
* Clases que exponen solo lo necesario
* Capas (controller, service, repository)

---

### Idea clave de entrevista

> Una buena abstracción simplifica el uso y oculta complejidad.

Si para usar algo necesitas entender su implementación:
👉 la abstracción está fallando.

---

### Señales de mala abstracción

* Exponer demasiados detalles internos
* Métodos con muchos parámetros innecesarios
* Dependencias fuertes entre partes del sistema
* Cambios internos rompen código externo

---

### Buena práctica

* Pensar primero en el **uso**, luego en la implementación
* Nombrar abstracciones según **qué hacen**, no **cómo**
* Mantener interfaces pequeñas y claras

---

### Error común de junior

Confundir abstracción con:

* “hacer genérico”
* “agregar capas sin sentido”

Más capas ≠ mejor abstracción.

---

### Frase que suma puntos

> “La abstracción correcta reduce el impacto de los cambios.”

---
