# **Diccionarios / Mapas (Maps)**

---

## ¿Qué son?

Un **diccionario** o **mapa** es una estructura de datos que almacena información en **pares clave–valor**, donde cada clave es única y permite acceder rápidamente a su valor asociado.

---

## Idea Clave

> Se accede al valor **mediante una clave**, no por posición.

---

## Características Principales

* Claves **únicas**.
* Acceso rápido a los datos.
* No mantienen orden (salvo implementaciones específicas).
* Permiten búsqueda, inserción y eliminación eficientes.

---

## Operaciones Básicas

* **Insertar** (put)
* **Obtener** (get)
* **Actualizar**
* **Eliminar** (remove)
* **Buscar por clave**

---

## Ejemplos por Lenguaje

### Java

```java
Map<String, Integer> edades = new HashMap<>();
edades.put("Ana", 20);
int edad = edades.get("Ana");
```

### Python

```python
edades = {"Ana": 20}
edad = edades["Ana"]
```

---

## Implementaciones Comunes

### Java

* **HashMap**: rápido, sin orden.
* **TreeMap**: ordenado por clave.
* **LinkedHashMap**: mantiene orden de inserción.

### Otros Lenguajes

* Python: `dict`
* JavaScript: `Object` / `Map`
* C#: `Dictionary`

---

## Ventajas

* Acceso eficiente a datos.
* Ideal para búsquedas y asociaciones.
* Flexible y ampliamente utilizada.

---

## Desventajas

* Mayor consumo de memoria.
* No adecuado para accesos secuenciales.

---

## Cuándo Usarlos

* Búsquedas rápidas por identificador.
* Asociaciones clave–valor.
* Conteos, cachés y configuraciones.

---

## Comparación Rápida

* **Lista**: acceso por índice.
* **Mapa**: acceso por clave.

---

## Idea Clave Final

> Los diccionarios permiten **acceso rápido y directo** a los datos mediante claves.
