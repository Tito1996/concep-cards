# ☕ JAVA — Polimorfismo

### Polimorfismo

El **polimorfismo** permite que una misma referencia se comporte de distintas formas
según el **tipo real del objeto** que apunta.

### Idea clave
> “Una interfaz, múltiples implementaciones”

---

### Ejemplo
```java
Animal animal = new Perro();
animal.hacerSonido(); // Ladrido
````

Aunque la referencia es de tipo `Animal`, el método ejecutado
corresponde al objeto `Perro`.

---

### Tipos de polimorfismo en Java

* **Polimorfismo en tiempo de ejecución** (override)
* **Polimorfismo en tiempo de compilación** (sobrecarga de métodos)

---

### Override

```java
@Override
void hacerSonido() {
    System.out.println("Ladrido");
}
```

---

### Beneficios

* Código flexible y extensible
* Reducción de condicionales (`if / switch`)
* Base para diseño orientado a interfaces

---

### Error común

❌ Depender de tipos concretos
✅ Programar contra **abstracciones**
