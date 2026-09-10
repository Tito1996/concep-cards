# Patrón de Diseño **State**

**Tipo:** Comportamiento

---

## ¿Qué es?

El patrón **State** permite que un objeto **cambie su comportamiento cuando cambia su estado interno**, como si cambiara de clase en tiempo de ejecución.

---

## Intención

* Eliminar condicionales complejos basados en estados.
* Encapsular comportamientos dependientes del estado.
* Facilitar la extensión de nuevos estados.

---

## Idea Clave

> El comportamiento depende del **estado actual**, y cada estado se modela como una clase.

---

## Estructura Básica

* **State**: interfaz común para los estados.
* **Concrete States**: implementan el comportamiento según el estado.
* **Context**: mantiene una referencia al estado actual y delega el comportamiento.

---

## Ejemplo (Java)

```java
interface Estado {
    void manejar(Pedido pedido);
}

class EstadoNuevo implements Estado {
    public void manejar(Pedido pedido) {
        System.out.println("Pedido nuevo");
        pedido.setEstado(new EstadoProcesando());
    }
}

class EstadoProcesando implements Estado {
    public void manejar(Pedido pedido) {
        System.out.println("Pedido en proceso");
    }
}

class Pedido {
    private Estado estado;

    Pedido() {
        estado = new EstadoNuevo();
    }

    void setEstado(Estado estado) {
        this.estado = estado;
    }

    void procesar() {
        estado.manejar(this);
    }
}
```

---

## Cuándo Usarlo

* Cuando el comportamiento depende del estado.
* Cuando existen múltiples estados bien definidos.
* Cuando se desea evitar grandes bloques `if/else` o `switch`.

---

## Ventajas

* Código más limpio y mantenible.
* Fácil adición de nuevos estados.
* Cumple el principio abierto/cerrado.

## Desventajas

* Incrementa el número de clases.
* Mayor complejidad inicial.

---

## Comparación Rápida

* **State**: cambia comportamiento según el estado.
* **Strategy**: intercambia algoritmos.
* **Command**: encapsula acciones.
