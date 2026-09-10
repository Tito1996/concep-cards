# 🧠 TARJETA DE ESTUDIO – PATRONES DE DISEÑO

### ¿Qué son los patrones de diseño?

Los **patrones de diseño** son **soluciones probadas y reutilizables** a problemas comunes de diseño de software.

No son:

* código listo para copiar
* librerías

Sí son:

* **guías de diseño**
* buenas prácticas estandarizadas

En simple:
👉 *formas conocidas de resolver problemas recurrentes.*

---

### ¿Por qué usar patrones?

Permiten:

* escribir código más mantenible
* reducir acoplamiento
* mejorar la comunicación entre desarrolladores
* evitar reinventar soluciones

Idea clave:
👉 *un patrón es un lenguaje común entre programadores.*

---

### Clasificación clásica (GoF 🚨)

#### 🏗️ Patrones Creacionales

Se enfocan en:

* **cómo se crean los objetos**
* ocultar la lógica de instanciación

Ejemplos:

* Singleton
* Factory
* Builder

👉 controlan el **proceso de creación**.

---

#### 🧩 Patrones Estructurales

Se enfocan en:

* **cómo se relacionan y componen los objetos**

Ejemplos:

* Adapter
* Decorator
* Facade
* Composite

👉 organizan la **estructura del sistema**.

---

#### 🔄 Patrones de Comportamiento

Se enfocan en:

* **cómo interactúan los objetos**
* cómo se distribuye la responsabilidad

Ejemplos:

* Strategy
* Observer
* Command
* State

👉 definen **comportamientos y flujos**.

---

### Ejemplo mental rápido

* Factory: 👉 *delegar la creación*
* Adapter: 👉 *hacer compatibles cosas incompatibles*
* Strategy: 👉 *variar el comportamiento sin if/else*
* Observer: 👉 *notificar cambios*

---

### Cuándo usar patrones

Usar patrones cuando:

* el problema es recurrente
* el diseño empieza a ser complejo
* necesitas flexibilidad futura

No usarlos cuando:

* el problema es simple
* agregan complejidad innecesaria

---

### Regla importante 🚨

> **No forzar patrones.**

Un patrón mal usado:

* complica el código
* reduce claridad

---

### Beneficios clave

* soluciones probadas
* código más limpio
* mejor extensibilidad
* menor dependencia entre componentes

---

### Errores comunes (entrevista 🚨)

* creer que un patrón es una regla
* usar patrones por moda
* no entender el problema que resuelven
* confundir patrón con arquitectura

---

### Diferencia clave

> **Arquitectura ≠ Patrón**

* arquitectura: estructura general del sistema
* patrón: solución puntual a un problema de diseño

---

### Regla de oro

> **Primero el problema, luego el patrón.**

---

### Frase que suma muchos puntos (entrevista)

> “Los patrones de diseño son soluciones reutilizables a problemas comunes de diseño, no implementaciones específicas.”
