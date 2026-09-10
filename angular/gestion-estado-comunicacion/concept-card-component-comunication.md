**TARJETA DE ESTUDIO – Comunicación entre Componentes en Angular**

---

## 📌 ¿Por qué es importante?

La **comunicación entre componentes** permite **compartir datos y eventos** manteniendo una arquitectura **desacoplada, clara y escalable**.

Es clave para aplicaciones Angular medianas y grandes.

---

## 🔁 Tipos de Comunicación

### 👨‍👧 Padre → Hijo

Se usa **@Input()** para pasar datos.

* Flujo unidireccional
* Ideal para configuraciones y datos simples

✔ Simple
✔ Directo
📍 Uso más común

---

### 👶‍👨 Hijo → Padre

Se usa **@Output() + EventEmitter** para emitir eventos.

* El hijo notifica acciones
* El padre decide qué hacer

✔ Controlado
✔ Orientado a eventos

---

### 🔄 Componentes Hermanos

No se comunican directamente.

✔ Se usa un **servicio compartido**

* `Subject`
* `BehaviorSubject`
* `Observable`

📍 Patrón recomendado
📍 Evita acoplamiento

---

### 🌐 Componentes No Relacionados

Siempre mediante **servicios compartidos**.

* Estado global
* Eventos transversales
* Datos compartidos

✔ Escalable
✔ Mantenible

---

## 🧠 Comparación Rápida

* **@Input / @Output** → relación directa
* **Servicio + RxJS** → relación indirecta
* **Servicio** → preferido a largo plazo

---

## 🎯 Buenas Prácticas

* Preferir comunicación unidireccional
* Evitar cadenas largas de @Input
* Usar servicios para estado compartido
* Desuscribirse de Observables
* Mantener componentes simples

---

## 📝 Nota para Full Stack

* Similar a capas backend comunicándose por contratos
* Facilita mantenimiento y testing
* Fundamental para arquitectura Angular profesional

---

**Tip:**
Si los componentes no tienen relación padre–hijo, **no fuerces @Input/@Output**: usa un servicio.
