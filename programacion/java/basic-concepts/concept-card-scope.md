## 📌 ¿Qué es el Scope de una Variable?

El **scope** define **dónde existe una variable** y **desde qué partes del código puede ser utilizada**.

Determina:
- Tiempo de vida de la variable
- Quién puede modificarla
- Riesgo de efectos colaterales

---

## 🧱 Tipos de Scope en Java

### 🔹 Scope Local
- Declarada dentro de un método o bloque `{ }`
- Vive solo durante la ejecución del bloque

```java
if (condicion) {
    int total = 10;
}
````

---

### 🔹 Scope de Instancia

* Atributos de una clase
* Cada objeto tiene su propia copia

```java
class User {
    private String name;
}
```

---

### 🔹 Scope de Clase (`static`)

* Compartido por todas las instancias
* Vive mientras la aplicación esté activa

```java
static int counter;
```

---

## ⚠️ Riesgos de un Scope Incorrecto

* Variables accesibles desde demasiados lugares
* Bugs difíciles de rastrear
* Dependencias implícitas
* Código frágil ante cambios

---

## 🎯 Buenas Prácticas (Nivel Mid)

* Usar **el scope más pequeño posible**
* Preferir variables **locales**
* Evitar `static` sin justificación clara
* No reutilizar variables para múltiples propósitos

---

## 🧪 Señal de Entrevista

> “Si una variable vive más tiempo del necesario, su scope es incorrecto.”

---

## 🧠 Regla Mental

**Menor scope = menor complejidad = menos bugs**
