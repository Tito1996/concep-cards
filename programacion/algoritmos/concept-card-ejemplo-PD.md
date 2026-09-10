# **Programación Dinámica — Ejemplo Paso a Paso**

---

## Problema Clásico: Fibonacci

### Definición

La sucesión de Fibonacci se define como:

* f(0) = 0
* f(1) = 1
* f(n) = f(n−1) + f(n−2)

---

## Enfoque 1: Recursión Simple (❌ Ineficiente)

```text
f(5) = f(4) + f(3)
f(4) = f(3) + f(2)
f(3) = f(2) + f(1)
```

### Problema

* Se recalculan los mismos valores muchas veces.
* Complejidad: **O(2ⁿ)**

---

## Enfoque 2: Programación Dinámica

### Idea Clave

> Cada resultado se calcula **una sola vez** y se guarda.

---

## Método Bottom‑Up (Tabulación)

### Paso 1: Casos base

| n | f(n) |
| - | ---- |
| 0 | 0    |
| 1 | 1    |

---

### Paso 2: Construcción de la tabla

| n | Cálculo | Resultado |
| - | ------- | --------- |
| 2 | 1 + 0   | 1         |
| 3 | 1 + 1   | 2         |
| 4 | 2 + 1   | 3         |
| 5 | 3 + 2   | 5         |

---

### Paso 3: Resultado Final

➡ **f(5) = 5**

---

## Complejidad

* **Tiempo**: O(n)
* **Espacio**: O(n)

---

## Qué Aprendemos

* Se eliminan cálculos repetidos.
* El algoritmo es mucho más eficiente.

---

## Dónde se Aplica la Misma Idea

* Mochila (Knapsack)
* Cambio de monedas
* Caminos mínimos en DAG
* Subcadenas comunes

---

## Comparación Rápida

| Enfoque               | Complejidad |
| --------------------- | ----------- |
| Recursivo             | O(2ⁿ)       |
| Programación Dinámica | O(n)        |

---

## Idea Clave Final

> La Programación Dinámica convierte problemas **exponenciales en lineales**.
