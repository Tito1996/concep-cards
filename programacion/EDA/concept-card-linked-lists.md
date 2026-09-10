# **Listas Enlazadas (Linked Lists)**

---

## ¿Qué son?

Las **listas enlazadas** son estructuras de datos **lineales y dinámicas** formadas por **nodos**, donde cada nodo almacena un **dato** y una **referencia** al siguiente (y/o anterior) nodo.

---

## Idea Clave

> Los elementos **no están en posiciones contiguas de memoria**; se conectan mediante enlaces.

---

## Estructura de un Nodo

* **Dato**: información almacenada.
* **Referencia**: apunta al siguiente nodo.

```java
class Nodo {
    int dato;
    Nodo siguiente;
}
```

---

## Tipos de Listas Enlazadas

### Lista Simple

* Cada nodo apunta al siguiente.

### Lista Doblemente Enlazada

* Cada nodo apunta al siguiente y al anterior.

### Lista Circular

* El último nodo apunta al primero.

---

## Operaciones Básicas

* Insertar (inicio, medio, final)
* Eliminar nodos
* Recorrer la lista
* Buscar elementos

---

## Ventajas

* Tamaño dinámico.
* Inserciones y eliminaciones eficientes.
* No requiere memoria contigua.

---

## Desventajas

* Acceso secuencial (no aleatorio).
* Mayor uso de memoria (referencias).
* Más complejas que los arrays.

---

## Cuándo Usarlas

* Cuando el tamaño cambia frecuentemente.
* Muchas inserciones/eliminaciones.
* Implementación de pilas y colas.

---

## Comparación Rápida

* **Array**: acceso rápido por índice.
* **Lista enlazada**: inserciones eficientes.

---

## Complejidad

* Acceso: O(n)
* Inserción/eliminación: O(1) (si se tiene la referencia)

---

## Idea Clave Final

> Las listas enlazadas priorizan **flexibilidad** sobre acceso rápido.
