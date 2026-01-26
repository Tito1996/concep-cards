# 🧠 TARJETA DE ESTUDIO – PATRONES ESTRUCTURALES

### ¿Qué son los patrones estructurales?

Los **patrones estructurales** se enfocan en **cómo se organizan y relacionan las clases y objetos**, buscando:

* componer estructuras flexibles
* reducir acoplamiento
* facilitar cambios sin romper el sistema

En simple:
👉 *definen cómo se conectan las piezas.*

---

### Problema que resuelven

Sin estos patrones:

* estructuras rígidas
* dependencias fuertes
* cambios costosos

Con patrones estructurales:
👉 *la estructura se adapta sin modificar el núcleo.*

---

### Objetivo principal (entrevista 🚨)

> **Componer objetos de forma flexible y desacoplada.**

---

### Principales patrones estructurales

#### 🔌 Adapter

Permite:

* que interfaces incompatibles trabajen juntas

Idea clave:
👉 *adaptar, no reescribir.*

Ejemplo mental:
👉 un enchufe convertido a otro formato.

---

#### 🎁 Decorator

Permite:

* agregar responsabilidades **dinámicamente**
* sin modificar la clase original

Idea:
👉 *envolver para extender.*

---

#### 🏛️ Facade

Proporciona:

* una interfaz simple
* sobre un sistema complejo

Idea:
👉 *ocultar complejidad.*

---

#### 🌳 Composite

Permite:

* tratar objetos individuales y compuestos de la misma forma

Útil para:

* estructuras jerárquicas

Idea:
👉 *parte y todo se usan igual.*

---

#### 🪞 Proxy

Controla el acceso a un objeto.

Usos comunes:

* seguridad
* lazy loading
* control remoto

Idea:
👉 *intermediario con control.*

---

#### 🧩 Bridge

Separa:

* abstracción
* implementación

Permite:
👉 que ambas evolucionen independientemente.

---

### Comparación rápida (entrevista)

* Adapter: 👉 compatibilidad
* Decorator: 👉 extensión dinámica
* Facade: 👉 simplificación
* Composite: 👉 jerarquía
* Proxy: 👉 control de acceso
* Bridge: 👉 desacoplar abstracción e implementación

---

### Beneficios clave

* menor acoplamiento
* mayor flexibilidad
* estructuras más limpias
* facilidad de mantenimiento

---

### Errores comunes (entrevista 🚨)

* confundir Adapter con Facade
* usar Decorator cuando basta herencia simple
* sobrecomponer sin necesidad
* complicar estructuras simples

---

### Regla importante

> **Composición sobre herencia.**

---

### Regla de oro

> **Estructura flexible hoy, cambios simples mañana.**

---

### Frase que suma muchos puntos (entrevista)

> “Los patrones estructurales permiten organizar y componer objetos de forma flexible, reduciendo el acoplamiento.”
