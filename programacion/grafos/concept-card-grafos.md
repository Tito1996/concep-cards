# **Grafos**

---

## ¿Qué son?

Un **grafo** es una estructura de datos que representa **relaciones** entre elementos mediante **nodos (vértices)** y **aristas**.

---

## Idea Clave

> Un grafo modela **conexiones** entre entidades.

---

## Componentes

* **Vértices (nodos)**: elementos del grafo.
* **Aristas**: conexiones entre vértices.
* **Peso** (opcional): costo de una arista.

---

## Tipos de Grafos

### Según Dirección

* **No dirigido**: conexiones bidireccionales.
* **Dirigido (digrafo)**: conexiones con sentido.

### Según Peso

* **No ponderado**: todas las aristas iguales.
* **Ponderado**: aristas con peso.

### Otros Tipos

* **Grafo conexo / no conexo**
* **Grafo cíclico / acíclico**
* **Árbol**: grafo conexo sin ciclos

---

## Representaciones

### Lista de Adyacencia

* Más eficiente en memoria.
* Ideal para grafos dispersos.

### Matriz de Adyacencia

* Acceso rápido.
* Consume más memoria.

---

## Recorridos Básicos

### BFS (Breadth‑First Search)

* Recorre por **niveles**.
* Usa **cola**.
* Complejidad: O(V + E).

### DFS (Depth‑First Search)

* Recorre en **profundidad**.
* Usa **pila o recursión**.
* Complejidad: O(V + E).

---

## Aplicaciones Comunes

* Redes sociales.
* Mapas y rutas.
* Sistemas de recomendación.
* Dependencias entre tareas.

---

## Ventajas

* Modelo muy flexible.
* Representa problemas reales complejos.

---

## Desventajas

* Implementación más compleja.
* Alto consumo si el grafo es denso.

---

## Comparación Rápida

* **Árbol**: grafo sin ciclos.
* **Grafo**: permite ciclos y múltiples caminos.

---

## Idea Clave Final

> Los grafos permiten modelar **relaciones complejas** entre datos.
