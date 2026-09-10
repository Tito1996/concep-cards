# **Algoritmo Quick Sort**

---

## ¿Qué es?

**Quick Sort** es un algoritmo de ordenamiento **eficiente** basado en **divide y vencerás**, que ordena una lista **particionándola** alrededor de un elemento llamado **pivote**.

---

## Idea Clave

> Coloca el pivote en su posición correcta y ordena **recursivamente** los elementos menores y mayores.

---

## Cómo Funciona

1. Elegir un **pivote**.
2. Reordenar la lista: menores a la izquierda, mayores a la derecha.
3. El pivote queda en su posición final.
4. Aplicar Quick Sort a cada sublista.

---

## Elección del Pivote

* Primer elemento
* Último elemento
* Elemento central
* **Aleatorio** (reduce el peor caso)

---

## Ejemplo (Java)

```java
void quickSort(int[] arr, int low, int high) {
    if (low < high) {
        int p = particion(arr, low, high);
        quickSort(arr, low, p - 1);
        quickSort(arr, p + 1, high);
    }
}
```

---

## Complejidad

* **Mejor caso**: O(n log n)
* **Caso promedio**: O(n log n)
* **Peor caso**: O(n²) (mal pivote)

---

## Uso de Memoria

* Algoritmo **in-place**.
* Complejidad espacial: **O(log n)** (recursión).

---

## Ventajas

* Muy rápido en la práctica.
* No requiere memoria adicional significativa.
* Amplio uso en librerías estándar.

---

## Desventajas

* No es estable.
* Peor caso O(n²) si el pivote es malo.

---

## Cuándo Usarlo

* Listas grandes.
* Cuando el rendimiento es prioritario.
* Cuando no se requiere estabilidad.

---

## Comparación Rápida

* **Quick Sort**: rápido en promedio, in-place.
* **Merge Sort**: estable, requiere memoria extra.
* **Heap Sort**: O(n log n) garantizado.

---

## Idea Clave Final

> Quick Sort es rápido porque **reduce el problema en cada partición**.
