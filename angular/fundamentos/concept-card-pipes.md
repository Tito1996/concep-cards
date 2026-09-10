**TARJETA DE ESTUDIO – Pipes en Angular**

---

## 📌 ¿Qué es un Pipe?

Un **pipe** es una función que **transforma datos para su visualización en la vista (HTML)**, sin modificar el valor original ni la lógica de negocio.

Se usa directamente en las plantillas.

---

## 🔄 Sintaxis Básica

```html
{{ valor | pipe }}
```

Permite **encadenar pipes**:

```html
{{ valor | pipe1 | pipe2 }}
```

---

## 🧩 Pipes Incorporados Comunes

* `date` → formato de fechas
* `currency` → formato monetario
* `uppercase / lowercase`
* `percent`
* `json`
* `slice`

✔ Uso inmediato
✔ Código más legible

---

## 🔁 Pipe `async`

* Maneja **Observables y Promises**
* Se suscribe y desuscribe automáticamente
* Actualiza la vista cuando llegan datos

✔ Evita memory leaks
✔ Muy usado con HTTP y RxJS

---

## 🛠️ Pipes Personalizados

Se crean para transformaciones específicas.

**Buenas prácticas:**

* Usar solo para presentación
* Evitar lógica compleja
* Preferir pipes **puros**
* Reutilizables

---

## ⚠️ Pipes Puros vs Impuros

* **Puros (default):** se ejecutan solo cuando cambia el valor
* **Impuros:** se ejecutan en cada ciclo de detección (impactan rendimiento)

---

## 🎯 ¿Cuándo usar Pipes?

* Formatear datos
* Transformar valores simples
* Mantener HTML limpio
* Evitar lógica en la vista

---

## 📝 Nota para Full Stack

* Mejoran claridad del frontend
* Separan presentación y lógica
* Complementan servicios y componentes

---

**Tip:** Si una transformación afecta datos o negocio, no es un pipe, es un servicio.
