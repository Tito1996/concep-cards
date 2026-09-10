# **Algoritmo de Búsqueda Lineal**

---

## ¿Qué es?

La **búsqueda lineal** (o secuencial) es un algoritmo que **recorre una colección elemento por elemento** hasta encontrar el valor buscado o hasta llegar al final.

---

## Idea Clave

> Se compara el elemento buscado **con cada elemento**, uno a uno.

---

## Cómo Funciona

1. Comienza desde el primer elemento.
2. Compara el elemento actual con el valor buscado.
3. Si coincide, se detiene.
4. Si no, continúa con el siguiente.
5. Si llega al final, el elemento no existe.

---

## Ejemplo (Java)

```java
int buscar(int[] arr, int objetivo) {
    for (int i = 0; i < arr.length; i++) {
        if (arr[i] == objetivo) {
            return i; // encontrado
        }
    }
    return -1; // no encontrado
}
```

---

## Complejidad

* **Mejor caso**: O(1) → el elemento está al inicio.
* **Peor caso**: O(n) → el elemento está al final o no existe.
* **Caso promedio**: O(n).

---

## Ventajas

* Muy fácil de implementar.
* No requiere datos ordenados.
* Funciona con cualquier estructura lineal.

---

## Desventajas

* Poco eficiente con grandes volúmenes de datos.
* Tiempo de búsqueda alto en el peor caso.

---

## Cuándo Usarlo

* Listas pequeñas.
* Datos no ordenados.
* Búsquedas simples o poco frecuentes.

---

## Comparación Rápida

* **Búsqueda Lineal**: simple, O(n).
* **Búsqueda Binaria**: más rápida, O(log n), requiere datos ordenados.

---

## Idea Clave Final

> La búsqueda lineal es **simple y universal**, pero no la más eficiente.
