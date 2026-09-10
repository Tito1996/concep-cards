# **Comparativa Visual de Complejidades (Big O)**

---

## ¿Qué representa Big O?

La notación **Big O** describe cómo **crece el coste** (tiempo o espacio) de un algoritmo cuando aumenta el tamaño de la entrada (*n*).

---

## Escala de Complejidades (de mejor a peor)

1. **O(1)** — Constante
2. **O(log n)** — Logarítmica
3. **O(n)** — Lineal
4. **O(n log n)** — Linealítmica
5. **O(n²)** — Cuadrática
6. **O(2ⁿ)** — Exponencial
7. **O(n!)** — Factorial

---

## Tabla Comparativa

| Complejidad | Crecimiento         | Ejemplo típico      |
| ----------- | ------------------- | ------------------- |
| O(1)        | Constante           | Acceso a array      |
| O(log n)    | Muy lento           | Búsqueda binaria    |
| O(n)        | Proporcional        | Recorrer lista      |
| O(n log n)  | Eficiente           | Merge / Quick Sort  |
| O(n²)       | Rápido              | Bubble / Selection  |
| O(2ⁿ)       | Explosivo           | Fibonacci recursivo |
| O(n!)       | Extremadamente alto | Fuerza bruta        |

---

## Comparación Intuitiva

Para n = 10:

* O(n) → 10
* O(n²) → 100
* O(2ⁿ) → 1.024
* O(n!) → 3.628.800

---

## Regla Práctica

* **≤ O(n log n)** → aceptable
* **O(n²)** → cuidado
* **≥ O(2ⁿ)** → evitar

---

## Relación con Algoritmos

* **Búsqueda binaria** → O(log n)
* **Quick Sort** → O(n log n)
* **Bubble Sort** → O(n²)
* **Backtracking** → O(2ⁿ)

---

## Idea Clave Final

> Una pequeña diferencia en Big O implica **enormes diferencias de rendimiento** al escalar.
