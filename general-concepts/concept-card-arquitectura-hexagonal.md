# 🧠 TARJETA DE ESTUDIO – ARQUITECTURA HEXAGONAL

### ¿Qué es la arquitectura hexagonal?

La **arquitectura hexagonal** (también llamada **Ports & Adapters**) es un estilo arquitectónico que busca:

* desacoplar la **lógica de negocio**
* aislar la aplicación de detalles externos
* facilitar mantenimiento, testing y cambios tecnológicos

En simple:
👉 *el negocio no depende de frameworks, bases de datos ni interfaces.*

---

### Problema que resuelve

En arquitecturas tradicionales:

* la lógica queda atada a frameworks
* cambiar una base de datos o interfaz es costoso
* los tests son complejos

Arquitectura hexagonal propone:
👉 *poner el negocio en el centro y todo lo demás alrededor.*

---

### Idea central (muy preguntada 🚨)

> **El dominio no conoce el mundo exterior.**

El núcleo:

* no sabe si hay una API REST, una BD o una UI
* solo conoce **interfaces (puertos)**

---

### Componentes principales

#### 🧠 Núcleo (Dominio / Aplicación)

Contiene:

* reglas de negocio
* casos de uso
* entidades y lógica principal

Características:

* independiente de frameworks
* testeable sin infraestructura

---

#### 🔌 Puertos (Ports)

Son **interfaces** que define el núcleo para comunicarse con el exterior.

Tipos comunes:

* puertos de entrada (casos de uso)
* puertos de salida (persistencia, servicios externos)

👉 el núcleo **define qué necesita**, no cómo se implementa.

---

#### 🔄 Adaptadores (Adapters)

Implementan los puertos.

Ejemplos:

* controlador HTTP
* repositorio de base de datos
* cliente de API externa

👉 conectan el mundo externo con el núcleo.

---

### Flujo típico

1. Una interfaz externa recibe la solicitud (UI / API / CLI)
2. Un adaptador de entrada llama a un puerto
3. El núcleo ejecuta la lógica de negocio
4. Si necesita algo externo, usa un puerto de salida
5. Un adaptador de salida ejecuta la acción concreta

---

### Regla de dependencias (clave 🚨)

> **Las dependencias siempre apuntan hacia el núcleo.**

* adaptadores dependen del núcleo
* el núcleo no depende de adaptadores

---

### Beneficios principales

* alto desacoplamiento
* facilidad para testear
* cambios tecnológicos sin romper el negocio
* mayor claridad del dominio

---

### Ejemplo mental simple

👉 cambiar la base de datos **no afecta** al negocio
👉 cambiar la API **no afecta** al negocio

Solo se reemplaza el adaptador.

---

### Diferencia con capas tradicionales

Arquitectura en capas:

* dependencias hacia abajo
* negocio depende de infraestructura

Hexagonal:

* dependencias hacia adentro
* negocio aislado

---

### Errores comunes (entrevista 🚨)

* confundir hexagonal con MVC
* meter lógica de negocio en controladores
* que el dominio dependa de frameworks
* no usar interfaces como puertos

---

### Regla de oro

> **El negocio manda; la tecnología se adapta.**

---

### Frase que suma muchos puntos (entrevista)

> “En arquitectura hexagonal el dominio es independiente y se comunica con el exterior mediante puertos y adaptadores.”
