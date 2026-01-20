**TARJETA DE ESTUDIO – Built-in Directives en Angular**

---

## 📌 ¿Qué son las Built-in Directives?

Son **directivas incluidas por defecto en Angular** que permiten **controlar la estructura, el comportamiento y la apariencia del DOM** directamente desde el template.

No requieren instalación adicional.

---

## 🧱 Directivas Estructurales

**Modifican la estructura del DOM** (agregan o eliminan elementos).

### `*ngIf`

* Muestra u oculta elementos según una condición
* Crea o destruye nodos del DOM

📍 Uso común: renderizado condicional

---

### `*ngFor`

* Itera sobre colecciones
* Renderiza listas dinámicas

✔ Soporta `index`, `first`, `last`
✔ Usar `trackBy` para rendimiento

---

### `*ngSwitch`

* Control condicional múltiple
* Alternativa a múltiples `ngIf`

📍 Más legible para muchos casos

---

## 🎨 Directivas de Atributo

**Modifican apariencia o comportamiento** de un elemento existente.

### `ngClass`

* Aplica clases CSS dinámicamente

### `ngStyle`

* Aplica estilos inline dinámicos

✔ No alteran la estructura del DOM

---

## 🔗 Directivas de Enlace y Navegación

* `routerLink` → navegación entre rutas
* `routerLinkActive` → estilos según ruta activa

📍 Integradas con el Router

---

## 🎯 Buenas Prácticas

* Usar directivas estructurales con moderación
* Evitar lógica compleja en el template
* Preferir legibilidad sobre atajos
* Combinar con componentes pequeños
* Usar `trackBy` en listas grandes

---

## 📝 Nota para Full Stack

* Built-in directives controlan la UI sin JavaScript manual
* Reducen código en componentes
* Base del desarrollo Angular profesional

---

**Tip:**
Si necesitas controlar el DOM, primero revisa si Angular ya tiene una directiva built-in antes de crear una propia.
