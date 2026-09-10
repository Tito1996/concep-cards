# TARJETA DE ESTUDIO – `Set` en Java


## 📌 ¿Qué es `Set`?

`Set` es una **interfaz** del *Java Collections Framework* que representa una colección **sin elementos duplicados**.

✔ Garantiza **unicidad**
❌ No mantiene acceso por índice

---

## 🧱 Implementaciones Principales

### `HashSet`

* Basada en **hashing**
* **No mantiene orden**
* Operaciones rápidas (`O(1)` promedio)

📍 Ideal para verificar unicidad rápidamente

---

### `LinkedHashSet`

* Mantiene **orden de inserción**
* Rendimiento similar a `HashSet`

📍 Útil cuando importa el orden y la unicidad

---

### `TreeSet`

* Mantiene elementos **ordenados**
* Basado en **árbol balanceado**
* Operaciones `O(log n)`

📍 Requiere elementos comparables (`Comparable` o `Comparator`)

---

## 🔄 Operaciones Comunes

* `add(element)` → ignora duplicados
* `remove(element)`
* `contains(element)`
* `size()`
* `isEmpty()`

---

## 🧠 Iteración

* `for-each`
* `Iterator`
* `Stream API`

✔ No hay acceso por índice

---

## ⚠️ Consideraciones Importantes

* La unicidad depende de `equals()` y `hashCode()`
* Puede permitir `null` (según implementación)
* No es thread-safe por defecto

📍 Implementar correctamente `equals/hashCode` es **crítico**

---

## 🎯 Buenas Prácticas

* Programar contra la **interfaz**: `Set<T> s = new HashSet<>();`
* Elegir implementación según orden y rendimiento
* Usar genéricos
* Preferir `TreeSet` solo si necesitas orden
* Considerar sets inmutables cuando aplique

---

## 📝 Nota para Full Stack

* Muy usado para eliminar duplicados
* Ideal para roles, permisos y catálogos únicos
* Impacta rendimiento y consistencia de datos

---

**Tip:**
Si necesitas **unicidad** → `Set`.
Si además necesitas **orden**, elige entre `LinkedHashSet` o `TreeSet` según el caso.
