# ☕ JAVA — Modificadores de acceso (A5)

### Modificadores de acceso

Los **modificadores de acceso** controlan **desde dónde** se puede acceder
a clases, atributos y métodos.

---

### Modificadores disponibles en Java

| Modificador | Misma clase | Mismo paquete | Subclase | Fuera |
|------------|-------------|---------------|----------|-------|
| `private`  | ✅ | ❌ | ❌ | ❌ |
| *(default)*| ✅ | ✅ | ❌ | ❌ |
| `protected`| ✅ | ✅ | ✅ | ❌ |
| `public`   | ✅ | ✅ | ✅ | ✅ |

---

### Uso recomendado
- **`private`** → atributos
- **`protected`** → extensión controlada
- **`public`** → API expuesta
- **default** → uso interno del paquete

---

### Ejemplo
```java
public class Usuario {
    private String nombre;

    protected void validar() {}

    public String getNombre() {
        return nombre;
    }
}
````

---

### Principio clave

> Cuanto más restrictivo, mejor

### Error común

❌ Usar `public` por comodidad
✅ Empezar con `private` y abrir solo si es necesario
