# TARJETA DE ESTUDIO – Colecciones en Java


## 📌 ¿Qué son las Colecciones?

Las **colecciones** en Java son **estructuras de datos** que permiten **almacenar, organizar y manipular grupos de objetos** de forma eficiente.

Forman parte del **Java Collections Framework**.

---

## 🧱 Interfaces Principales

### 📋 List

Colección **ordenada** que permite **elementos duplicados**.

* `ArrayList` → acceso rápido por índice
* `LinkedList` → inserciones/eliminaciones frecuentes

✔ Mantiene orden
✔ Acceso por posición

---

### 🧺 Set

Colección **sin elementos duplicados**.

* `HashSet` → rápido, sin orden
* `LinkedHashSet` → mantiene orden de inserción
* `TreeSet` → ordenado automáticamente

✔ Garantiza unicidad
❌ No acceso por índice

---

### 🗺️ Map

Estructura **clave–valor**.

* `HashMap` → rápido, sin orden
* `LinkedHashMap` → mantiene orden
* `TreeMap` → ordenado por clave

✔ Búsqueda eficiente por clave
❌ No es una Collection directa

---

## 🔄 Iteración

* `for-each`
* `Iterator`
* `Stream API`

✔ Streams permiten filtros y transformaciones funcionales

---

## 🧠 Comparación Rápida

* **List:** orden + duplicados
* **Set:** sin duplicados
* **Map:** clave–valor

---

## ⚠️ Errores Comunes

* Usar `List` cuando se necesita unicidad
* Usar `Map` sin sobrescribir `equals()` y `hashCode()`
* Modificar colecciones mientras se iteran incorrectamente
* No elegir la implementación adecuada

---

## 🎯 Buenas Prácticas

* Programar contra **interfaces**, no implementaciones
* Elegir la colección según el caso de uso
* Usar genéricos (`List<String>`)
* Preferir `Collections.unmodifiable*` cuando aplique

---

## 📝 Nota para Full Stack

* Muy usadas en backend Java (APIs, servicios)
* Clave para manejar datos desde bases de datos
* Impactan directamente en rendimiento y memoria

---

**Tip:**
Elegir mal una colección puede convertir un buen algoritmo en un problema de rendimiento.
