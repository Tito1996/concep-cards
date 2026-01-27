# **Algoritmo Shell Sort**

---

## ¿Qué es?

**Shell Sort** es un algoritmo de ordenamiento **mejorado de Insertion Sort** que permite intercambios lejanos usando **saltos (gaps)** para reducir el desorden rápidamente.

---

## Idea Clave

> Ordena primero elementos **lejanos** y va reduciendo el salto hasta ordenar por completo.

---

## Cómo Funciona

1. Se elige un **gap** inicial (por ejemplo, n/2).
2. Se ordenan sublistas separadas por ese gap usando Insertion Sort.
3. Se reduce el gap progresivamente.
4. Cuando el gap es 1, se realiza un Insertion Sort final.

---

## Ejemplo (Java)

```java
void shellSort(int[] arr) {
    int n = arr.length;
    for (int gap = n / 2; gap > 0; gap /= 2) {
        for (int i = gap; i < n; i++) {
            int temp = arr[i];
            int j = i;
            while (j >= gap && arr[j - gap] > temp) {
                arr[j] = arr[j - gap];
                j -= gap;
            }
            arr[j] = temp;
        }
    }
}
```

---

## Complejidad

* **Mejor caso**: O(n log n)
* **Peor caso**: depende del gap (≈ O(n²))
* **Caso promedio**: entre O(n log n) y O(n^1.5)

---

## Ventajas

* Más rápido que Insertion y Bubble Sort.
* No requiere memoria adicional.
* Fácil de implementar.

---

## Desventajas

* Complejidad depende de la secuencia de gaps.
* No es estable.
* Menos eficiente que Quick/Merge Sort.

---

## Cuándo Usarlo

* Listas medianas.
* Cuando se busca algo simple pero más eficiente que O(n²).
* Sistemas con memoria limitada.

---

## Comparación Rápida

* **Shell Sort**: inserciones con saltos.
* **Insertion Sort**: inserciones adyacentes.
* **Quick Sort**: divide y vencerás.

---

## Idea Clave Final

> Shell Sort mejora Insertion Sort reduciendo el desorden **antes** del ordenamiento final.
 
