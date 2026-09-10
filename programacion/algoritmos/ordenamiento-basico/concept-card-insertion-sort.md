# **Algoritmo Insertion Sort**

---

## ¿Qué es?

**Insertion Sort** es un algoritmo de ordenamiento **simple y eficiente para listas pequeñas o casi ordenadas**, que construye la lista ordenada **insertando cada elemento en su posición correcta**.

---

## Idea Clave

> Cada nuevo elemento se **inserta** en el lugar adecuado dentro de la parte ya ordenada.

---

## Cómo Funciona

1. Se considera el primer elemento como ordenado.
2. Se toma el siguiente elemento.
3. Se compara con los elementos anteriores.
4. Se desplazan los mayores una posición a la derecha.
5. Se inserta el elemento en su posición correcta.
6. Se repite hasta finalizar la lista.

---

## Ejemplo (Java)

```java
void insertionSort(int[] arr) {
    for (int i = 1; i < arr.length; i++) {
        int clave = arr[i];
        int j = i - 1;
        while (j >= 0 && arr[j] > clave) {
            arr[j + 1] = arr[j];
            j--;
        }
        arr[j + 1] = clave;
    }
}
```

---

## Complejidad

* **Mejor caso**: O(n) → lista casi ordenada.
* **Peor caso**: O(n²) → lista inversamente ordenada.
* **Caso promedio**: O(n²).

---

## Ventajas

* Fácil de implementar.
* Muy eficiente en listas pequeñas.
* Estable (mantiene el orden relativo).
* No requiere memoria adicional.

---

## Desventajas

* Ineficiente para listas grandes.
* Muchas comparaciones en el peor caso.

---

## Cuándo Usarlo

* Listas pequeñas.
* Datos casi ordenados.
* Como parte de algoritmos híbridos.

---

## Comparación Rápida

* **Insertion Sort**: eficiente en listas casi ordenadas.
* **Selection Sort**: menos intercambios, siempre O(n²).
* **Bubble Sort**: más intercambios.

---

## Idea Clave Final

> Insertion Sort es **simple, estable y eficaz** cuando los datos están casi ordenados.
