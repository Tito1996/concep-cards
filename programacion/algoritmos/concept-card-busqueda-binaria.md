# **Algoritmo de Búsqueda Binaria**

---

## ¿Qué es?

La **búsqueda binaria** es un algoritmo de búsqueda **eficiente** que localiza un elemento en una colección **ordenada** dividiéndola repetidamente en mitades.

---

## Requisito Fundamental

> La colección debe estar **ordenada**.

---

## Idea Clave

> En cada paso se **descarta la mitad** del espacio de búsqueda.

---

## Cómo Funciona

1. Definir los límites **inicio** y **fin**.
2. Calcular el índice **medio**.
3. Comparar el valor buscado con el elemento medio.
4. Si es menor → buscar a la izquierda.
5. Si es mayor → buscar a la derecha.
6. Repetir hasta encontrarlo o agotar el rango.

---

## Ejemplo (Java)

```java
int busquedaBinaria(int[] arr, int objetivo) {
    int ini = 0, fin = arr.length - 1;
    while (ini <= fin) {
        int mid = ini + (fin - ini) / 2;
        if (arr[mid] == objetivo) return mid;
        if (arr[mid] < objetivo) ini = mid + 1;
        else fin = mid - 1;
    }
    return -1;
}
```

---

## Complejidad

* **Mejor caso**: O(1)
* **Caso promedio**: O(log n)
* **Peor caso**: O(log n)

---

## Ventajas

* Muy rápida para grandes volúmenes de datos.
* Reduce drásticamente el número de comparaciones.

---

## Desventajas

* Requiere datos ordenados.
* No funciona bien en listas enlazadas.

---

## Cuándo Usarla

* Arrays o listas ordenadas.
* Búsquedas frecuentes.
* Datos estáticos o poco cambiantes.

---

## Comparación Rápida

* **Búsqueda Lineal**: O(n), sin orden.
* **Búsqueda Binaria**: O(log n), requiere orden.

---

## Idea Clave Final

> La búsqueda binaria es eficiente porque **divide el problema en cada paso**.
