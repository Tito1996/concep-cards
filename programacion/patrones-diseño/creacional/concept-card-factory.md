# Patrón de Diseño **Factory**

**Tipo:** Creacional

---

## ¿Qué es?

El patrón **Factory** define una **interfaz para crear objetos**, pero permite que las **subclases decidan** qué clase concreta instanciar. Desacopla la creación del objeto de su uso.

---

## Intención

* Encapsular la lógica de creación de objetos.
* Reducir el acoplamiento entre el cliente y las clases concretas.
* Facilitar la extensión del sistema sin modificar el código cliente.

---

## Idea Clave

> El cliente solicita un objeto, **no sabe ni le importa** qué clase concreta se crea.

---

## Estructura Básica

* **Producto**: interfaz o clase abstracta común.
* **Productos Concretos**: implementaciones del producto.
* **Factory**: clase o método que crea y devuelve productos.

---

## Ejemplo (Java)

```java
interface Transporte {
    void entregar();
}

class Camion implements Transporte {
    public void entregar() {
        System.out.println("Entrega por carretera");
    }
}

class Barco implements Transporte {
    public void entregar() {
        System.out.println("Entrega por mar");
    }
}

class TransporteFactory {
    public static Transporte crearTransporte(String tipo) {
        if (tipo.equals("camion")) return new Camion();
        if (tipo.equals("barco")) return new Barco();
        return null;
    }
}
```

---

## Cuándo Usarlo

* Cuando el tipo exacto del objeto se decide en tiempo de ejecución.
* Cuando hay muchas clases relacionadas.
* Cuando se desea seguir el **principio de abierto/cerrado**.

---

## Ventajas

* Menor acoplamiento.
* Código más flexible y extensible.
* Centraliza la lógica de creación.

## Desventajas

* Puede aumentar el número de clases.
* Mayor complejidad inicial.

---

## Nota Importante

No confundir con **Abstract Factory**: Factory crea **un producto**, Abstract Factory crea **familias de productos relacionados**.
