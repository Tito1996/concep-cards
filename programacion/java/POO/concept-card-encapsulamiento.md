# ☕ JAVA — Encapsulamiento

### Encapsulamiento

El **encapsulamiento** es el principio de POO que consiste en **ocultar el estado interno**
de un objeto y **exponer solo lo necesario** a través de métodos controlados.

---

### ¿Qué se encapsula?
- **Atributos** (datos internos)
- **Implementación interna** de la lógica

---

### ¿Cómo se logra en Java?
- Atributos `private`
- Métodos públicos (getters/setters) para acceso controlado

---

### Ejemplo
```java
class CuentaBancaria {
    private double saldo;

    public double getSaldo() {
        return saldo;
    }

    public void depositar(double monto) {
        if (monto > 0) {
            saldo += monto;
        }
    }
}
````

---

### Beneficios

* Protege la integridad del objeto
* Reduce dependencias externas
* Permite cambiar la implementación sin afectar a los consumidores

---

### Buenas prácticas

✅ Validar datos dentro del objeto
✅ Exponer solo lo necesario
❌ Evitar getters/setters sin lógica en exceso

---

 ### Señal de mal encapsulamiento

* Atributos `public`
* Lógica de negocio fuera del objeto
