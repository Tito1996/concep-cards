# Patrón de Diseño **Prototype**

**Tipo:** Creacional

---

## ¿Qué es?

El patrón **Prototype** permite crear nuevos objetos **clonando una instancia existente**, en lugar de crear objetos desde cero.

---

## Intención

* Evitar el costo de creación de objetos complejos.
* Crear objetos sin depender de sus clases concretas.
* Facilitar la creación de copias configuradas previamente.

---

## Idea Clave

> En lugar de instanciar, **se clona** un objeto prototipo.

---

## Estructura Básica

* **Prototype**: interfaz que declara el método de clonación.
* **Concrete Prototype**: implementa la clonación.
* **Cliente**: solicita la clonación del prototipo.

---

## Ejemplo (Java)

```java
interface Figura extends Cloneable {
    Figura clonar();
}

class Circulo implements Figura {
    int radio;

    Circulo(int radio) {
        this.radio = radio;
    }

    public Figura clonar() {
        return new Circulo(this.radio);
    }
}
```

---

## Cuándo Usarlo

* Cuando la creación de objetos es costosa.
* Cuando se requiere duplicar objetos en tiempo de ejecución.
* Cuando se quiere evitar una jerarquía compleja de fábricas.

---

## Ventajas

* Mejora el rendimiento.
* Reduce dependencias de clases concretas.
* Permite crear copias personalizadas.

## Desventajas

* Clonación profunda puede ser compleja.
* Manejo cuidadoso de referencias internas.

---

## Comparación Rápida

* **Prototype**: crea objetos clonando.
* **Builder**: construye paso a paso.
* **Factory**: crea instancias nuevas.
