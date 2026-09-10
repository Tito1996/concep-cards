# **Clase** vs **Interfaz** vs **Clase Abstracta**

---

## Clase

### ¿Qué es?

Una **clase** es una plantilla completa para crear objetos. Define **atributos, métodos y comportamiento** concreto.

### Características Clave

* Puede instanciarse directamente.
* Contiene métodos **implementados**.
* Puede tener atributos con estado.

### Ejemplo

```java
class Persona {
    String nombre;
    void saludar() {
        System.out.println("Hola");
    }
}
```

---

## Clase Abstracta

### ¿Qué es?

Una **clase abstracta** es una clase incompleta que **no puede instanciarse** y sirve como base para otras clases.

### Características Clave

* Puede tener métodos **abstractos y concretos**.
* Puede tener atributos.
* Usa **herencia** (`extends`).

### Ejemplo

```java
abstract class Animal {
    abstract void hacerSonido();
}
```

---

## Interfaz

### ¿Qué es?

Una **interfaz** define un **contrato** que una clase debe cumplir, sin indicar cómo se implementa.

### Características Clave

* Solo declara métodos (y constantes).
* No tiene estado.
* Una clase puede implementar **múltiples interfaces**.

### Ejemplo

```java
interface Volador {
    void volar();
}
```

---

## Diferencias Principales

| Clase               | Clase Abstracta                | Interfaz                |
| ------------------- | ------------------------------ | ----------------------- |
| Se puede instanciar | No se puede instanciar         | No se puede instanciar  |
| Métodos concretos   | Métodos abstractos y concretos | Métodos abstractos      |
| Herencia simple     | Herencia simple                | Implementación múltiple |
| Tiene estado        | Tiene estado                   | No tiene estado         |

---

## Cuándo Usar Cada Una

* **Clase**: cuando el comportamiento está completamente definido.
* **Clase abstracta**: cuando se quiere compartir código base.
* **Interfaz**: cuando se define un contrato común entre clases no relacionadas.

---

## Idea Clave

> **Clase** = implementación completa.
> **Clase abstracta** = base con partes incompletas.
> **Interfaz** = contrato sin implementación.
