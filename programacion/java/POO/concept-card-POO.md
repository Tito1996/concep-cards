# ☕ JAVA — POO (A5)

## Programación Orientada a Objetos (POO)

La **Programación Orientada a Objetos** es un paradigma que organiza el software en
**objetos** que combinan **estado (datos)** y **comportamiento (métodos)**.

---

### Objetivos principales
- Modelar el dominio de forma cercana a la realidad
- Reducir acoplamiento
- Aumentar reutilización y mantenibilidad
- Facilitar la evolución del código

---

### Conceptos clave en Java
- **Clase**: plantilla que define atributos y métodos
- **Objeto**: instancia concreta de una clase
- **Atributos**: estado del objeto
- **Métodos**: comportamiento del objeto

---

### Ejemplo simple
```java
class Usuario {
    String nombre;

    void saludar() {
        System.out.println("Hola " + nombre);
    }
}
