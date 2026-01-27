# **Algoritmo Heap Sort**

---

## ¿Qué es?

**Heap Sort** es un algoritmo de ordenamiento **eficiente y no estable** que utiliza una estructura **Heap (normalmente Max Heap)** para ordenar los elementos.

---

## Idea Clave

> Convierte la lista en un **Heap** y extrae repetidamente el máximo para colocarlo al final.

---

## Cómo Funciona

1. Construir un **Max Heap** a partir del array.
2. Intercambiar la raíz (máximo) con el último elemento.
3. Reducir el tamaño del heap.
4. Reaplicar **heapify** para mantener la propiedad.
5. Repetir hasta ordenar todo el array.

---

## Ejemplo (Java)

```java
void heapSort(int[] arr) {
    int n = arr.length;

    // Construir el heap
    for (int i = n / 2 - 1; i >= 0; i--)
        heapify(arr, n, i);

    // Extraer elementos del heap
    for (int i = n - 1; i > 0; i--) {
        int temp = arr[0];
        arr[0] = arr[i];
        arr[i] = temp;
        heapify(arr, i, 0);
    }
}
```

---

## Complejidad

* **Mejor caso**: O(n log n)
* **Caso promedio**: O(n log n)
* **Peor caso**: O(n log n)

---

## Uso de Memoria

* Algoritmo **in-place**.
* Complejidad espacial: **O(1)**.

---

## Ventajas

* Tiempo garantizado O(n log n).
* No requiere memoria adicional.
* Ideal cuando la memoria es limitada.

---

## Desventajas

* No es estable.
* Más lento que Quick Sort en la práctica.
* Implementación más compleja.

---

## Cuándo Usarlo

* Cuando se requiere rendimiento garantizado.
* Sistemas con memoria limitada.
* Alternativa segura a Quick Sort.

---

## Comparación Rápida

* **Heap Sort**: O(n log n), in-place.
* **Quick Sort**: rápido en promedio.
* **Merge Sort**: estable, usa memoria extra.

---

## Idea Clave Final

> Heap Sort combina **estructura Heap** con ordenamiento eficiente y seguro.
