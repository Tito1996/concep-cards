# Patrón de Diseño **Strategy**

**Tipo:** Comportamiento

---

## ¿Qué es?

El patrón **Strategy** define una **familia de algoritmos**, los encapsula y los hace **intercambiables**. Permite cambiar el comportamiento de un objeto en tiempo de ejecución.

---

## Intención

* Seleccionar un algoritmo en tiempo de ejecución.
* Eliminar condicionales extensos (if/else o switch).
* Separar el qué se hace del cómo se hace.

---

## Idea Clave

> El comportamiento se **delegá** a un objeto estrategia, no se codifica directamente en la clase.

---

## Estructura Básica

* **Strategy**: interfaz común para los algoritmos.
* **Concrete Strategies**: implementaciones del algoritmo.
* **Context**: usa una Strategy y delega el comportamiento.

---

## Ejemplo (Java)

```java
interface MetodoPago {
    void pagar(double monto);
}

class PagoTarjeta implements MetodoPago {
    public void pagar(double monto) {
        System.out.println("Pago con tarjeta: " + monto);
    }
}

class PagoPaypal implements MetodoPago {
    public void pagar(double monto) {
        System.out.println("Pago con PayPal: " + monto);
    }
}

class Carrito {
    private MetodoPago metodoPago;

    void setMetodoPago(MetodoPago metodoPago) {
        this.metodoPago = metodoPago;
    }

    void pagar(double monto) {
        metodoPago.pagar(monto);
    }
}
```

---

## Cuándo Usarlo

* Cuando hay múltiples variantes de un algoritmo.
* Cuando el comportamiento debe cambiar dinámicamente.
* Cuando se quiere evitar lógica condicional compleja.

---

## Ventajas

* Alta flexibilidad.
* Código más limpio y mantenible.
* Facilita pruebas unitarias.

## Desventajas

* Incrementa el número de clases.
* El cliente debe conocer las estrategias disponibles.

---

## Comparación Rápida

* **Strategy**: cambia algoritmos.
* **State**: cambia comportamiento según el estado.
* **Command**: encapsula acciones como objetos.
