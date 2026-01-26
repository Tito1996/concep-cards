# Patrón de Diseño **Composite**

**Tipo:** Estructural

---

## ¿Qué es?

El patrón **Composite** permite tratar **objetos individuales y composiciones de objetos de manera uniforme**, organizándolos en estructuras de árbol.

---

## Intención

* Representar jerarquías parte–todo.
* Permitir que el cliente trate objetos simples y compuestos de la misma forma.
* Simplificar el uso de estructuras complejas.

---

## Idea Clave

> Un objeto compuesto contiene otros objetos que siguen la **misma interfaz**.

---

## Estructura Básica

* **Component**: interfaz común.
* **Leaf**: objeto simple sin hijos.
* **Composite**: objeto que contiene hijos (Component).
* **Cliente**: trabaja solo con Component.

---

## Ejemplo (Java)

```java
interface Archivo {
    void mostrar();
}

class ArchivoSimple implements Archivo {
    private String nombre;
    ArchivoSimple(String nombre) { this.nombre = nombre; }
    public void mostrar() {
        System.out.println(nombre);
    }
}

class Carpeta implements Archivo {
    private List<Archivo> archivos = new ArrayList<>();

    public void agregar(Archivo archivo) {
        archivos.add(archivo);
    }

    public void mostrar() {
        for (Archivo a : archivos) {
            a.mostrar();
        }
    }
}
```

---

## Cuándo Usarlo

* Cuando se manejan estructuras jerárquicas.
* Cuando se necesita tratar objetos simples y compuestos igual.
* En árboles de archivos, menús, gráficos.

---

## Ventajas

* Simplifica el código cliente.
* Facilita la extensión.
* Uso uniforme de objetos.

## Desventajas

* Puede ser difícil restringir tipos de componentes.
* Diseño más complejo.

---

## Comparación Rápida

* **Composite**: trata objetos simples y compuestos igual.
* **Decorator**: añade comportamiento.
* **Facade**: simplifica el acceso a un sistema.
