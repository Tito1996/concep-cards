# Patrón de Diseño **Bridge**

**Tipo:** Estructural

---

## ¿Qué es?

El patrón **Bridge** desacopla una **abstracción** de su **implementación**, permitiendo que ambas evolucionen de forma independiente.

---

## Intención

* Evitar una explosión de subclases.
* Separar lo que hace un objeto de cómo lo hace.
* Permitir cambios independientes en abstracción e implementación.

---

## Idea Clave

> La abstracción **contiene una referencia** a la implementación, no la hereda.

---

## Estructura Básica

* **Abstraction**: define la interfaz de alto nivel.
* **Refined Abstraction**: extiende la abstracción.
* **Implementor**: interfaz de implementación.
* **Concrete Implementor**: implementaciones concretas.

---

## Ejemplo (Java)

```java
interface Dispositivo {
    void encender();
    void apagar();
}

class TV implements Dispositivo {
    public void encender() { System.out.println("TV encendida"); }
    public void apagar() { System.out.println("TV apagada"); }
}

abstract class ControlRemoto {
    protected Dispositivo dispositivo;

    ControlRemoto(Dispositivo dispositivo) {
        this.dispositivo = dispositivo;
    }

    abstract void encender();
}

class ControlBasico extends ControlRemoto {
    ControlBasico(Dispositivo dispositivo) { super(dispositivo); }
    void encender() { dispositivo.encender(); }
}
```

---

## Cuándo Usarlo

* Cuando se necesitan múltiples combinaciones de abstracciones e implementaciones.
* Cuando se quiere extender clases sin afectar a otras.
* En sistemas multiplataforma.

---

## Ventajas

* Alta flexibilidad.
* Menor acoplamiento.
* Fácil extensión.

## Desventajas

* Mayor complejidad inicial.
* Más clases en el diseño.

---

## Comparación Rápida

* **Bridge**: separa abstracción e implementación.
* **Adapter**: adapta interfaces existentes.
* **Decorator**: añade comportamiento dinámico.
