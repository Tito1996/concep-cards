# **Árbol AVL**

---

## ¿Qué es?

Un **Árbol AVL** es un **Árbol Binario de Búsqueda auto‑balanceado** que mantiene su altura equilibrada tras cada inserción o eliminación.

---

## Idea Clave

> Para cada nodo, la **diferencia de alturas** entre subárbol izquierdo y derecho es **−1, 0 o +1**.

---

## Factor de Balance

**Factor de balance = altura(izq) − altura(der)**

* Valores permitidos: **−1, 0, +1**
* Si se sale de ese rango → se **rebalancea**.

---

## ¿Cómo se Rebalancea?

Mediante **rotaciones**:

* **Rotación simple derecha (LL)**
* **Rotación simple izquierda (RR)**
* **Rotación doble izquierda‑derecha (LR)**
* **Rotación doble derecha‑izquierda (RL)**

---

## Operaciones Básicas

* **Inserción**: como BST + rebalanceo
* **Búsqueda**: igual que BST
* **Eliminación**: como BST + rebalanceo

---

## Complejidad

| Operación   | Complejidad |
| ----------- | ----------- |
| Búsqueda    | O(log n)    |
| Inserción   | O(log n)    |
| Eliminación | O(log n)    |

---

## Ventajas

* Rendimiento garantizado O(log n).
* Árbol siempre balanceado.
* Ideal para búsquedas frecuentes.

---

## Desventajas

* Implementación compleja.
* Más rotaciones que otros árboles balanceados.
* Inserciones ligeramente más costosas.

---

## Cuándo Usarlo

* Sistemas con muchas búsquedas.
* Datos dinámicos que deben mantenerse ordenados.
* Cuando se requiere rendimiento estable.

---

## Comparación Rápida

* **BST**: rápido si está balanceado.
* **AVL**: siempre balanceado.
* **Red‑Black**: menos balanceo, inserciones más rápidas.

---

## Idea Clave Final

> El árbol AVL garantiza eficiencia manteniendo el **equilibrio automáticamente**.
