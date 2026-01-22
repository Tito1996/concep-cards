## 🧠 TARJETA DE ESTUDIO – `equals()` y `hashCode()` (JAVA) (A6)

### ¿Qué son `equals()` y `hashCode()`?
Son métodos de `Object` que definen **cómo se compara un objeto** y **cómo se identifica en estructuras hash**.

En simple:
👉 *`equals()` dice si dos objetos son “iguales”*  
👉 *`hashCode()` ayuda a ubicarlos rápidamente en memoria*

---

### ¿Por qué sobrescribirlos?
Porque por defecto:
- `equals()` compara **referencias**, no contenido
- `hashCode()` se basa en la identidad del objeto

Si tu objeto representa un **valor lógico** (usuario, producto, etc.):
👉 **debes definir qué significa que dos objetos sean iguales**.

---

### Regla fundamental (entrevista 🚨)
> **Si sobrescribes `equals()`, debes sobrescribir `hashCode()`**

Si no lo haces:
- Las colecciones hash **se rompen**
- Aparecen bugs difíciles de detectar

---

### Relación con `HashMap` y `HashSet`
Estas estructuras usan:
1. `hashCode()` → para ubicar el objeto
2. `equals()` → para confirmar igualdad

Problema típico:
- `equals()` dice que dos objetos son iguales
- pero `hashCode()` es distinto  
👉 el objeto **no se encuentra**, aunque “exista”

Esto **descarta candidatos mid**.

---

### ¿En qué basarlos?
Buenas prácticas:
- Usar **campos inmutables**
- Evitar campos que cambian con el tiempo
- Normalmente usar el **identificador lógico**

Cuidado con:
🚨 campos mutables dentro de `hashCode()`

---

### Error común de junior
- No sobrescribirlos
- Sobrescribir solo uno
- Usar todos los campos “por las dudas”
- Basarlos en estado mutable

---

### Idea clave de entrevista
> “Un mal `equals()` / `hashCode()` rompe colecciones y genera bugs silenciosos.”

---

### Frase que suma muchos puntos
> “`HashMap` y `HashSet` dependen de `hashCode()` y `equals()` para funcionar correctamente.”

---
