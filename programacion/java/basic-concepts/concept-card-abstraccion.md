## TARJETA DE ESTUDIO – Abstracción Básica en Java**

---

## 📌 ¿Qué es la Abstracción?

La **abstracción** consiste en **ocultar detalles innecesarios** y exponer solo lo esencial.

Permite que otros usen tu código **sin conocer su implementación interna**.

---

## 🧱 Formas de Abstracción en Java

### 🔹 Métodos
Encapsulan lógica compleja detrás de un nombre claro.

```java
calculateTotalPrice(order);
````

---

### 🔹 Clases

Agrupan comportamiento relacionado.

```java
class OrderService { }
```

---

### 🔹 Interfaces

Definen **qué se puede hacer**, no **cómo**.

```java
interface PaymentProcessor {
    void pay();
}
```

---

## ⚠️ Señales de Mala Abstracción

* Métodos con demasiadas responsabilidades
* Nombres que explican el “cómo”
* Código duplicado
* Lógica expuesta al consumidor

---

## 🎯 Buenas Prácticas (Nivel Mid)

* Nombres que expliquen **intención**
* Métodos pequeños y enfocados
* Separar responsabilidades
* Ocultar complejidad innecesaria

---

## 🧪 Señal de Entrevista

> “Puedo usar este método sin saber cómo funciona.”

---

## 🧠 Regla Mental

**Expón el qué, oculta el cómo**
