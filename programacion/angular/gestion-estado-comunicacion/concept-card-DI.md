**TARJETA DE ESTUDIO – Dependency Injection (DI) en Angular**
**Formato:** A6

---

## 📌 ¿Qué es Dependency Injection?

La **Dependency Injection (DI)** es un patrón de diseño que permite que **Angular proporcione automáticamente las dependencias** que una clase necesita, en lugar de crearlas manualmente.

✔ Bajo acoplamiento
✔ Código más mantenible
✔ Fácil testing

---

## 🧩 Conceptos Clave

* **Dependency:** objeto que una clase necesita
* **Injector:** responsable de crear y entregar dependencias
* **Provider:** instrucción que indica cómo crear una dependencia

---

## 🧱 Servicios y `@Injectable`

Los servicios se marcan con `@Injectable` para que Angular pueda inyectarlos.

```ts
@Injectable({ providedIn: 'root' })
export class UserService {}
```

✔ `providedIn: 'root'` → singleton global

---

## 🔄 Inyección en Componentes

Las dependencias se inyectan por **constructor**.

```ts
constructor(private userService: UserService) {}
```

✔ Angular resuelve la instancia automáticamente

---

## 📦 Scopes de Providers

* **Root:** una instancia para toda la app
* **Módulo:** una instancia por módulo
* **Componente:** nueva instancia por componente

📍 Elegir el scope impacta en estado y rendimiento

---

## 🎯 Beneficios Principales

* Separación de responsabilidades
* Reutilización de servicios
* Sustitución sencilla de implementaciones
* Facilita mocks en testing

---

## ⚠️ Errores Comunes

* Crear servicios manualmente (`new`)
* Servicios “Dios” con demasiada lógica
* Scope incorrecto del provider
* Dependencias circulares

---

## 📝 Nota para Full Stack

* DI en Angular es similar a Spring en Java
* Base de arquitecturas escalables
* Clave para testing y mantenimiento

---

**Tip:**
Si ves `new Service()` en Angular, probablemente estás rompiendo la inyección de dependencias.
