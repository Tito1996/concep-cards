## 🧠 TARJETA DE ESTUDIO – `HashMap` y `HashSet` (JAVA) (A6)

### ¿Qué son `HashMap` y `HashSet`?
Son **estructuras de datos basadas en hash**, pensadas para **búsquedas rápidas**.

- **`HashMap`** → almacena pares **clave → valor**
- **`HashSet`** → almacena **valores únicos**, sin duplicados

Idea simple:
👉 *usan un “hash” para encontrar datos rápido.*

---

### `HashMap`
Se usa cuando:
- Necesitas acceder a un valor a partir de una **clave**
- La búsqueda debe ser rápida
- La clave es única

Características:
- No permite claves duplicadas
- Permite valores duplicados
- El orden **no está garantizado**

Ejemplo conceptual:
👉 usuarioId → usuario

---

### `HashSet`
Se usa cuando:
- Necesitas **evitar duplicados**
- Solo importa si el elemento existe o no
- No necesitas acceder por índice

Características:
- No permite duplicados
- No mantiene orden
- Muy rápido para `contains`

Ejemplo conceptual:
👉 lista de emails únicos

---

### Clave de entrevista 🚨
> `HashMap` y `HashSet` dependen de `hashCode()` y `equals()`

Funcionan así:
1. Usan `hashCode()` para ubicar el objeto
2. Usan `equals()` para confirmar igualdad

Si estos métodos están mal implementados:
👉 aparecen bugs silenciosos.

---

### Errores comunes en entrevistas
- Usar `HashSet` con objetos sin `equals/hashCode`
- Pensar que mantiene el orden
- Usar `HashMap` cuando una lista alcanza
- Modificar campos usados en `hashCode()`

---

### ¿Cuándo NO usarlos?
- Si necesitas orden → usar `List` o estructuras ordenadas
- Si el tamaño es pequeño y solo recorres → una lista puede ser suficiente

---

### Buena práctica
- Usar `HashMap` para búsquedas por clave
- Usar `HashSet` para evitar duplicados
- Asegurar `equals()` y `hashCode()` correctos

---

### Frase que suma puntos
> “`HashMap` y `HashSet` son rápidos, pero solo funcionan bien si `equals()` y `hashCode()` están bien definidos.”

---
