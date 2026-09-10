# **Algoritmo de Ordenamiento Básico**

---

## ¿Qué es?

Un **algoritmo de ordenamiento básico** organiza una colección de elementos (números, cadenas, objetos) en un **orden determinado**, normalmente ascendente o descendente.

---

## Ejemplo Clásico: **Bubble Sort**

### Idea Principal

Compara **elementos adyacentes** y los intercambia si están en el orden incorrecto. El proceso se repite hasta que la lista queda ordenada.

---

## Cómo Funciona

1. Se recorren los elementos de la lista.
2. Se comparan pares consecutivos.
3. Si están desordenados, se intercambian.
4. Cada pasada coloca el elemento mayor al final.
5. Se repite hasta que no haya intercambios.

---

## Ejemplo (Java)

```java
void bubbleSort(int[] arr) {
    int n = arr.length;
    for (int i = 0; i < n - 1; i++) {
        for (int j = 0; j < n - i - 1; j++) {
            if (arr[j] > arr[j + 1]) {
                int temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
}
```

---

## Complejidad

* **Mejor caso**: O(n) (lista ya ordenada, con optimización).
* **Peor caso**: O(n²).
* **Caso promedio**: O(n²).

---

## Ventajas

* Muy fácil de entender.
* Implementación sencilla.
* Útil para aprendizaje.

---

## Desventajas

* Muy ineficiente para listas grandes.
* No recomendado en producción.

---

## Cuándo Usarlo

* Aprender algoritmos de ordenamiento.
* Listas pequeñas.
* Contextos educativos.

---

## Comparación Rápida

* **Bubble Sort**: simple, O(n²).
* **Insertion Sort**: más eficiente en listas pequeñas.
* **Quick Sort**: mucho más rápido, O(n log n).

---

## Idea Clave Final

> Los algoritmos de ordenamiento básicos son ideales para **aprender**, no para grandes volúmenes de datos.
