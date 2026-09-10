**TARJETA DE ESTUDIO – Routing en Angular**

---

## 📌 ¿Qué es el Routing?

Mecanismo que permite **navegar entre vistas** en una Single Page Application (SPA) **sin recargar la página**.

Angular asocia **URLs → Componentes**.

---

## 🧭 Elementos Clave

* **RouterModule**: habilita el sistema de rutas
* **Routes**: arreglo de configuración de rutas
* **router-outlet**: punto donde se renderiza el componente
* **routerLink**: navegación declarativa

---

## 🧩 Configuración Básica

* Definir rutas:

  * `path` → URL
  * `component` → vista asociada
* Ruta por defecto y wildcard (`**`)

✔ Navegación clara
✔ Separación de vistas

---

## 🚀 Lazy Loading

Carga módulos **solo cuando se necesitan**.

* Reduce el tamaño inicial
* Mejora el rendimiento
* Ideal para módulos grandes

✔ Escalabilidad
✔ Mejor experiencia de usuario

---

## 🔐 Guards

Protegen rutas según condiciones.

* `CanActivate` → acceso permitido
* `CanDeactivate` → salir de una vista
* `CanLoad` → carga de módulos

📍 Usados para autenticación y permisos

---

## 🔁 Navegación Programática

* Usando `Router`
* Redirecciones tras acciones (login, logout)

✔ Control desde el código

---

## 🎯 Buenas Prácticas

* Rutas por módulo
* Usar Lazy Loading
* Proteger rutas sensibles con Guards
* Mantener URLs semánticas

---

## 📝 Nota para Full Stack

* Routing define la experiencia de navegación
* Se integra con seguridad backend
* Clave para SPAs profesionales

---

**Tip:** Si una aplicación Angular crece, el Lazy Loading deja de ser opcional y pasa a ser obligatorio.
