# **Árbol Binario de Búsqueda (BST)**

---

## ¿Qué es?

Un **Árbol Binario de Búsqueda (BST)** es un árbol binario donde, para cada nodo:

* Los valores del **subárbol izquierdo** son menores.
* Los valores del **subárbol derecho** son mayores.

---

## Idea Clave

> Izquierda < Nodo < Derecha

---

## Propiedades

* No hay valores duplicados (en la forma clásica).
* Mantiene los datos **ordenados**.
* Permite búsquedas eficientes.

---

## Estructura de un Nodo

```java
class Nodo {
    int valor;
    Nodo izquierdo;
    Nodo derecho;
}
```

---

## Operaciones Básicas

### Inserción

* Se compara el valor.
* Se baja por izquierda o derecha.
* Se inserta como hoja.

### Búsqueda

* Comparación recursiva.
* Se descarta medio árbol en cada paso.

### Eliminación

* Nodo hoja.
* Nodo con un hijo.
* Nodo con dos hijos (reemplazo por sucesor).

---

## Recorrido Inorden

* Izquierda → Raíz → Derecha
* Devuelve los valores **ordenados**.

---

## Complejidad

### BST Balanceado

* Búsqueda: O(log n)
* Inserción: O(log n)
* Eliminación: O(log n)

### BST Desbalanceado

* Todas las operaciones: O(n)

---

## Ventajas

* Búsqueda eficiente.
* Mantiene orden natural.
* Implementación clara.

---

## Desventajas

* Puede desbalancearse.
* Rendimiento depende del orden de inserción.

---

## Cuándo Usarlo

* Datos que deben mantenerse ordenados.
* Búsquedas frecuentes.
* Base para árboles balanceados (AVL, Red-Black).

---

## Comparación Rápida

* **BST**: ordenado, puede desbalancearse.
* **AVL**: BST auto-balanceado.
* **Heap**: acceso rápido al mínimo/máximo.

---

## Idea Clave Final

> Un BST es eficiente **solo si está balanceado**.
