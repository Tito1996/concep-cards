# Patrón de Diseño **Abstract Factory**

**Tipo:** Creacional

---

## ¿Qué es?

El patrón **Abstract Factory** proporciona una **interfaz para crear familias de objetos relacionados o dependientes**, sin especificar sus clases concretas.

---

## Intención

* Crear conjuntos de objetos que deben funcionar juntos.
* Garantizar la **compatibilidad** entre productos relacionados.
* Desacoplar el código cliente de las clases concretas.

---

## Idea Clave

> Se crea una **fábrica de fábricas** que produce **familias completas de objetos**.

---

## Estructura Básica

* **Abstract Factory**: declara métodos para crear cada producto.
* **Factories Concretas**: implementan la creación de una familia específica.
* **Productos Abstractos**: interfaces comunes.
* **Productos Concretos**: implementaciones compatibles entre sí.

---

## Ejemplo (Java)

```java
interface Boton {
    void render();
}

interface Ventana {
    void mostrar();
}

class BotonWindows implements Boton {
    public void render() { System.out.println("Botón Windows"); }
}

class VentanaWindows implements Ventana {
    public void mostrar() { System.out.println("Ventana Windows"); }
}

interface GUIFactory {
    Boton crearBoton();
    Ventana crearVentana();
}

class WindowsFactory implements GUIFactory {
    public Boton crearBoton() { return new BotonWindows(); }
    public Ventana crearVentana() { return new VentanaWindows(); }
}
```

---

## Cuándo Usarlo

* Cuando el sistema debe ser independiente de cómo se crean los objetos.
* Cuando se necesita asegurar coherencia entre productos relacionados.
* En sistemas multiplataforma (Windows, macOS, Linux).

---

## Ventajas

* Asegura compatibilidad entre productos.
* Facilita el cambio de familias completas.
* Cumple el principio **abierto/cerrado**.

## Desventajas

* Mayor complejidad estructural.
* Difícil añadir nuevos tipos de productos.

---

## Comparación Rápida

* **Factory**: crea un solo producto.
* **Abstract Factory**: crea **familias de productos** relacionados.
