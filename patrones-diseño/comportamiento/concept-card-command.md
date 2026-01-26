# Patrón de Diseño **Command**

**Tipo:** Comportamiento

---

## ¿Qué es?

El patrón **Command** encapsula una **petición como un objeto**, permitiendo parametrizar clientes con distintas solicitudes, encolar operaciones y soportar deshacer/rehacer.

---

## Intención

* Desacoplar el emisor de la petición del receptor.
* Tratar acciones como objetos.
* Implementar operaciones de **undo/redo**.

---

## Idea Clave

> Una acción se convierte en un **objeto comando** que puede ejecutarse cuando se desee.

---

## Estructura Básica

* **Command**: interfaz que declara el método `execute()`.
* **Concrete Command**: implementa la acción y conoce al receptor.
* **Receiver**: realiza la operación real.
* **Invoker**: solicita la ejecución del comando.
* **Cliente**: crea y configura el comando.

---

## Ejemplo (Java)

```java
interface Comando {
    void ejecutar();
}

class Luz {
    void encender() {
        System.out.println("Luz encendida");
    }
}

class EncenderLuzCommand implements Comando {
    private Luz luz;

    EncenderLuzCommand(Luz luz) {
        this.luz = luz;
    }

    public void ejecutar() {
        luz.encender();
    }
}

class ControlRemoto {
    private Comando comando;

    void setComando(Comando comando) {
        this.comando = comando;
    }

    void presionarBoton() {
        comando.ejecutar();
    }
}
```

---

## Cuándo Usarlo

* Cuando se necesitan colas o logs de operaciones.
* Para implementar deshacer/rehacer.
* Cuando se quiere desacoplar UI y lógica de negocio.

---

## Ventajas

* Alto desacoplamiento.
* Fácil extensión de nuevas acciones.
* Permite historial de comandos.

## Desventajas

* Incrementa el número de clases.
* Puede añadir complejidad innecesaria.

---

## Comparación Rápida

* **Command**: encapsula acciones.
* **Strategy**: encapsula algoritmos.
* **Observer**: notifica cambios.
