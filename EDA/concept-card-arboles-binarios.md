# **Árboles Binarios**

---

## ¿Qué son?

Los **árboles binarios** son estructuras de datos **jerárquicas** formadas por **nodos**, donde cada nodo puede tener **como máximo dos hijos**: izquierdo y derecho.

---

## Idea Clave

> Cada nodo tiene hasta **dos hijos**, organizados de forma jerárquica.

---

## Componentes de un Árbol

* **Raíz**: nodo inicial.
* **Nodo**: elemento del árbol.
* **Hijos**: nodos descendientes.
* **Padre**: nodo superior.
* **Hoja**: nodo sin hijos.
* **Subárbol**: parte del árbol.

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

## Tipos de Árboles Binarios

### Árbol Binario Simple

* Cada nodo tiene hasta dos hijos.

### Árbol Binario de Búsqueda (BST)

* Izquierda < nodo < derecha.

### Árbol Binario Balanceado

* Altura equilibrada.

---

## Recorridos del Árbol

* **Preorden**: raíz → izquierda → derecha
* **Inorden**: izquierda → raíz → derecha
* **Postorden**: izquierda → derecha → raíz

---

## Operaciones Básicas

* Insertar nodos
* Buscar valores
* Eliminar nodos
* Recorrer el árbol

---

## Complejidad (BST Balanceado)

* Búsqueda: O(log n)
* Inserción: O(log n)
* Eliminación: O(log n)

---

## Ventajas

* Búsquedas eficientes.
* Organización jerárquica.
* Útiles para datos ordenados.

---

## Desventajas

* Puede degradarse a O(n) si no está balanceado.
* Implementación más compleja.

---

## Cuándo Usarlos

* Representar jerarquías.
* Búsquedas y ordenamientos.
* Estructuras como expresiones y rutas.

---

## Comparación Rápida

* **Lista**: estructura lineal.
* **Árbol binario**: estructura jerárquica.

---

## Idea Clave Final

> Los árboles binarios permiten **búsqueda eficiente y organización jerárquica**.
