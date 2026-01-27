# **Análisis Amortizado**

---

## ¿Qué es?

El **análisis amortizado** evalúa el **costo promedio real** de una secuencia de operaciones, incluso si algunas operaciones individuales son costosas.

---

## Idea Clave

> Operaciones caras ocurren **pocas veces** y su costo se **reparte** entre muchas operaciones baratas.

---

## ¿Por qué es Necesario?

* El peor caso no siempre representa el uso real.
* Permite entender el **rendimiento a largo plazo**.

---

## Métodos de Análisis Amortizado

### 1️⃣ Método Agregado

* Se calcula el costo total de *n* operaciones.
* Se divide entre *n*.

### 2️⃣ Método del Contador

* Algunas operaciones pagan un costo extra.
* Ese crédito cubre operaciones futuras caras.

### 3️⃣ Método del Potencial

* Se define una función de **energía/potencial**.
* El cambio de potencial paga operaciones costosas.

---

## Ejemplo Clásico: Array Dinámico

### Operaciones

* Inserción normal → O(1)
* Redimensionar (copiar) → O(n)

### Análisis

* La redimensión ocurre raramente.
* Costo amortizado por inserción → **O(1)**

---

## Ejemplo: Pila con Multipop

* `push` → O(1)
* `pop` → O(1)
* `multipop(k)` → O(k)

➡ Amortizado: **O(1)** por operación

---

## Comparación de Casos

| Tipo       | Qué mide         |
| ---------- | ---------------- |
| Mejor caso | Escenario ideal  |
| Peor caso  | Escenario máximo |
| Amortizado | Promedio real    |

---

## Cuándo Usarlo

* Estructuras dinámicas.
* Operaciones ocasionalmente costosas.
* Diseño de estructuras eficientes.

---

## Ventajas

* Refleja uso real.
* Permite diseños eficientes.
* Reduce falsos peores casos.

---

## Error Común

* Confundir **amortizado** con **promedio estadístico**.

---

## Idea Clave Final

> Aunque una operación sea cara, el sistema puede ser **eficiente en conjunto**.
