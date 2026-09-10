# **DAG — Grafo Dirigido Acíclico**

---

## ¿Qué es?

Un **DAG** (*Directed Acyclic Graph*) es un grafo **dirigido** que **no contiene ciclos**.

---

## Idea Clave

> No es posible volver al mismo nodo siguiendo las direcciones.

---

## Características

* Direcciones definidas.
* Sin ciclos.
* Permite orden lógico.

---

## Operación Clave

### Ordenamiento Topológico

* Ordena los nodos respetando dependencias.
* Se basa en DFS o BFS.

---

## Complejidad

* **O(V + E)**

---

## Ventajas

* Ideal para representar dependencias.
* Estructura clara y predecible.

---

## Usos Comunes

* Planificación de tareas.
* Compiladores.
* Pipelines y workflows.

---

## Comparación Rápida

* **Árbol**: DAG especial.
* **Grafo general**: puede tener ciclos.

---

## Idea Clave Final

> Un DAG modela **dependencias sin ciclos**.
