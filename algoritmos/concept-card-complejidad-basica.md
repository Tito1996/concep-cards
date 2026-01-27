# **Complejidad Algorítmica (Big O)**

---

## ¿Qué es Big O?

La **notación Big O** describe cómo **crece el tiempo o espacio de ejecución** de un algoritmo en función del tamaño de la entrada (*n*).

---

## O(1) — Tiempo Constante

### Concepto

El tiempo de ejecución **no depende** del tamaño de la entrada.

### Ejemplo

* Acceder a un elemento de un array por índice.

```java
int valor = array[0];
```

### Idea Clave

> Siempre tarda lo mismo.

---

## O(n) — Tiempo Lineal

### Concepto

El tiempo de ejecución **crece proporcionalmente** al tamaño de la entrada.

### Ejemplo

* Recorrer una lista completa.

```java
for (int i = 0; i < n; i++) {
    System.out.println(lista[i]);
}
```

### Idea Clave

> A más datos, más tiempo.

---

## O(n²) — Tiempo Cuadrático

### Concepto

El tiempo de ejecución **crece al cuadrado** del tamaño de la entrada.

### Ejemplo

* Bucles anidados.

```java
for (int i = 0; i < n; i++) {
    for (int j = 0; j < n; j++) {
        System.out.println(i + j);
    }
}
```

### Idea Clave

> Crece muy rápido con entradas grandes.

---

## Comparación Visual

| Complejidad | Crecimiento |
| ----------- | ----------- |
| O(1)        | Constante   |
| O(n)        | Lineal      |
| O(n²)       | Cuadrático  |

---

## Cuándo Aparecen

* **O(1)**: accesos directos, variables.
* **O(n)**: recorridos simples.
* **O(n²)**: comparaciones dobles, algoritmos simples de ordenación.

---

## Idea Clave Final

> Big O mide **cómo escala un algoritmo**, no su tiempo exacto.
