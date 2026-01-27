# **Algoritmo Selection Sort**

---

## ¿Qué es?

**Selection Sort** es un algoritmo de ordenamiento **simple y comparativo** que organiza una lista **seleccionando repetidamente el elemento más pequeño** (o más grande) y colocándolo en su posición correcta.

---

## Idea Clave

> En cada iteración se **selecciona el mínimo** y se intercambia con la primera posición no ordenada.

---

## Cómo Funciona

1. Se asume que el primer elemento es el mínimo.
2. Se recorre la lista para encontrar el menor.
3. Se intercambia con el primer elemento no ordenado.
4. Se avanza a la siguiente posición.
5. Se repite hasta ordenar toda la lista.

---

## Ejemplo (Java)

```java
void selectionSort(int[] arr) {
    int n = arr.length;
    for (int i = 0; i < n - 1; i++) {
        int minIndex = i;
        for (int j = i + 1; j < n; j++) {
            if (arr[j] < arr[minIndex]) {
                minIndex = j;
            }
        }
        int temp = arr[minIndex];
        arr[minIndex] = arr[i];
        arr[i] = temp;
    }
}
```

---

## Complejidad

* **Mejor caso**: O(n²)
* **Peor caso**: O(n²)
* **Caso promedio**: O(n²)

---

## Ventajas

* Implementación sencilla.
* Número mínimo de intercambios.
* No requiere memoria adicional.

---

## Desventajas

* Muy ineficiente para listas grandes.
* Siempre realiza el mismo número de comparaciones.

---

## Cuándo Usarlo

* Contextos educativos.
* Listas pequeñas.
* Cuando los intercambios son costosos.

---

## Comparación Rápida

* **Selection Sort**: pocos intercambios, O(n²).
* **Bubble Sort**: más intercambios, O(n²).
* **Insertion Sort**: mejor para listas casi ordenadas.

---

## Idea Clave Final

> Selection Sort es **simple y predecible**, pero poco eficiente a gran escala.
