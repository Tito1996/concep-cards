# **BFS — Búsqueda en Anchura**

---

## ¿Qué es?

BFS (*Breadth‑First Search*) es un algoritmo de recorrido de grafos que explora los nodos **por niveles**, visitando primero los más cercanos al nodo inicial.

---

## Idea Clave

> Visita primero los vecinos más próximos.

---

## Cómo Funciona

1. Se inicia desde un nodo origen.
2. Se visitan todos sus vecinos.
3. Luego los vecinos de esos vecinos.
4. Se repite por niveles.

---

## Estructura Usada

* **Cola (Queue)**

---

## Complejidad

* **Tiempo**: O(V + E)
* **Espacio**: O(V)

---

## Ventajas

* Encuentra el camino más corto en grafos no ponderados.
* Fácil de implementar.

---

## Usos Comunes

* Caminos mínimos sin pesos.
* Redes sociales.
* Sistemas por niveles.

---

## Idea Clave Final

> BFS es ideal para encontrar **distancias mínimas** sin pesos.
