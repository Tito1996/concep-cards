## TARJETA DE ESTUDIO – Manejo Básico de Errores en Java**

---

## 📌 ¿Qué es el Manejo de Errores?

Consiste en **anticipar fallos**, **controlarlos** y **responder de forma segura** cuando algo no sale como se espera.

Un programa correcto **no es el que nunca falla**, sino el que **falla bien**.

---

## 🧱 Tipos de Errores en Java

### ❌ Excepciones Comunes
- `NullPointerException`
- `IllegalArgumentException`
- `IndexOutOfBoundsException`

---

### ⚙️ Checked vs Unchecked
- **Checked** → deben manejarse (`IOException`)
- **Unchecked** → errores de lógica (`RuntimeException`)

---

## 🛠️ Herramientas del Lenguaje

### try / catch
```java
try {
    service.process(data);
} catch (IllegalArgumentException e) {
    log.error(e.getMessage());
}
````

---

### Validación de Entradas

```java
if (input == null) {
    throw new IllegalArgumentException("Input inválido");
}
```

---

## ⚠️ Errores Comunes

* Capturar `Exception` genérica
* Ignorar excepciones
* Usar excepciones para control de flujo
* Mensajes poco claros

---

## 🎯 Buenas Prácticas (Nivel Mid)

* Validar antes de ejecutar lógica
* Fallar rápido (*fail fast*)
* Usar excepciones específicas
* Mensajes claros y útiles

---

## 🧪 Señal de Entrevista

> “¿Qué pasa si esto falla?”

---

## 🧠 Regla Mental

**Anticipar errores es parte del diseño**
