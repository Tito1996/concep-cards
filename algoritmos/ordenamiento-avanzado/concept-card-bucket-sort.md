# **Algoritmo Bucket Sort**

---

## ¿Qué es?

**Bucket Sort** es un algoritmo de ordenamiento **no comparativo** que distribuye los elementos en varios **contenedores (buckets)**, los ordena individualmente y luego los concatena.

---

## Idea Clave

> Distribuye los datos en **rangos**, ordena cada rango y los **une**.

---

## Requisitos

* Datos **uniformemente distribuidos**.
* Conocimiento aproximado del **rango** de valores.
* Algoritmo auxiliar para ordenar cada bucket (p. ej., Insertion Sort).

---

## Cómo Funciona

1. Crear *k* buckets vacíos.
2. Distribuir cada elemento en su bucket correspondiente.
3. Ordenar cada bucket individualmente.
4. Concatenar los buckets en orden.

---

## Ejemplo Conceptual

Entrada: `[0.42, 0.32, 0.23, 0.52]`

Buckets:

* B0: `[0.23]`
* B1: `[0.32]`
* B2: `[0.42]`
* B3: `[0.52]`

Salida ordenada: `[0.23, 0.32, 0.42, 0.52]`

---

## Complejidad

* **Mejor / Promedio**: O(n + k)
* **Peor caso**: O(n²)
* **Espacio**: O(n + k)

*n = elementos, k = buckets*

---

## Ventajas

* Muy eficiente con distribución uniforme.
* Puede ser estable.
* Fácil de paralelizar.

---

## Desventajas

* Rendimiento depende de la distribución.
* Uso adicional de memoria.
* No adecuado para datos muy dispersos.

---

## Cuándo Usarlo

* Números reales en rangos conocidos.
* Datos uniformes.
* Grandes volúmenes con distribución predecible.

---

## Comparación Rápida

* **Bucket Sort**: distribución por rangos.
* **Counting Sort**: conteo por valor exacto.
* **Radix Sort**: ordena por dígitos.

---

## Idea Clave Final

> Bucket Sort es rápido **si los datos están bien distribuidos**.
