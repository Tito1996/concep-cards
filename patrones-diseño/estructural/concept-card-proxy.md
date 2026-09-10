# Patrón de Diseño **Proxy**

**Tipo:** Estructural

---

## ¿Qué es?

El patrón **Proxy** proporciona un **objeto sustituto o representante** que controla el acceso a otro objeto, llamado **Real Subject**.

---

## Intención

* Controlar el acceso a un objeto.
* Añadir funcionalidades adicionales (seguridad, caché, control remoto).
* Retrasar la creación de objetos costosos (lazy loading).

---

## Idea Clave

> El cliente interactúa con el **Proxy**, no directamente con el objeto real.

---

## Tipos Comunes de Proxy

* **Proxy Virtual**: creación diferida del objeto.
* **Proxy de Protección**: control de permisos.
* **Proxy Remoto**: acceso a objetos en otro sistema.
* **Proxy de Caché**: almacena resultados.

---

## Estructura Básica

* **Subject**: interfaz común.
* **Real Subject**: objeto real.
* **Proxy**: controla el acceso al Real Subject.
* **Cliente**: usa el Subject.

---

## Ejemplo (Java)

```java
interface Imagen {
    void mostrar();
}

class ImagenReal implements Imagen {
    private String archivo;

    ImagenReal(String archivo) {
        this.archivo = archivo;
        cargarDesdeDisco();
    }

    private void cargarDesdeDisco() {
        System.out.println("Cargando " + archivo);
    }

    public void mostrar() {
        System.out.println("Mostrando " + archivo);
    }
}

class ImagenProxy implements Imagen {
    private ImagenReal imagen;
    private String archivo;

    ImagenProxy(String archivo) {
        this.archivo = archivo;
    }

    public void mostrar() {
        if (imagen == null) {
            imagen = new ImagenReal(archivo);
        }
        imagen.mostrar();
    }
}
```

---

## Cuándo Usarlo

* Cuando el objeto real es costoso de crear.
* Cuando se requiere control de acceso.
* Cuando se necesita acceso remoto o diferido.

---

## Ventajas

* Control adicional sin modificar el objeto real.
* Mejora de rendimiento.
* Mayor seguridad.

## Desventajas

* Incrementa la complejidad.
* Puede introducir latencia adicional.

---

## Comparación Rápida

* **Proxy**: controla el acceso a un objeto.
* **Decorator**: añade comportamiento.
* **Facade**: simplifica el uso de un sistema.
