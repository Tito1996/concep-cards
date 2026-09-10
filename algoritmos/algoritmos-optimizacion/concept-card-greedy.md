# **Algoritmos Greedy (Voraces)**

---

## ¿Qué son?

Los **algoritmos Greedy** (o voraces) construyen una solución **paso a paso**, eligiendo en cada paso la **mejor opción local** con la esperanza de alcanzar una solución óptima global.

---

## Idea Clave

> Tomar la **mejor decisión inmediata** sin reconsiderar decisiones previas.

---

## Características Principales

* Decisiones **locales**.
* No hay retroceso (*backtracking*).
* Implementación simple y rápida.

---

## Cuándo Funcionan Correctamente

Un problema debe cumplir:

* **Propiedad de elección voraz** (la elección local conduce a la solución óptima).
* **Subestructura óptima**.

---

## Ejemplos Clásicos

* **Selección de actividades**
* **Cambio de monedas** (sistemas canónicos)
* **Kruskal y Prim** (árbol generador mínimo)
* **Dijkstra** (sin pesos negativos)

---

## Ejemplo Conceptual

Seleccionar actividades que no se solapen:

1. Elegir la que termina antes.
2. Eliminar las incompatibles.
3. Repetir.

---

## Complejidad

* Generalmente **O(n)** o **O(n log n)**.
* Muy eficientes en tiempo.

---

## Ventajas

* Simples de implementar.
* Muy rápidos.
* Bajo consumo de memoria.

---

## Desventajas

* No siempre producen solución óptima.
* Dependen fuertemente del problema.

---

## Comparación Rápida

| Enfoque               | Resultado                 |
| --------------------- | ------------------------- |
| Greedy                | Rápido, no siempre óptimo |
| Programación Dinámica | Óptimo, más costoso       |
| Backtracking          | Exhaustivo, lento         |

---

## Cuándo Usarlos

* Problemas grandes.
* Cuando se necesita rapidez.
* Cuando se demuestra corrección voraz.

---

## Idea Clave Final

> Los algoritmos Greedy son rápidos y simples, pero **solo funcionan bien en problemas adecuados**.
