# **Algoritmo Exchange Sort**

---

## ¿Qué es?

**Exchange Sort** es un algoritmo de ordenamiento **simple y comparativo** que ordena una lista **comparando pares de elementos y realizando intercambios** cuando están en el orden incorrecto.

---

## Idea Clave

> Si dos elementos están desordenados, **se intercambian**.

---

## Cómo Funciona

1. Se selecciona un elemento inicial.
2. Se compara con todos los elementos posteriores.
3. Si se encuentra un elemento menor, se intercambian.
4. El proceso continúa con el siguiente elemento.
5. Se repite hasta ordenar toda la lista.

---

## Ejemplo (Java)

```java
void exchangeSort(int[] arr) {
    int n = arr.length;
    for (int i = 0; i < n - 1; i++) {
        for (int j = i + 1; j < n; j++) {
            if (arr[i] > arr[j]) {
                int temp = arr[i];
                arr[i] = arr[j];
                arr[j] = temp;
            }
        }
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

* Implementación muy sencilla.
* Fácil de entender.
* Útil para fines educativos.

---

## Desventajas

* Muy ineficiente para listas grandes.
* Realiza muchos intercambios.

---

## Cuándo Usarlo

* Aprendizaje de algoritmos.
* Listas pequeñas.
* Comparación con otros métodos básicos.

---

## Comparación Rápida

* **Exchange Sort**: intercambia cualquier par desordenado.
* **Bubble Sort**: intercambia elementos adyacentes.
* **Selection Sort**: selecciona el mínimo y lo coloca.

---

## Idea Clave Final

> Exchange Sort es **conceptualmente simple**, pero no adecuado para grandes volúmenes de datos.
