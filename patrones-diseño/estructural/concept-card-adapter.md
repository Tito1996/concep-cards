# Patrón de Diseño **Adapter**

**Tipo:** Estructural

---

## ¿Qué es?

El patrón **Adapter** permite que **interfaces incompatibles trabajen juntas**, convirtiendo la interfaz de una clase en otra que el cliente espera.

---

## Intención

* Reutilizar clases existentes con interfaces incompatibles.
* Evitar modificar código ya probado.
* Facilitar la integración entre sistemas o librerías distintas.

---

## Idea Clave

> El Adapter actúa como un **traductor** entre dos interfaces.

---

## Estructura Básica

* **Target**: interfaz esperada por el cliente.
* **Adaptee**: clase existente con interfaz incompatible.
* **Adapter**: adapta la interfaz del Adaptee al Target.
* **Cliente**: usa la interfaz Target.

---

## Ejemplo (Java)

```java
interface EnchufeEuropeo {
    void conectar();
}

class EnchufeAmericano {
    public void plugIn() {
        System.out.println("Conectado a enchufe americano");
    }
}

class AdaptadorEnchufe implements EnchufeEuropeo {
    private EnchufeAmericano enchufe;

    AdaptadorEnchufe(EnchufeAmericano enchufe) {
        this.enchufe = enchufe;
    }

    public void conectar() {
        enchufe.plugIn();
    }
}
```

---

## Cuándo Usarlo

* Cuando se integran sistemas heredados.
* Cuando se usan librerías de terceros.
* Cuando no es posible modificar la clase original.

---

## Ventajas

* Reutilización de código existente.
* Mayor flexibilidad.
* Aisla cambios de implementación.

## Desventajas

* Incrementa el número de clases.
* Puede añadir complejidad innecesaria.

---

## Comparación Rápida

* **Adapter**: adapta interfaces incompatibles.
* **Facade**: simplifica una interfaz compleja.
* **Decorator**: añade comportamiento sin cambiar la interfaz.
