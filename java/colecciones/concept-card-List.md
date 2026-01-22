# TARJETA DE ESTUDIO – `List` en Java


## 📌 ¿Qué es `List`?

`List` es una **interfaz** del *Java Collections Framework* que representa una **colección ordenada** de elementos y **permite duplicados**.

✔ Mantiene el orden de inserción
✔ Acceso por índice (`get(int)`)

---

## 🧱 Implementaciones Principales

### `ArrayList`

* Basada en **array dinámico**
* Acceso rápido por índice `O(1)`
* Inserciones/eliminaciones intermedias más costosas

📍 Ideal para lecturas frecuentes

---

### `LinkedList`

* Basada en **lista doblemente enlazada**
* Inserciones/eliminaciones rápidas `O(1)`
* Acceso por índice más lento

📍 Ideal para modificaciones frecuentes

---

## 🔄 Operaciones Comunes

* `add(element)` / `add(index, element)`
* `get(index)`
* `set(index, element)`
* `remove(index)`
* `size()`
* `contains(element)`

---

## 🧠 Iteración

* `for-each`
* `Iterator`
* `Stream API` (map, filter, collect)

✔ Streams permiten programación funcional y código más limpio

---

## ⚠️ Consideraciones Importantes

* Permite `null` (según implementación)
* No garantiza sincronización (no thread-safe)
* El rendimiento depende de la implementación elegida

---

## 🎯 Buenas Prácticas

* Programar contra la **interfaz**: `List<String> lista = new ArrayList<>();`
* Elegir implementación según el uso
* Usar **genéricos**
* Evitar modificar la lista durante iteración sin `Iterator`
* Considerar listas inmutables cuando aplique

---

## 📝 Nota para Full Stack

* Muy usadas en servicios y APIs Java
* Frecuentes al mapear resultados de bases de datos
* Impactan rendimiento y consumo de memoria

---

**Tip:**
Si necesitas acceso rápido por índice, usa `ArrayList`.
Si necesitas insertar y eliminar mucho, considera `LinkedList`.
