**TARJETA DE ESTUDIO – Mutabilidad e Inmutabilidad en Java**

---

## 📌 ¿Qué es la Mutabilidad?

Define si un objeto **puede cambiar su estado interno** después de ser creado.

- **Mutable** → su estado puede modificarse  
- **Inmutable** → su estado no cambia; se crea uno nuevo

---

## 🧱 Ejemplos en Java

### 🔒 Objetos Inmutables
- `String`
- `Integer`, `Long`
- `LocalDate`, `LocalDateTime`

```java
String s = "Hola";
s = s.concat(" Mundo"); // crea un nuevo objeto
````

---

### 🔓 Objetos Mutables

* `ArrayList`
* `HashMap`
* Clases propias con setters

```java
list.add("item"); // modifica el mismo objeto
```

---

## ⚠️ Impacto Real

* **Bugs**: cambios inesperados de estado
* **Legibilidad**: código difícil de razonar
* **Concurrencia**: riesgo de condiciones de carrera

---

## 🎯 Buenas Prácticas (Nivel Mid)

* Preferir **inmutabilidad por defecto**
* Usar `final` siempre que sea posible
* Evitar setters innecesarios
* Crear nuevos objetos en vez de modificar existentes

---

## 🧪 Señal de Entrevista

> “¿Este objeto realmente necesita cambiar?”

---

## 🧠 Regla Mental

**Si no debe cambiar, hazlo inmutable**`
