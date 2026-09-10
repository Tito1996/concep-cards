# Patrón de Diseño **Observer**

**Tipo:** Comportamiento

---

## ¿Qué es?

El patrón **Observer** define una **relación uno-a-muchos** entre objetos, de modo que cuando uno cambia de estado, **todos sus observadores son notificados automáticamente**.

---

## Intención

* Mantener objetos sincronizados sin acoplamiento fuerte.
* Notificar cambios de estado de forma automática.
* Implementar sistemas reactivos y basados en eventos.

---

## Idea Clave

> Los observadores **se suscriben** a un sujeto y reciben notificaciones cuando hay cambios.

---

## Estructura Básica

* **Subject**: mantiene la lista de observadores y los notifica.
* **Observer**: interfaz de notificación.
* **Concrete Subject**: cambia de estado.
* **Concrete Observer**: reacciona a los cambios.

---

## Ejemplo (Java)

```java
interface Observer {
    void actualizar(int estado);
}

interface Sujeto {
    void agregar(Observer o);
    void eliminar(Observer o);
    void notificar();
}

class Sensor implements Sujeto {
    private List<Observer> observadores = new ArrayList<>();
    private int estado;

    public void setEstado(int estado) {
        this.estado = estado;
        notificar();
    }

    public void agregar(Observer o) { observadores.add(o); }
    public void eliminar(Observer o) { observadores.remove(o); }
    public void notificar() {
        for (Observer o : observadores) {
            o.actualizar(estado);
        }
    }
}
```

---

## Cuándo Usarlo

* Cuando varios objetos dependen de otro.
* En sistemas de eventos, notificaciones o UI.
* Cuando se quiere bajo acoplamiento.

---

## Ventajas

* Bajo acoplamiento.
* Soporta múltiples observadores.
* Facilita sistemas reactivos.

## Desventajas

* Orden de notificación no garantizado.
* Posibles problemas de rendimiento.

---

## Comparación Rápida

* **Observer**: notifica cambios de estado.
* **Strategy**: intercambia algoritmos.
* **Command**: encapsula acciones.
