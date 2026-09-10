# **Algoritmo Radix Sort**

---

## ¿Qué es?

**Radix Sort** es un algoritmo de ordenamiento **no comparativo** que ordena números **procesando sus dígitos** (o caracteres) desde el menos significativo al más significativo (LSD) o viceversa (MSD).

---

## Idea Clave

> Ordena por **dígitos**, no comparando números completos.

---

## Requisitos

* Datos **numéricos** o cadenas.
* Longitud máxima de dígitos conocida.
* Usa un algoritmo **estable** como subproceso (normalmente Counting Sort).

---

## Cómo Funciona (LSD)

1. Ordenar por el **dígito menos significativo**.
2. Repetir para el siguiente dígito.
3. Continuar hasta el dígito más significativo.

---

## Ejemplo Conceptual

Entrada: `[170, 45, 75, 90]`

* Unidades → `[170, 90, 45, 75]`
* Decenas → `[170, 45, 75, 90]`
* Centenas → `[45, 75, 90, 170]`

---

## Complejidad

* **Tiempo**: O(d · (n + k))
* **Espacio**: O(n + k)

*d = número de dígitos, k = base (ej. 10)*

---

## Ventajas

* Muy rápido para claves de tamaño fijo.
* No comparativo.
* Puede ser estable.

---

## Desventajas

* Uso adicional de memoria.
* No eficiente para rangos o longitudes grandes.
* Implementación más compleja.

---

## Cuándo Usarlo

* Grandes volúmenes de números enteros.
* Claves con longitud limitada.
* Cuando se requiere tiempo casi lineal.

---

## Comparación Rápida

* **Radix Sort**: O(d·n), no comparativo.
* **Counting Sort**: O(n + k), depende del rango.
* **Quick Sort**: O(n log n), comparativo.

---

## Idea Clave Final

> Radix Sort es eficiente cuando los **dígitos son pocos y conocidos**.
