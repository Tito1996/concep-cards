# Patrón de Diseño **Builder**

**Tipo:** Creacional

---

## ¿Qué es?

El patrón **Builder** separa la **construcción de un objeto complejo** de su representación final, permitiendo crear distintos tipos y configuraciones del mismo objeto paso a paso.

---

## Intención

* Construir objetos complejos de forma controlada.
* Evitar constructores con muchos parámetros.
* Permitir diferentes representaciones usando el mismo proceso de construcción.

---

## Idea Clave

> El mismo proceso de construcción puede crear **distintas versiones** de un objeto.

---

## Estructura Básica

* **Builder**: define los pasos para construir el objeto.
* **Concrete Builder**: implementa los pasos y ensambla el objeto.
* **Producto**: objeto complejo que se construye.
* **Director** (opcional): controla el orden de construcción.

---

## Ejemplo (Java)

```java
class Casa {
    String paredes;
    String techo;
    String puertas;
}

interface CasaBuilder {
    void construirParedes();
    void construirTecho();
    void construirPuertas();
    Casa getCasa();
}

class CasaConcretaBuilder implements CasaBuilder {
    private Casa casa = new Casa();

    public void construirParedes() { casa.paredes = "Ladrillo"; }
    public void construirTecho() { casa.techo = "Teja"; }
    public void construirPuertas() { casa.puertas = "Madera"; }
    public Casa getCasa() { return casa; }
}
```

---

## Cuándo Usarlo

* Cuando un objeto tiene muchas partes opcionales.
* Cuando el orden de construcción es importante.
* Cuando se necesitan múltiples representaciones del mismo objeto.

---

## Ventajas

* Construcción clara y paso a paso.
* Mayor legibilidad y mantenimiento.
* Evita constructores largos y confusos.

## Desventajas

* Incrementa el número de clases.
* Puede ser excesivo para objetos simples.

---

## Comparación Rápida

* **Builder**: construye objetos complejos paso a paso.
* **Factory**: crea objetos en una sola operación.
* **Abstract Factory**: crea familias de objetos relacionados.
