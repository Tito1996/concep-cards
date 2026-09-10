# TARJETA DE ESTUDIO – `Map` en Java


## 📌 ¿Qué es `Map`?

`Map` es una **interfaz** del *Java Collections Framework* que representa una **estructura clave–valor**.

✔ Cada **clave es única**
✔ Cada clave apunta a **un solo valor**
❌ No es una `Collection`

---

## 🧱 Implementaciones Principales

### `HashMap`

* Basada en **hashing**
* **No mantiene orden**
* Operaciones rápidas (`O(1)` promedio)

📍 Uso general más común

---

### `LinkedHashMap`

* Mantiene **orden de inserción**
* Rendimiento similar a `HashMap`

📍 Útil cuando el orden importa

---

### `TreeMap`

* Mantiene claves **ordenadas**
* Basada en **árbol balanceado**
* Operaciones `O(log n)`

📍 Requiere claves comparables

---

## 🔄 Operaciones Comunes

* `put(key, value)`
* `get(key)`
* `remove(key)`
* `containsKey(key)`
* `containsValue(value)`
* `size()`

✔ Acceso rápido por clave
❌ No acceso por índice

---

## 🧠 Iteración

* `keySet()` → claves
* `values()` → valores
* `entrySet()` → clave + valor (recomendado)

```java
for (Map.Entry<K,V> e : map.entrySet()) {}
```

---

## ⚠️ Consideraciones Importantes

* Las claves dependen de `equals()` y `hashCode()`
* `HashMap` permite una clave `null`
* No es thread-safe por defecto
* Reemplaza el valor si la clave ya existe

---

## 🎯 Buenas Prácticas

* Programar contra la **interfaz**: `Map<K,V> m = new HashMap<>();`
* Usar `entrySet()` para iterar
* Implementar bien `equals/hashCode`
* Elegir implementación según orden y rendimiento
* Considerar mapas inmutables cuando aplique

---

## 📝 Nota para Full Stack

* Muy usado para DTOs, caches y configuraciones
* Ideal para búsquedas rápidas por identificador
* Frecuente en servicios y lógica backend

---

**Tip:**
Si necesitas **buscar por clave**, usa `Map`.
Si el orden importa, decide entre `LinkedHashMap` o `TreeMap`.
