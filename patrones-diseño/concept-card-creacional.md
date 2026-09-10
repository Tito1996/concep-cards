
# 🧠 TARJETA DE ESTUDIO – PATRONES CREACIONALES

### ¿Qué son los patrones creacionales?

Los **patrones creacionales** se enfocan en **cómo se crean los objetos**, buscando:

* desacoplar la creación del uso
* ocultar la lógica de instanciación
* mejorar flexibilidad y mantenibilidad

En simple:
👉 *controlan cómo y cuándo nacen los objetos.*

---

### Problema que resuelven

Sin patrones creacionales:

* el código depende de `new`
* hay fuerte acoplamiento
* es difícil cambiar implementaciones

Con patrones:
👉 *el cliente no sabe cómo se crea el objeto.*

---

### Objetivo principal (entrevista 🚨)

> **Separar la creación del objeto de su uso.**

---

### Principales patrones creacionales

#### 🧱 Singleton

Garantiza que:

* exista **una única instancia**
* acceso global controlado

Uso típico:

* configuración
* logging

Riesgo:
👉 acoplamiento global y problemas en testing.

---

#### 🏭 Factory (Factory Method / Simple Factory)

Delegan la creación a una fábrica.

Permiten:

* decidir qué objeto crear
* ocultar la lógica de instanciación

Idea clave:
👉 *el cliente pide un objeto, no lo construye.*

---

#### 🧰 Abstract Factory

Permite crear:

* **familias de objetos relacionados**
* sin conocer sus clases concretas

Ejemplo mental:
👉 crear UI para distintos sistemas (tema claro / oscuro).

---

#### 🧑‍🍳 Builder

Separa:

* construcción compleja
* representación final

Útil cuando:

* muchos parámetros
* objetos inmutables

Idea:
👉 *construir paso a paso.*

---

#### 🧬 Prototype

Crea objetos:

* clonando una instancia existente

Útil cuando:

* crear desde cero es costoso

---

### Comparación rápida (entrevista)

* Factory: 👉 un objeto
* Abstract Factory: 👉 familias de objetos
* Builder: 👉 construcción compleja paso a paso
* Prototype: 👉 clonación
* Singleton: 👉 única instancia

---

### Cuándo usar patrones creacionales

* cuando la creación es compleja
* cuando hay múltiples implementaciones
* cuando se quiere reducir acoplamiento

---

### Regla importante 🚨

> **No instanciar directamente lo que puede variar.**

---

### Beneficios clave

* menor acoplamiento
* mayor flexibilidad
* código más limpio
* facilidad de cambio

---

### Errores comunes (entrevista 🚨)

* abusar de Singleton
* confundir Factory con Builder
* usar Abstract Factory sin necesidad
* sobreingeniería

---

### Regla de oro

> **La creación también es diseño.**

---

### Frase que suma muchos puntos (entrevista)

> “Los patrones creacionales desacoplan la creación de objetos de su uso para mejorar flexibilidad y mantenibilidad.”
