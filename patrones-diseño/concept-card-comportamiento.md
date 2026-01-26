# 🧠 TARJETA DE ESTUDIO – PATRONES DE COMPORTAMIENTO

### ¿Qué son los patrones de comportamiento?

Los **patrones de comportamiento** se enfocan en **cómo interactúan los objetos y cómo se distribuyen las responsabilidades**, buscando:

* reducir dependencias directas
* definir flujos claros
* encapsular comportamientos variables

En simple:
👉 *organizan cómo se comunican y actúan los objetos.*

---

### Problema que resuelven

Sin estos patrones:

* lógica dispersa
* muchos `if / else`
* objetos demasiado acoplados

Con patrones:
👉 *cada objeto sabe qué hacer y cuándo.*

---

### Objetivo principal (entrevista 🚨)

> **Definir interacciones claras y flexibles entre objetos.**

---

### Principales patrones de comportamiento

#### 🔄 Strategy

Permite:

* intercambiar algoritmos en tiempo de ejecución

Idea clave:
👉 *variar el comportamiento sin condicionales.*

---

#### 👀 Observer

Define:

* una relación uno-a-muchos

Permite:

* notificar cambios automáticamente

Idea:
👉 *cuando uno cambia, los demás se enteran.*

---

#### 🧾 Command

Encapsula una acción como objeto.

Permite:

* deshacer/rehacer
* colas de comandos

Idea:
👉 *una acción convertida en objeto.*

---

#### 🚦 State

Permite:

* cambiar el comportamiento según el estado interno

Idea:
👉 *el estado define el comportamiento.*

---

#### 🧭 Template Method

Define:

* el esqueleto de un algoritmo
* delega pasos a subclases

Idea:
👉 *estructura fija, pasos variables.*

---

#### 🔗 Chain of Responsibility

Permite:

* pasar una petición por una cadena de manejadores

Idea:
👉 *el primero que puede, la maneja.*

---

### Comparación rápida (entrevista)

* Strategy: 👉 cambiar algoritmo
* Observer: 👉 notificación
* Command: 👉 encapsular acciones
* State: 👉 comportamiento por estado
* Template: 👉 estructura fija
* Chain: 👉 cadena de manejo

---

### Beneficios clave

* menor acoplamiento
* mayor claridad de responsabilidades
* código más extensible
* eliminación de lógica condicional compleja

---

### Errores comunes (entrevista 🚨)

* confundir Strategy con State
* usar Observer sin control (efecto cascada)
* sobreingeniería
* no identificar el comportamiento variable

---

### Regla importante

> **Encapsular lo que cambia.**

---

### Regla de oro

> **Los objetos colaboran, no se controlan entre sí.**

---

### Frase que suma muchos puntos (entrevista)

> “Los patrones de comportamiento definen cómo se comunican los objetos y cómo se distribuyen las responsabilidades de forma flexible.”
