# ☕ JAVA — Herencia (A5)

### Herencia

La **herencia** permite que una clase **reutilice y extienda** el comportamiento de otra.
Establece una relación **“es un” (is-a)** entre clases.

---

### Conceptos clave
- **Clase padre (superclase)**
- **Clase hija (subclase)**
- Uso de la palabra clave `extends`

---

### Ejemplo
```java
class Animal {
    void hacerSonido() {
        System.out.println("Sonido genérico");
    }
}

class Perro extends Animal {
    void hacerSonido() {
        System.out.println("Ladrido");
    }
}
````

---

### Características en Java

* Java permite **herencia simple** (una sola superclase)
* Las subclases heredan métodos y atributos `protected` y `public`
* Los constructores **no se heredan**

---

### Uso de `super`

* Acceder a métodos o constructores de la clase padre

```java
super.hacerSonido();
```

---

### Riesgos de mal uso

❌ Jerarquías profundas
❌ Clases rígidas y acopladas

---

### Buena práctica

✅ Usar herencia solo cuando exista una relación clara “es un”
✅ Preferir **composición** cuando sea posible
