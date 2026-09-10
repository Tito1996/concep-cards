## 🧠 TARJETA DE ESTUDIO – SERVICIOS (`@Service`) EN SPRING BOOT

### ¿Qué es un servicio?
Un **servicio** es la capa donde vive la **lógica de negocio** de la aplicación.

En simple:
👉 *el servicio decide **qué se hace** y **cómo se hace***.

---

### Responsabilidad principal
Un servicio:
- Aplica reglas de negocio
- Coordina repositorios
- Orquesta procesos
- Toma decisiones del dominio

👉 **No** maneja HTTP  
👉 **No** accede directamente a la request o response

---

### `@Service`
- Marca una clase como **componente de servicio**
- Permite que Spring:
  - la detecte automáticamente
  - la inyecte donde se necesite

Idea clave:
> `@Service` no cambia la lógica, **define el rol** de la clase.

---

### Relación con otras capas
Flujo típico:
Controller → Service → Repository


- **Controller**: recibe y responde
- **Service**: contiene la lógica
- **Repository**: accede a la base de datos

---

### Regla de oro (entrevista 🚨)
> **La lógica de negocio nunca va en el controller.**

Si hay reglas, validaciones de negocio o decisiones:
👉 pertenecen al **service**.

---

### Buenas prácticas
- Servicios **finos y claros**
- Métodos con una responsabilidad
- Nombres que expresen acciones del negocio
- Usar transacciones (`@Transactional`) cuando aplica

---

### Errores comunes en entrevistas
- Lógica de negocio en controllers
- Servicios que solo llaman repositorios (anémicos)
- Servicios demasiado grandes
- Mezclar lógica técnica con lógica de negocio

---

### Frase que suma muchos puntos
> “El controller orquesta la request; el service contiene la lógica de negocio.”

---

