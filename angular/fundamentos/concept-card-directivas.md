**TARJETA DE ESTUDIO – Directivas en Angular**

---

## 📌 ¿Qué es una Directiva?

Clase que **extiende el comportamiento del DOM**.
Permite agregar lógica declarativa directamente en el HTML, sin manipular el DOM manualmente.

---

## 🧩 Tipos de Directivas

### 🧱 Directivas Estructurales

**Cambian la estructura del DOM** (agregan o eliminan elementos).

* `*ngIf` → muestra u oculta elementos
* `*ngFor` → renderiza listas
* `*ngSwitch` → control condicional múltiple

**Características:**

* Usan el prefijo `*`
* Se traducen internamente a `<ng-template>`

---

### 🎨 Directivas de Atributo

**Modifican apariencia o comportamiento** de un elemento existente.

* `ngClass` → clases dinámicas
* `ngStyle` → estilos dinámicos
* Directivas personalizadas

**Características:**

* No alteran la estructura
* Actúan sobre elementos ya renderizados

---

## 🛠️ Directivas Personalizadas

Permiten crear comportamientos reutilizables.

**Ejemplos de uso:**

* Resaltar elementos
* Controlar permisos
* Validaciones visuales

**Buenas prácticas:**

* Responsabilidad única
* Reutilizables
* Sin lógica de negocio

---

## 🎯 ¿Cuándo usar Directivas?

* Reutilizar lógica visual
* Evitar duplicar código en componentes
* Mantener componentes simples

---

## 📝 Nota para Full Stack

* Directivas = control fino del frontend
* Complementan componentes y servicios
* Mejoran mantenibilidad y legibilidad

---

**Tip:** Si repites la misma lógica HTML en varios componentes, probablemente necesitas una directiva.
