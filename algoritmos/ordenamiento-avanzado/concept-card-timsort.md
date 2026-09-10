# **Algoritmo TimSort**

---

## ¿Qué es?

**TimSort** es un algoritmo de ordenamiento **híbrido, estable y eficiente**, que combina **Insertion Sort** y **Merge Sort**. Está optimizado para **datos reales** que suelen estar parcialmente ordenados.

---

## Idea Clave

> Aprovecha **sublistas ya ordenadas (runs)** y las fusiona eficientemente.

---

## Origen y Uso

* Diseñado por **Tim Peters**.
* Usado por defecto en:

  * **Python** (`sorted`, `list.sort`)
  * **Java** (ordenación de objetos)

---

## Concepto de *Run*

Un **run** es una subsecuencia ya ordenada:

* Puede ser creciente o decreciente.
* Si es pequeña, se ordena con **Insertion Sort**.

---

## Cómo Funciona

1. Detecta *runs* naturales en la lista.
2. Extiende runs pequeños con Insertion Sort.
3. Fusiona los runs usando Merge Sort.
4. Mantiene reglas para fusionar eficientemente.

---

## Complejidad

* **Mejor caso**: O(n) → datos casi ordenados
* **Caso promedio**: O(n log n)
* **Peor caso**: O(n log n)

---

## Uso de Memoria

* Requiere **memoria adicional**.
* Complejidad espacial: **O(n)**.

---

## Ventajas

* Muy rápido en la práctica.
* Estable.
* Excelente para datos reales.
* Aprovecha orden previo.

---

## Desventajas

* Implementación compleja.
* Uso adicional de memoria.
* No ideal para sistemas muy limitados.

---

## Cuándo Usarlo

* Ordenamiento general de objetos.
* Datos parcialmente ordenados.
* Cuando se requiere estabilidad.

---

## Comparación Rápida

* **TimSort**: híbrido y estable.
* **Quick Sort**: rápido, no estable.
* **Merge Sort**: estable, más memoria.

---

## Idea Clave Final

> TimSort es rápido porque **aprovecha el orden existente** en los datos.
