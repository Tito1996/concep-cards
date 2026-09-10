# Patrón de Diseño **Template Method**

**Tipo:** Comportamiento

---

## ¿Qué es?

El patrón **Template Method** define el **esqueleto de un algoritmo** en una clase base, delegando algunos pasos a las subclases sin cambiar la estructura general.

---

## Intención

* Reutilizar código común entre algoritmos similares.
* Permitir variaciones controladas en ciertos pasos.
* Evitar duplicación de lógica.

---

## Idea Clave

> La clase base define **qué pasos se ejecutan y en qué orden**; las subclases definen **cómo** se ejecutan algunos pasos.

---

## Estructura Básica

* **Abstract Class**: define el método plantilla (`templateMethod`).
* **Primitive Operations**: pasos abstractos u opcionales.
* **Concrete Classes**: implementan los pasos variables.

---

## Ejemplo (Java)

```java
abstract class Bebida {
    // Template Method
    final void preparar() {
        hervirAgua();
        prepararBebida();
        servir();
    }

    void hervirAgua() {
        System.out.println("Hirviendo agua");
    }

    abstract void prepararBebida();

    void servir() {
        System.out.println("Sirviendo bebida");
    }
}

class Te extends Bebida {
    void prepararBebida() {
        System.out.println("Preparando té");
    }
}
```

---

## Cuándo Usarlo

* Cuando varios algoritmos comparten una estructura común.
* Cuando se quiere controlar el orden de ejecución.
* Cuando se necesita extender comportamiento sin modificar la lógica base.

---

## Ventajas

* Alta reutilización de código.
* Control del flujo del algoritmo.
* Facilita mantenimiento.

## Desventajas

* Dependencia fuerte de herencia.
* Menor flexibilidad que la composición.

---

## Comparación Rápida

* **Template Method**: redefine pasos de un algoritmo.
* **Strategy**: intercambia algoritmos completos.
* **State**: cambia comportamiento según el estado.
