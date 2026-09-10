**TARJETA DE ESTUDIO – Control Flow Blocks en Angular**

---

## 📌 ¿Qué son los Control Flow Blocks?

Son la **nueva sintaxis declarativa de Angular** para controlar el flujo del template, introducida para **reemplazar gradualmente** a las directivas estructurales clásicas.

Usan bloques con `@`:

* `@if`
* `@for`
* `@switch`

✔ Más legibles
✔ Mejor rendimiento
✔ Sintaxis moderna

---

## 🧱 `@if`

Controla renderizado condicional.

```html
@if (isLoggedIn) {
  <p>Bienvenido</p>
} @else {
  <p>Inicia sesión</p>
}
```

✔ Más claro que `*ngIf`
✔ Soporta `@else if`

---

## 🔁 `@for`

Itera sobre colecciones.

```html
@for (item of items; track item.id) {
  <li>{{ item.name }}</li>
}
```

✔ `track` obligatorio (mejor rendimiento)
✔ Reemplaza `*ngFor + trackBy`

---

## 🔀 `@switch`

Control condicional múltiple.

```html
@switch (status) {
  @case ('SUCCESS') { <p>OK</p> }
  @case ('ERROR') { <p>Error</p> }
  @default { <p>Desconocido</p> }
}
```

✔ Más expresivo que `*ngSwitch`

---

## 🧠 Diferencias vs Directivas Clásicas

* **Control Flow Blocks:**
  → Sintaxis de bloques, más legible, futura recomendación
* **Directivas (`*ngIf`, `*ngFor`):**
  → Compatibles, pero menos expresivas

---

## 🎯 Buenas Prácticas

* Preferir Control Flow Blocks en proyectos nuevos
* Usar condiciones simples en templates
* Mantener la lógica en el componente
* Usar `track` siempre en `@for`

---

## 📝 Nota para Full Stack

* Templates más claros y mantenibles
* Mejor rendimiento en listas grandes
* Alineado con la evolución moderna de Angular

---

**Tip:**
Si estás empezando un proyecto nuevo en Angular, usa **Control Flow Blocks** desde el inicio. Son el futuro del framework.
