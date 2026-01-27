# QuickSort

---

## ¿Qué es?
QuickSort es un **algoritmo de ordenamiento** que utiliza el paradigma **Divide y Vencerás** para ordenar una colección de elementos comparándolos con un **pivote**.

---

## Idea Clave
Seleccionar un pivote, **particionar** el arreglo en elementos menores y mayores que él, y **aplicar recursión** sobre cada subarreglo.

---

## Componentes Principales
- **Pivote**: elemento de referencia.
- **Partición**: reorganización del arreglo alrededor del pivote.
- **Recursión**: ordenamiento de subarreglos.
- **Intercambio (swap)**: movimiento de elementos.

---

## Manejo de Colisiones
No existen colisiones como en hashing.  
El caso equivalente es el **tratamiento de elementos iguales al pivote**, que depende de la implementación.

---

## Operaciones Básicas
- Comparaciones
- Intercambios
- División del arreglo
- Llamadas recursivas

---

## Complejidad
- **Mejor caso**: O(n log n)
- **Promedio**: O(n log n)
- **Peor caso**: O(n²)
- **Espacio**: O(log n) (in-place)

---

## Ventajas
- Muy rápido en la práctica
- Uso eficiente de memoria
- Implementación flexible

---

## Desventajas
- No es estable
- Peor caso cuadrático
- Sensible a la elección del pivote

---

## Ejemplos de Uso
- Ordenamiento de grandes arreglos
- Algoritmos internos de bibliotecas estándar
- Sistemas con memoria limitada

---

## Implementaciones Comunes
- Pivote fijo
- Pivote aleatorio
- Median-of-three
- Introsort (QuickSort + HeapSort)

---

## Comparación Rápida
- **QuickSort vs MergeSort**: menos memoria, no estable
- **QuickSort vs HeapSort**: mejor rendimiento promedio
- **QuickSort vs BubbleSort**: muchísimo más eficiente

---

## Ejemplo en Java

```java
public class QuickSort {

    public static void quickSort(int[] arr, int low, int high) {
        if (low < high) {
            int pivotIndex = partition(arr, low, high);
            quickSort(arr, low, pivotIndex - 1);
            quickSort(arr, pivotIndex + 1, high);
        }
    }

    private static int partition(int[] arr, int low, int high) {
        int pivot = arr[high]; // pivote
        int i = low - 1;

        for (int j = low; j < high; j++) {
            if (arr[j] <= pivot) {
                i++;
                swap(arr, i, j);
            }
        }

        swap(arr, i + 1, high);
        return i + 1;
    }

    private static void swap(int[] arr, int i, int j) {
        int temp = arr[i];
        arr[i] = arr[j];
        arr[j] = temp;
    }
}
```

---

### Idea Clave Final

QuickSort es eficiente porque reduce el problema ordenando localmente alrededor de un pivote, logrando gran velocidad con bajo uso de memoria.
