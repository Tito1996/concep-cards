# **Pilas y Colas**

---

## ¿Qué son?

Las **pilas (stacks)** y **colas (queues)** son **estructuras de datos lineales** que organizan los elementos según un orden específico de inserción y extracción.

---

## Pila (Stack)

### Concepto

Funciona bajo el principio **LIFO** (*Last In, First Out*): el **último en entrar es el primero en salir**.

### Operaciones Básicas

* **push** → insertar elemento
* **pop** → eliminar el último elemento
* **peek/top** → consultar el último elemento

### Usos Comunes

* Deshacer/rehacer (undo/redo)
* Llamadas a funciones (call stack)
* Evaluación de expresiones

---

## Cola (Queue)

### Concepto

Funciona bajo el principio **FIFO** (*First In, First Out*): el **primero en entrar es el primero en salir**.

### Operaciones Básicas

* **enqueue** → insertar elemento
* **dequeue** → eliminar el primer elemento
* **peek/front** → consultar el primer elemento

### Usos Comunes

* Gestión de tareas
* Colas de impresión
* Sistemas de mensajería

---

## Variantes Importantes

* **Cola circular**
* **Cola de prioridad**
* **Deque** (doble cola)

---

## Ejemplo (Java)

```java
Stack<Integer> pila = new Stack<>();
pila.push(1);
pila.pop();

Queue<Integer> cola = new LinkedList<>();
cola.add(1);
cola.poll();
```

---

## Ventajas

* Implementación sencilla.
* Control claro del orden de acceso.
* Muy eficientes.

---

## Desventajas

* Acceso limitado (no aleatorio).
* No adecuadas para búsquedas complejas.

---

## Comparación Rápida

| Estructura | Orden |
| ---------- | ----- |
| Pila       | LIFO  |
| Cola       | FIFO  |

---

## Idea Clave Final

> **Pilas** gestionan el último elemento agregado; **colas** gestionan el primero.
