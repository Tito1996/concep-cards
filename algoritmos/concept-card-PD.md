# **Programación Dinámica**

---

## ¿Qué es?

La **Programación Dinámica (PD)** es una técnica de diseño de algoritmos que **resuelve problemas complejos dividiéndolos en subproblemas** y **almacenando sus resultados** para evitar cálculos repetidos.

---

## Idea Clave

> Resolver una vez, **reutilizar muchas veces**.

---

## Cuándo Aplicarla

Un problema es apto para PD si cumple:

* **Subproblemas superpuestos**.
* **Estructura óptima** (la solución óptima se construye a partir de subsoluciones óptimas).

---

## Enfoques Principales

### Top‑Down (Memoización)

* Recursivo.
* Guarda resultados ya calculados.

### Bottom‑Up (Tabulación)

* Iterativo.
* Construye soluciones desde los casos base.

---

## Ejemplo Clásico: Fibonacci

### Sin PD

* Recalcula valores.
* Complejidad: **O(2ⁿ)**

### Con PD

* Guarda resultados.
* Complejidad: **O(n)**

---

## Ejemplo Conceptual

```text
f(n) = f(n-1) + f(n-2)
```

Se calcula cada valor **una sola vez**.

---

## Problemas Típicos

* Fibonacci
* Mochila (Knapsack)
* Cambio de monedas
* Longest Common Subsequence (LCS)
* Longest Increasing Subsequence (LIS)

---

## Complejidad

* **Tiempo**: normalmente O(n) o O(n·m)
* **Espacio**: depende de la tabla usada

---

## Ventajas

* Gran mejora de rendimiento.
* Soluciones óptimas garantizadas.

---

## Desventajas

* Mayor uso de memoria.
* Diseño más complejo.

---

## Comparación Rápida

* **Fuerza bruta**: lento, repetitivo.
* **Greedy**: rápido, no siempre óptimo.
* **Programación Dinámica**: óptima y eficiente.

---

## Idea Clave Final

> La programación dinámica transforma problemas **exponenciales en polinómicos**.
