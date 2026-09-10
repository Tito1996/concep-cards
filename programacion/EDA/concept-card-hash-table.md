# **Hash Tables (Tablas Hash)**

---

## ¿Qué son?

Las **Hash Tables** son estructuras de datos que almacenan información en **pares clave–valor**, utilizando una **función hash** para calcular la posición donde se guarda cada valor.

---

## Idea Clave

> La clave se transforma con una **función hash** para acceder al valor en **tiempo constante**.

---

## Componentes Principales

### Función Hash

* Convierte una clave en un índice numérico.
* Debe ser rápida y distribuir bien los datos.

### Tabla (Array)

* Estructura subyacente donde se almacenan los datos.

### Colisiones

* Ocurren cuando dos claves generan el mismo índice.

---

## Manejo de Colisiones

* **Encadenamiento (Chaining)**: lista en cada posición.
* **Direcciones Abiertas**: búsqueda de otra posición (linear probing).

---

## Operaciones Básicas

* **Insertar (put)**
* **Buscar (get)**
* **Eliminar (remove)**

---

## Complejidad

| Operación | Promedio | Peor Caso |
| --------- | -------- | --------- |
| Buscar    | O(1)     | O(n)      |
| Insertar  | O(1)     | O(n)      |
| Eliminar  | O(1)     | O(n)      |

---

## Ventajas

* Acceso muy rápido.
* Ideal para búsquedas y asociaciones.
* Muy usada en la práctica.

---

## Desventajas

* Uso adicional de memoria.
* Depende de una buena función hash.
* No mantiene orden.

---

## Ejemplos de Uso

* Diccionarios y mapas.
* Cachés.
* Conteo de frecuencias.

---

## Implementaciones Comunes

* Java: `HashMap`
* Python: `dict`
* C#: `Dictionary`

---

## Comparación Rápida

* **Hash Table**: acceso por clave O(1).
* **Árbol (AVL/BST)**: acceso ordenado O(log n).

---

## Idea Clave Final

> Las hash tables priorizan **velocidad de acceso**, no el orden.
