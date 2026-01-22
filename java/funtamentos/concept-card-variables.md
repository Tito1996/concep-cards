## 🧠 TARJETA DE ESTUDIO – VARIABLES Y ALCANCE (JAVA)

### ¿Qué es una variable?

Una variable es un **nombre que referencia un valor en memoria**.
Se usa para **guardar y reutilizar información** durante la ejecución del programa.

---

### Declarar e inicializar

* **Declarar**: definir tipo y nombre
* **Inicializar**: asignar un valor

Idea clave:
👉 en Java, **el tipo es obligatorio**.

---

### Tipos de variables según su alcance

#### 1️⃣ Variables locales

* Declaradas dentro de un método o bloque (`if`, `for`)
* **Solo existen dentro de ese bloque**
* No tienen valor por defecto

Son las **más seguras y recomendadas**.

---

#### 2️⃣ Variables de clase (atributos)

* Declaradas dentro de la clase, fuera de los métodos
* Pertenecen a una instancia del objeto
* Tienen valores por defecto

Se usan para **estado del objeto**, no para lógica temporal.

---

### Regla fundamental de alcance

> Una variable **solo vive dentro del bloque donde fue creada**.

Si sales del bloque:
👉 la variable deja de existir.

---

### Diferencia clave (entrevista)

* **Local** → temporal, segura, controlada
* **De clase** → estado compartido entre métodos

Usar una variable de clase cuando puede ser local:
🚨 mala señal en entrevistas.

---

### Errores comunes de junior

* Usar variables fuera de su scope
* Reutilizar nombres en distintos niveles
* Abusar de variables de clase
* Confiar en valores por defecto sin saberlo

---

### Buena práctica

* Declarar variables **lo más cerca posible de su uso**
* Mantener el **alcance más pequeño posible**
* Usar variables de clase solo cuando representan estado real

---

### Frase que suma puntos

> “Cuanto menor es el alcance de una variable, menor es el riesgo de errores.”

---
