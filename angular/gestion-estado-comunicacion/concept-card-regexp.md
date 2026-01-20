**TARJETA DE ESTUDIO – RegExp en Angular**
**Enfoque:** Validaciones y uso práctico

---

## 📌 ¿Qué es una RegExp?

Una **RegExp (Regular Expression)** es un **patrón de búsqueda** usado para **validar, buscar o transformar texto**.

En Angular se utiliza principalmente para:

* Validaciones de formularios
* Control de entradas de usuario
* Reglas de formato

---

## 🧱 RegExp en Angular Forms

Angular usa **RegExp** a través de `Validators.pattern`.

```ts
Validators.pattern(/^[a-zA-Z]+$/)
```

✔ Funciona en **Reactive Forms** y **Template-driven Forms**

---

## 🧩 Casos Comunes de Uso

### 📧 Email

```ts
/^[^\s@]+@[^\s@]+\.[^\s@]+$/
```

---

### 🔢 Solo números

```ts
/^[0-9]+$/
```

---

### 🔐 Password fuerte

```ts
/^(?=.*[A-Z])(?=.*\d).{8,}$/
```

✔ Al menos una mayúscula
✔ Al menos un número
✔ Mínimo 8 caracteres

---

### 📱 Teléfono

```ts
/^\d{9,10}$/
```

---

## ⚙️ Uso en Reactive Forms

```ts
this.form = this.fb.group({
  email: ['', [Validators.required, Validators.pattern(emailRegex)]]
});
```

✔ Validación declarativa
✔ Clara y reutilizable

---

## 🎯 Buenas Prácticas

* Centralizar RegExp en constantes
* Mantener patrones legibles
* Documentar expresiones complejas
* No abusar de RegExp muy largas
* Validar también en backend

---

## ⚠️ Errores Comunes

* RegExp demasiado estrictas
* No escapar caracteres especiales
* Confiar solo en validación frontend
* Repetir patrones en múltiples componentes

---

## 📝 Nota para Full Stack

* RegExp en Angular = primera capa de validación
* Backend (Java) debe validar nuevamente
* Mejora UX y reduce errores tempranos

---

**Tip:**
Si no puedes explicar una RegExp en una frase, probablemente es demasiado compleja y necesita refactorización.
