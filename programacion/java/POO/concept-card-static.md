# ☕ JAVA — static vs instancia (A5)

### static vs instancia

En Java, los miembros pueden pertenecer a la **clase** o a la **instancia**.

---

### Miembros de instancia
- Pertenecen a cada objeto
- Requieren crear una instancia
- Cada objeto tiene su propio estado

```java
class Usuario {
    String nombre;
}
````

---

### Miembros `static`

* Pertenecen a la **clase**
* Se comparten entre todas las instancias
* No dependen de un objeto concreto

```java
class Contador {
    static int total;
}
```
### Acceso

```java
Contador.total++;
```

---

### Cuándo usar `static`

✅ Constantes (`public static final`)
✅ Utilidades sin estado
✅ Contadores o configuraciones globales

### Cuándo NO usar `static`

❌ Lógica de negocio dependiente de estado
❌ Cuando se requiere polimorfismo

### Error común

Usar `static` como reemplazo de diseño orientado a objetos
