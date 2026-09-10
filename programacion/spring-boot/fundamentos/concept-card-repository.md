## 🧠 TARJETA DE ESTUDIO – REPOSITORIOS Y JPA BÁSICO (SPRING BOOT)

### ¿Qué es JPA?
JPA (Java Persistence API) es una **especificación** que permite **mapear objetos Java a tablas de base de datos**.

En simple:
👉 *trabajas con objetos y JPA se encarga de la base de datos.*

---

### `@Entity`
Marca una clase como **entidad persistente**.

Una entidad:
- Representa una **tabla**
- Cada instancia representa una **fila**
- Debe tener un `@Id`

Idea clave:
> Una entidad es el modelo de datos, no la API.

---

### ¿Qué es un repositorio?
Un repositorio es la **capa de acceso a datos**.

Se encarga de:
- Guardar
- Leer
- Actualizar
- Borrar

👉 **No contiene lógica de negocio**.

---

### `JpaRepository`
Es una interfaz de Spring Data JPA que:
- Ya trae operaciones CRUD listas
- Evita escribir SQL básico
- Se integra automáticamente con JPA

Idea clave:
> Con `JpaRepository` no escribes SQL para lo básico.

---

### Operaciones CRUD básicas

#### Crear / Guardar
- Persistir una entidad nueva
- También se usa para actualizar

👉 mismo método, distinto estado del objeto.

---

#### Leer
- Buscar por ID
- Listar registros
- Consultar existencia

Se usan métodos ya provistos por el repositorio.

---

#### Actualizar
- Se modifica una entidad existente
- JPA detecta los cambios (dirty checking)
- Se persisten al finalizar la transacción

👉 no siempre necesitas llamar a `save`.

---

#### Borrar
- Eliminar por ID o entidad
- Borra la fila correspondiente en la base

---

### Qué NO se espera en nivel junior
- SQL complejo
- Queries optimizadas
- Manejo avanzado de performance

👉 solo entender **el flujo básico de persistencia**.

---

### Errores comunes en entrevistas
- Lógica de negocio en repositorios
- Pensar que `save` solo crea
- Confundir entidad con DTO
- No entender qué hace realmente JPA

---

### Frase que suma puntos
> “El repositorio accede a datos; la lógica vive en el service.”

---
