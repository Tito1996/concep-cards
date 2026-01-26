# Patrón de Diseño **Facade**

**Tipo:** Estructural

---

## ¿Qué es?

El patrón **Facade** proporciona una **interfaz simplificada** para un sistema complejo de clases, librerías o subsistemas.

---

## Intención

* Reducir la complejidad para el cliente.
* Desacoplar el cliente de los subsistemas internos.
* Facilitar el uso de sistemas complejos.

---

## Idea Clave

> El cliente interactúa con una **fachada**, no con el sistema completo.

---

## Estructura Básica

* **Facade**: interfaz de alto nivel que coordina el subsistema.
* **Subsistemas**: clases complejas que realizan el trabajo real.
* **Cliente**: usa únicamente la fachada.

---

## Ejemplo (Java)

```java
class CPU {
    void iniciar() { System.out.println("CPU iniciada"); }
}

class Memoria {
    void cargar() { System.out.println("Memoria cargada"); }
}

class DiscoDuro {
    void leer() { System.out.println("Disco duro leyendo datos"); }
}

class ComputadoraFacade {
    private CPU cpu = new CPU();
    private Memoria memoria = new Memoria();
    private DiscoDuro disco = new DiscoDuro();

    void iniciar() {
        cpu.iniciar();
        memoria.cargar();
        disco.leer();
    }
}
```

---

## Cuándo Usarlo

* Cuando un sistema es complejo o difícil de usar.
* Cuando se quiere reducir dependencias.
* Para crear un punto de entrada claro a un subsistema.

---

## Ventajas

* Uso sencillo del sistema.
* Menor acoplamiento.
* Código cliente más limpio.

## Desventajas

* La fachada puede crecer demasiado.
* Puede ocultar funcionalidades avanzadas.

---

## Comparación Rápida

* **Facade**: simplifica el acceso a un sistema.
* **Adapter**: adapta interfaces incompatibles.
* **Decorator**: añade comportamiento dinámico.
