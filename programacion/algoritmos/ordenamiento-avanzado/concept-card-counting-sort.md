# **Algoritmo Counting Sort**

---

## ¿Qué es?

**Counting Sort** es un algoritmo de ordenamiento **no comparativo** que ordena elementos **contando la frecuencia** de cada valor dentro de un rango conocido.

---

## Idea Clave

> No compara elementos entre sí: **cuenta cuántas veces aparece cada valor**.

---

## Requisitos

* Los elementos deben ser **enteros**.
* El rango de valores (**k**) debe ser **conocido y limitado**.

---

## Cómo Funciona

1. Crear un array de conteo de tamaño *k*.
2. Contar la frecuencia de cada valor.
3. Calcular posiciones acumuladas.
4. Colocar cada elemento en su posición ordenada.

---

## Ejemplo Conceptual

Entrada: `[4, 2, 2, 8, 3]`

Conteo:

* 2 → 2 veces
* 3 → 1 vez
* 4 → 1 vez
* 8 → 1 vez

Salida ordenada: `[2, 2, 3, 4, 8]`

---

## Complejidad

* **Tiempo**: O(n + k)
* **Espacio**: O(n + k)

*n = número de elementos, k = rango de valores*

---

## Ventajas

* Muy rápido para rangos pequeños.
* Tiempo lineal.
* Algoritmo estable (implementación correcta).

---

## Desventajas

* Uso adicional de memoria.
* No funciona bien con rangos grandes.
* No aplicable a datos no numéricos.

---

## Cuándo Usarlo

* Valores enteros pequeños.
* Grandes volúmenes de datos.
* Cuando se requiere rendimiento lineal.

---

## Comparación Rápida

* **Counting Sort**: O(n + k), no comparativo.
* **Quick Sort**: O(n log n), comparativo.
* **Merge Sort**: O(n log n), estable.

---

## Idea Clave Final

> Counting Sort es extremadamente eficiente **si el rango de valores es pequeño**.
