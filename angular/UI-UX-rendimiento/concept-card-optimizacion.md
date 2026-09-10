**TARJETA DE ESTUDIO – Optimización y Rendimiento en Angular**
**Formato:** A6

---

## 📌 ¿Por qué es importante el rendimiento?

Una aplicación Angular optimizada:

* Carga más rápido
* Consume menos recursos
* Mejora la experiencia de usuario (UX)
* Escala mejor en producción

El rendimiento es **arquitectura + buenas prácticas**, no solo código.

---

## 🚀 Técnicas Clave de Optimización

### 🧭 Lazy Loading

* Cargar módulos solo cuando se necesitan
* Reduce el bundle inicial
* Imprescindible en apps medianas/grandes

---

### 🔁 Change Detection

* Usar `ChangeDetectionStrategy.OnPush`
* Reduce ciclos innecesarios de detección
* Ideal para componentes con inputs inmutables

✔ Mejora rendimiento notablemente

---

### 🔄 Async Pipe

* Usar `| async` en templates
* Gestiona suscripciones automáticamente

✔ Evita memory leaks
✔ Código más limpio

---

### 🧱 Componentes Livianos

* Lógica en servicios, no en componentes
* Evitar componentes muy grandes
* Dividir vistas complejas en subcomponentes

---

## ⚙️ Optimización de Plantillas

* Evitar funciones en el HTML
* Usar `trackBy` en `*ngFor`
* Minimizar bindings innecesarios

✔ Reduce renderizados costosos

---

## 📦 Build y Producción

* Usar `ng build --configuration production`
* AOT (Ahead-of-Time Compilation)
* Tree Shaking automático
* Minificación de JS y CSS

---

## 🧠 Buenas Prácticas Generales

* Evitar `any`
* Desuscribirse de Observables
* Usar `PreloadingStrategy` cuando aplique
* Medir rendimiento (no asumir)

---

## 📝 Nota para Full Stack

* Frontend rápido reduce carga percibida del backend
* Impacta directamente en métricas de negocio
* Angular bien optimizado compite con cualquier SPA moderna

---

**Tip:**
Si la aplicación es lenta, no empieces por el servidor: revisa primero el Change Detection y el Lazy Loading.
