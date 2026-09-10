# **Recurrencias y Teorema Maestro**

---

## ¿Qué es una recurrencia?

Una **recurrencia** expresa el **costo de un algoritmo recursivo** en función del tamaño de la entrada (*n*) y de subproblemas más pequeños.

---

## Forma General

**T(n) = a · T(n / b) + f(n)**

* **a**: número de subproblemas
* **b**: factor de reducción del tamaño
* **f(n)**: trabajo fuera de la recursión

---

## Ejemplos Comunes

* **Búsqueda binaria**:

  * T(n) = T(n/2) + O(1)

* **Merge Sort**:

  * T(n) = 2T(n/2) + O(n)

* **Quick Sort (promedio)**:

  * T(n) = 2T(n/2) + O(n)

---

## Teorema Maestro

Se usa para resolver recurrencias de la forma:

**T(n) = aT(n/b) + f(n)**

Comparando **f(n)** con **n^{log_b a}**.

---

## Casos del Teorema Maestro

### Caso 1

* f(n) = O(n^{log_b a − ε})
* **Resultado**: T(n) = Θ(n^{log_b a})

### Caso 2

* f(n) = Θ(n^{log_b a})
* **Resultado**: T(n) = Θ(n^{log_b a} · log n)

### Caso 3

* f(n) = Ω(n^{log_b a + ε})
* **Resultado**: T(n) = Θ(f(n))

---

## Ejemplo Resuelto

**Merge Sort**:

* a = 2, b = 2 → n^{log₂2} = n
* f(n) = n

➡ Caso 2 → **T(n) = Θ(n log n)**

---

## Cuándo Usarlo

* Algoritmos recursivos.
* Divide y vencerás.
* Análisis formal de complejidad.

---

## Limitaciones

* No aplica a todas las recurrencias.
* No sirve para divisiones irregulares.

---

## Idea Clave Final

> El Teorema Maestro permite resolver **rápidamente** la complejidad de muchos algoritmos recursivos.
