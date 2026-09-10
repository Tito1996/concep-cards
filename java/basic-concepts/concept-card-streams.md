# TARJETA DE ESTUDIO – Streams y Programación Funcional en Java


## 📌 ¿Qué son los Streams?

Los **Streams** en Java son una **abstracción para procesar colecciones de datos** de forma **declarativa, funcional y eficiente**, introducida en Java 8.

❌ No almacenan datos
✔ Procesan datos de colecciones, arrays o I/O

---

## 🧠 Programación Funcional (En Java)

Paradigma basado en:

* **Funciones puras**
* **Inmutabilidad**
* **Expresiones lambda**
* **Operaciones declarativas**

📍 Java combina OOP + funcional (no es 100% funcional)

---

## 🧱 Flujo de un Stream

**Fuente → Operaciones intermedias → Operación terminal**

Ejemplo mental:

```
colección → filter → map → collect
```

---

## 🔄 Operaciones Intermedias

Devuelven otro Stream (lazy).

* `filter()` → filtra elementos
* `map()` → transforma elementos
* `sorted()` → ordena
* `distinct()` → elimina duplicados
* `limit()` / `skip()`

✔ No se ejecutan hasta una operación terminal

---

## 🏁 Operaciones Terminales

Ejecutan el Stream.

* `forEach()`
* `collect()`
* `count()`
* `findFirst()`
* `anyMatch()`, `allMatch()`
* `reduce()`

✔ Consumen el Stream (no reutilizable)

---

## 🔧 Lambdas (Base de Streams)

```java
x -> x * 2
```

✔ Código más conciso
✔ Menos boilerplate
✔ Mayor expresividad

---

## 🎯 Beneficios Clave

* Código más legible
* Menos errores imperativos
* Fácil paralelización (`parallelStream`)
* Ideal para transformaciones de datos

---

## ⚠️ Errores Comunes

* Usar Streams para lógica compleja
* Abusar de `parallelStream`
* Modificar estado externo
* Olvidar que los Streams son lazy

---

## 🎯 Buenas Prácticas

* Streams para **transformar datos**, no para control de flujo
* Preferir claridad sobre cadenas largas
* Mantener lambdas simples
* Usar `Collectors` estándar

---

## 📝 Nota para Full Stack

* Muy usados en servicios y repositorios Java
* Frecuentes al procesar datos de base de datos
* Mejoran legibilidad y mantenibilidad del backend

---

**Tip:**
Si tu código tiene muchos `for` y `if` para procesar listas, probablemente un **Stream** lo puede expresar mejor.
