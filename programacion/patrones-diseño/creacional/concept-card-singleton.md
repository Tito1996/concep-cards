# Patrón de Diseño **Singleton**

**Tipo:** Creacional

---

## ¿Qué es?

El patrón **Singleton** garantiza que una clase tenga **una única instancia** y proporciona un **punto de acceso global** a ella.

---

## Intención

* Controlar el acceso concurrente a recursos compartidos.
* Evitar la creación de múltiples instancias de una clase crítica.
* Centralizar la gestión de estado o configuración.

---

## Estructura Básica

* **Constructor privado** (impide instanciación externa).
* **Atributo estático** que almacena la única instancia.
* **Método público estático** para obtener la instancia.

---

## Ejemplo (Java)

```java
public class Singleton {
    private static Singleton instancia;

    private Singleton() {}

    public static Singleton getInstancia() {
        if (instancia == null) {
            instancia = new Singleton();
        }
        return instancia;
    }
}
```

---

## Cuándo Usarlo

* Gestores de configuración.
* Pools de conexiones.
* Logs centralizados.
* Acceso a hardware o servicios únicos.

---

## Ventajas

* Control estricto de instancias.
* Acceso global y consistente.
* Inicialización perezosa (lazy).

## Desventajas

* Puede dificultar pruebas unitarias.
* Riesgo de dependencias globales.
* Requiere cuidado en entornos multihilo.

---

## Nota Importante

En aplicaciones concurrentes, considerar **thread-safe Singleton** (por ejemplo, inicialización estática o doble comprobación con `synchronized`).
