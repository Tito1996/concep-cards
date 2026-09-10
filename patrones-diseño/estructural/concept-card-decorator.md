# Patrón de Diseño **Decorator**

**Tipo:** Estructural

---

## ¿Qué es?

El patrón **Decorator** permite **añadir responsabilidades o comportamientos a un objeto de forma dinámica**, sin modificar su clase original.

---

## Intención

* Extender funcionalidades sin usar herencia.
* Mantener el código abierto a extensión y cerrado a modificación.
* Combinar comportamientos de manera flexible.

---

## Idea Clave

> En lugar de heredar, se **envuelve** el objeto con decoradores.

---

## Estructura Básica

* **Component**: interfaz común.
* **Concrete Component**: objeto base.
* **Decorator**: clase abstracta que envuelve al componente.
* **Concrete Decorators**: añaden comportamientos adicionales.

---

## Ejemplo (Java)

```java
interface Cafe {
    String descripcion();
    double costo();
}

class CafeSimple implements Cafe {
    public String descripcion() { return "Café simple"; }
    public double costo() { return 1.50; }
}

abstract class CafeDecorator implements Cafe {
    protected Cafe cafe;
    CafeDecorator(Cafe cafe) { this.cafe = cafe; }
}

class Leche extends CafeDecorator {
    Leche(Cafe cafe) { super(cafe); }
    public String descripcion() { return cafe.descripcion() + ", leche"; }
    public double costo() { return cafe.costo() + 0.50; }
}
```

---

## Cuándo Usarlo

* Cuando se necesitan combinaciones dinámicas de comportamientos.
* Cuando la herencia genera muchas subclases.
* Cuando se quiere modificar objetos en tiempo de ejecución.

---

## Ventajas

* Alta flexibilidad.
* Cumple el principio abierto/cerrado.
* Evita jerarquías complejas.

## Desventajas

* Puede generar muchos objetos pequeños.
* Difícil de depurar en estructuras muy anidadas.

---

## Comparación Rápida

* **Decorator**: añade comportamiento dinámicamente.
* **Adapter**: adapta interfaces.
* **Facade**: simplifica el acceso a un sistema complejo.
