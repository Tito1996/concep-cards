**TARJETA DE ESTUDIO – Data Binding en Angular**

---

## 📌 ¿Qué es Data Binding?

Mecanismo que permite **sincronizar datos entre la lógica (TypeScript) y la vista (HTML)** de forma automática.

Angular detecta cambios y actualiza la UI sin manipular el DOM manualmente.

---

## ➡️ One-Way Data Binding

Flujo de datos **en una sola dirección**.

### Tipos principales:

1. **Property Binding**
   TypeScript → HTML
   `[property]="valor"`

2. **Event Binding**
   HTML → TypeScript
   `(event)="metodo()"`

3. **Interpolation**
   TypeScript → HTML
   `{{ variable }}`

✔ Mayor control
✔ Mejor rendimiento
✔ Más predecible

---

## 🔁 Two-Way Data Binding

Flujo de datos **bidireccional** entre vista y lógica.

* Cambios en la UI actualizan el modelo
* Cambios en el modelo actualizan la UI

**Sintaxis:**
`[(ngModel)]="variable"`

✔ Ideal para formularios simples
❌ Requiere importar `FormsModule`

---

## 🧠 Comparación Rápida

* **One-Way:** control, claridad, recomendado
* **Two-Way:** comodidad, menos código

---

## 🎯 Buenas Prácticas

* Priorizar **One-Way Binding**
* Usar Two-Way solo cuando aporta simplicidad
* Evitar lógica compleja en la vista

---

## 📝 Nota para Full Stack

* Data Binding conecta UX con datos del backend
* Fundamental para formularios y consumo de APIs
* Impacta directamente en rendimiento y mantenibilidad

---

**Tip:** Si no necesitas sincronización automática, no uses Two-Way Binding.
