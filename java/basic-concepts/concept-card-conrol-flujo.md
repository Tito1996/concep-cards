**TARJETA DE ESTUDIO – Control del Flujo de Ejecución en Java**

---

## 📌 ¿Qué es el Control del Flujo?

Define **el orden en el que se ejecutan las instrucciones** de un programa.

No se trata solo de que el código funcione, sino de que sea:
- Fácil de leer
- Fácil de razonar
- Fácil de mantener

---

## 🧱 Herramientas Clave

### 🔁 Condiciones y Bucles
- `if / else`
- `switch`
- `for`, `while`, `do-while`

---

### 🚪 Return Temprano
Permite salir antes de un método cuando una condición no se cumple.

```java
if (user == null) return;
````

✔ Reduce anidaciones
✔ Mejora legibilidad

---

### ⛔ break y continue

* `break` → corta el bucle
* `continue` → salta a la siguiente iteración

Usarlos con moderación y claridad.

---

## ⚠️ Errores Comunes

* Exceso de `if` anidados
* Métodos largos y difíciles de seguir
* Lógica mezclada (validación + negocio)

---

## 🎯 Buenas Prácticas (Nivel Mid)

* Priorizar **return temprano**
* Mantener métodos cortos
* Ordenar el código de forma lógica
* Evitar flujos “sorpresa”

---

## 🧪 Señal de Entrevista

> “El código se lee de arriba hacia abajo sin esfuerzo.”

---

## 🧠 Regla Mental

**Código fácil de seguir > código ingenioso**
