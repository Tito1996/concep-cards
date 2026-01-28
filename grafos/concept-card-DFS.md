# **DFS — Búsqueda en Profundidad**

---

## ¿Qué es?

DFS (*Depth‑First Search*) es un algoritmo de recorrido de grafos que explora **lo más profundo posible** antes de retroceder.

---

## Idea Clave

> Avanza todo lo posible antes de retroceder.

---

## Cómo Funciona

1. Comienza en un nodo.
2. Visita un vecino no visitado.
3. Continúa hasta no poder avanzar.
4. Retrocede (*backtracking*).

---

## Estructura Usada

* **Pila** o **recursión**

---

## Complejidad

* **Tiempo**: O(V + E)
* **Espacio**: O(V)

---

## Ventajas

* Útil para detección de ciclos.
* Base del backtracking.

---

## Usos Comunes

* Componentes conexos.
* Detección de ciclos.
* Ordenamiento topológico.

---

## Idea Clave Final

> DFS explora **en profundidad**, no en distancia mínima.
