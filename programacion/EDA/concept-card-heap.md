# **Heap (Árbol Binario de Prioridad)**

---

## ¿Qué es?

Un **Heap** es una estructura de datos basada en un **árbol binario completo** que cumple la **propiedad de heap**, usada para gestionar prioridades.

---

## Idea Clave

> El elemento de **mayor o menor prioridad** siempre está en la **raíz**.

---

## Tipos de Heap

### Max Heap

* Cada nodo es **mayor o igual** que sus hijos.
* La raíz contiene el **máximo**.

### Min Heap

* Cada nodo es **menor o igual** que sus hijos.
* La raíz contiene el **mínimo**.

---

## Propiedad de Heap

* Es un **árbol binario completo** (se llena por niveles, de izquierda a derecha).
* **No está ordenado** como un BST.

---

## Representación

Normalmente se implementa con un **array**:

* Padre: `i`
* Hijo izquierdo: `2i + 1`
* Hijo derecho: `2i + 2`

---

## Operaciones Básicas

* **Insertar** (heapify up)
* **Eliminar raíz** (heapify down)
* **Obtener min/max**

---

## Complejidad

| Operación    | Complejidad |
| ------------ | ----------- |
| Obtener raíz | O(1)        |
| Inserción    | O(log n)    |
| Eliminación  | O(log n)    |

---

## Ventajas

* Acceso rápido al mínimo o máximo.
* Implementación eficiente con arrays.
* Base de colas de prioridad.

---

## Desventajas

* Búsqueda general es O(n).
* No mantiene orden total.

---

## Cuándo Usarlo

* **Colas de prioridad**.
* Algoritmos como **Dijkstra** y **Heap Sort**.
* Gestión de tareas.

---

## Comparación Rápida

* **Heap**: acceso rápido al min/max.
* **BST/AVL**: datos ordenados.
* **Lista**: acceso secuencial.

---

## Idea Clave Final

> Un Heap prioriza el **acceso rápido**, no el orden completo.
