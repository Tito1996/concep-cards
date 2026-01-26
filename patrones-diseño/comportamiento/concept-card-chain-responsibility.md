# Patrón de Diseño **Chain of Responsibility**

**Tipo:** Comportamiento

---

## ¿Qué es?

El patrón **Chain of Responsibility** permite **pasar una solicitud a lo largo de una cadena de manejadores**, donde cada uno decide si procesa la solicitud o la delega al siguiente.

---

## Intención

* Desacoplar el emisor de una solicitud de sus receptores.
* Permitir múltiples manejadores para una misma solicitud.
* Evitar dependencias rígidas entre cliente y receptor.

---

## Idea Clave

> La solicitud **recorre una cadena** hasta que algún manejador la procesa.

---

## Estructura Básica

* **Handler**: define la interfaz para manejar solicitudes.
* **Concrete Handlers**: procesan la solicitud o la pasan al siguiente.
* **Cliente**: inicia la solicitud.

---

## Ejemplo (Java)

```java
abstract class Soporte {
    protected Soporte siguiente;

    void setSiguiente(Soporte siguiente) {
        this.siguiente = siguiente;
    }

    abstract void manejar(int nivel);
}

class SoporteBasico extends Soporte {
    void manejar(int nivel) {
        if (nivel <= 1) {
            System.out.println("Soporte básico resuelve el problema");
        } else if (siguiente != null) {
            siguiente.manejar(nivel);
        }
    }
}

class SoporteAvanzado extends Soporte {
    void manejar(int nivel) {
        if (nivel <= 2) {
            System.out.println("Soporte avanzado resuelve el problema");
        } else if (siguiente != null) {
            siguiente.manejar(nivel);
        }
    }
}
```

---

## Cuándo Usarlo

* Cuando hay múltiples objetos que pueden manejar una solicitud.
* Cuando el manejador exacto no se conoce de antemano.
* En validaciones, flujos de aprobación o pipelines.

---

## Ventajas

* Bajo acoplamiento.
* Flexibilidad para añadir o reordenar manejadores.
* Simplifica el código cliente.

## Desventajas

* No se garantiza que la solicitud sea manejada.
* Puede dificultar el seguimiento del flujo.

---

## Comparación Rápida

* **Chain of Responsibility**: pasa solicitudes por una cadena.
* **Command**: encapsula una acción.
* **Observer**: notifica cambios.
