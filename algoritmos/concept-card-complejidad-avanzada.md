# **Análisis de Complejidad Avanzado**

---

## ¿Qué es?

El **análisis de complejidad avanzado** estudia cómo **escala un algoritmo** considerando distintos escenarios (mejor, promedio, peor), tipos de crecimiento y **costes temporales y espaciales**.

---

## Notaciones Asintóticas

### Big O — Cota Superior

* Límite **máximo** del crecimiento.
* Garantiza el peor caso.

### Ω (Omega) — Cota Inferior

* Límite **mínimo** del crecimiento.

### Θ (Theta) — Cota Ajustada

* Crecimiento **exacto** (mejor descripción).

---

## Complejidades Comunes

| Notación   | Tipo de Crecimiento |
| ---------- | ------------------- |
| O(1)       | Constante           |
| O(log n)   | Logarítmico         |
| O(n)       | Lineal              |
| O(n log n) | Linealítmico        |
| O(n²)      | Cuadrático          |
| O(2ⁿ)      | Exponencial         |
| O(n!)      | Factorial           |

---

## Casos de Análisis

* **Mejor caso**: escenario más favorable.
* **Caso promedio**: comportamiento esperado.
* **Peor caso**: escenario más costoso.

---

## Complejidad Temporal vs Espacial

### Temporal

* Tiempo de ejecución.
* Número de operaciones.

### Espacial

* Memoria adicional usada.
* Estructuras auxiliares y recursión.

---

## Análisis de Bucles

* Bucle simple → **O(n)**
* Bucles anidados → **O(n²)**
* Bucle que divide entre 2 → **O(log n)**

---

## Recurrencias Comunes

* **Divide y vencerás**:

  * T(n) = 2T(n/2) + O(n) → **O(n log n)**
* **Recursión lineal**:

  * T(n) = T(n-1) + O(1) → **O(n)**

---

## Amortized Analysis

* Evalúa el **costo promedio real** de una secuencia de operaciones.
* Ejemplo: inserciones en arrays dinámicos.

---

## Trade-offs Clásicos

* Tiempo vs Memoria.
* Simplicidad vs Rendimiento.
* Estabilidad vs Velocidad.

---

## Errores Comunes

* Ignorar constantes grandes.
* Analizar solo el mejor caso.
* Confundir O(n log n) con O(n²).

---

## Idea Clave Final

> El análisis avanzado permite **elegir el algoritmo correcto** según escala y contexto.
