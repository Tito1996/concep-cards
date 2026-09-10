# **Algoritmo Merge Sort**

---

## ¿Qué es?

**Merge Sort** es un algoritmo de ordenamiento **eficiente y estable** basado en la técnica de **divide y vencerás**, que divide la lista en partes más pequeñas, las ordena y luego las fusiona.

---

## Idea Clave

> Divide la lista en mitades, ordénalas y **combínalas** de forma ordenada.

---

## Cómo Funciona

1. Divide la lista en dos mitades.
2. Aplica Merge Sort recursivamente a cada mitad.
3. Fusiona (*merge*) las mitades ordenadas.
4. Repite hasta obtener la lista completa ordenada.

---

## Ejemplo (Java)

```java
void mergeSort(int[] arr, int l, int r) {
    if (l < r) {
        int m = (l + r) / 2;
        mergeSort(arr, l, m);
        mergeSort(arr, m + 1, r);
        merge(arr, l, m, r);
    }
}
```

---

## Complejidad

* **Mejor caso**: O(n log n)
* **Peor caso**: O(n log n)
* **Caso promedio**: O(n log n)

---

## Uso de Memoria

* Requiere **memoria adicional** para fusionar listas.
* Complejidad espacial: **O(n)**.

---

## Ventajas

* Rendimiento garantizado O(n log n).
* Algoritmo **estable**.
* Muy eficiente para grandes volúmenes de datos.

---

## Desventajas

* Uso adicional de memoria.
* Más lento que Quick Sort en algunos casos prácticos.

---

## Cuándo Usarlo

* Listas grandes.
* Cuando se requiere estabilidad.
* Procesamiento de grandes volúmenes de datos.

---

## Comparación Rápida

* **Merge Sort**: estable, O(n log n).
* **Quick Sort**: rápido en promedio, no estable.
* **Heap Sort**: O(n log n), sin memoria extra.

---

## Idea Clave Final

> Merge Sort garantiza eficiencia dividiendo el problema en partes pequeñas.
