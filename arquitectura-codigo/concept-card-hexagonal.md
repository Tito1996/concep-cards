# **Arquitectura Hexagonal (Ports & Adapters)**

---

## ¿Qué es?

La **arquitectura hexagonal**, también llamada **Ports & Adapters**, organiza el sistema colocando el **dominio en el centro** y aislándolo de detalles externos como bases de datos, frameworks o interfaces de usuario.

---

## Objetivo Principal

* Proteger la lógica de negocio.
* Reducir el acoplamiento con tecnologías externas.
* Facilitar pruebas y mantenimiento.

---

## Idea Clave

> El dominio **no conoce** nada del exterior; el exterior se adapta al dominio.

---

## Componentes

### Dominio

* Entidades y reglas de negocio.
* Casos de uso.
* Independiente de frameworks.

### Puertos (Ports)

* Interfaces que definen cómo se comunica el dominio.
* Entrada (casos de uso) y salida (repositorios, servicios externos).

### Adaptadores (Adapters)

* Implementaciones concretas de los puertos.
* Conectan el dominio con bases de datos, APIs, UI, etc.

---

## Flujo de Funcionamiento

1. Un adaptador de entrada recibe la solicitud.
2. Se invoca un puerto del dominio.
3. El dominio ejecuta la lógica.
4. Adaptadores de salida interactúan con sistemas externos.

---

## Ventajas

* Alto desacoplamiento.
* Dominio altamente testeable.
* Fácil cambio de tecnologías.

---

## Desventajas

* Mayor complejidad inicial.
* Curva de aprendizaje.
* Más código estructural.

---

## Cuándo Usarla

* Sistemas con lógica de negocio compleja.
* Proyectos a largo plazo.
* Aplicaciones orientadas a dominio.

---

## Comparación Rápida

* **Hexagonal**: dominio al centro.
* **Capas**: dependencias jerárquicas.
* **Clean Architecture**: reglas similares, más estrictas.

---

## Idea Clave Final

> Las tecnologías cambian; **el dominio debe permanecer estable**.
