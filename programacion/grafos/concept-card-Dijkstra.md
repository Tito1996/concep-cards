# **Algoritmo de Dijkstra**

---

## ¿Qué es?

Dijkstra es un algoritmo que calcula el **camino más corto** desde un nodo origen hacia todos los demás en un grafo **ponderado sin pesos negativos**.

---

## Idea Clave

> Siempre elige el nodo con **menor distancia acumulada**.

---

## Cómo Funciona

1. Inicializa distancias infinitas.
2. Marca el nodo origen con distancia 0.
3. Selecciona el nodo no visitado más cercano.
4. Actualiza distancias de sus vecinos.
5. Repite hasta visitar todos.

---

## Estructura Usada

* **Cola de prioridad (Heap)**

---

## Complejidad

* **O((V + E) log V)**

---

## Ventajas

* Encuentra rutas óptimas.
* Muy usado en la práctica.

---

## Limitación Importante

* ❌ No admite pesos negativos.

---

## Usos Comunes

* Mapas y GPS.
* Redes y routing.

---

## Idea Clave Final

> Dijkstra garantiza el **camino mínimo** sin pesos negativos.
