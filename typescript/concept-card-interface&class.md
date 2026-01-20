**TARJETA DE ESTUDIO – Interfaces y Clases (TypeScript)**

---

## 📌 ¿Qué es una Interface?

Contrato que **define la forma de un objeto**.
Especifica **qué propiedades y métodos debe tener**, pero **no cómo se implementan**.

✔ No genera código en JavaScript
✔ Se usa para tipado y diseño

**Ejemplo:**

```ts
interface Usuario {
  id: number;
  nombre: string;
  activo: boolean;
}
```

---

## 📌 ¿Qué es una Clase?

Plantilla que **define atributos y comportamiento** de un objeto.
Sí genera código en JavaScript.

✔ Contiene lógica
✔ Puede crear instancias
✔ Usa constructores y métodos

**Ejemplo:**

```ts
class UsuarioImpl {
  constructor(
    public id: number,
    public nombre: string,
    public activo: boolean
  ) {}
}
```

---

## 🔗 Relación entre Interfaces y Clases

Una clase puede **implementar una o varias interfaces**.

```ts
class UsuarioService implements Usuario {
  id: number;
  nombre: string;
  activo: boolean;
}
```

✔ Garantiza contratos
✔ Cumple principios SOLID
✔ Reduce errores

---

## 🧠 Diferencias Clave

* **Interface:** qué debe existir
* **Clase:** cómo funciona
* **Interface:** diseño
* **Clase:** implementación

---

## 🎯 Buenas Prácticas

* Usar **interfaces** para modelos y contratos
* Usar **clases** para lógica y comportamiento
* Programar contra interfaces, no implementaciones
* Reutilizar interfaces en APIs y servicios

---

## 📝 Nota para Full Stack

* Interfaces = DTOs / contratos con backend
* Clases = servicios, componentes, lógica
* Fundamental para Angular y código escalable

---

**Tip:** 
Si describes datos → interface.
Si describes comportamiento → clase.
