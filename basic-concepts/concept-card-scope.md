## 🧠 TARJETA DE ESTUDIO – ALCANCE (SCOPE) DE VARIABLES

### ¿Qué es el alcance (scope)?

El alcance define **dónde existe una variable** y **desde qué partes del código se puede usar**.

En simple:
👉 *una variable solo vive dentro del lugar donde fue declarada.*

---

### Tipos de alcance más comunes

#### 1️⃣ Scope local

* Variables declaradas dentro de un método, función o bloque (`if`, `for`)
* Solo se pueden usar **dentro de ese bloque**

Es el scope **más seguro y recomendado**.

---

#### 2️⃣ Scope de clase / instancia

* Variables declaradas a nivel de clase
* Existen mientras el objeto existe
* Comparten estado entre métodos

Útiles, pero deben usarse con cuidado.

---

#### 3️⃣ Scope global (conceptual)

* Variables accesibles desde cualquier lugar
* Aumentan el riesgo de bugs
* Dificultan testing y mantenimiento

👉 **Evitar siempre que sea posible.**

---

### Idea clave de entrevista

> Cuanto más pequeño el scope, **menos errores**.

Reducir el alcance:

* Mejora legibilidad
* Reduce efectos colaterales
* Hace el código más predecible

---

### Errores comunes

* Usar variables fuera de su scope
* Reutilizar variables con el mismo nombre en distintos niveles
* Variables de clase cuando podrían ser locales
* Variables globales “por comodidad”

---

### Buena práctica

Declarar las variables:

* **Lo más cerca posible de donde se usan**
* Con el **menor alcance posible**

---

### Relación con bugs reales

Muchos bugs difíciles vienen de:
👉 **estado compartido mal controlado**

El scope es la primera defensa contra eso.

---

### Frase que suma puntos

> “Un scope reducido hace el código más seguro y fácil de mantener.”

---
