## 🧠 TARJETA DE ESTUDIO – HIBERNATE (CRITERIO PRÁCTICO)

### JPA vs Hibernate
- **JPA**: es una **especificación** (qué se puede hacer)
- **Hibernate**: es la **implementación más usada** de JPA (cómo se hace)

Idea clave (entrevista):
👉 *JPA define las reglas, Hibernate las ejecuta.*

---

### Relaciones entre entidades (MUY preguntado)

#### `@ManyToOne`
- Muchas entidades apuntan a una
- Es la relación **más común**
- Vive del lado que tiene la FK

Ejemplo mental:
👉 muchos pedidos → un usuario

---

#### `@OneToMany`
- Una entidad tiene muchas relacionadas
- Es el lado **inverso**
- No suele tener la FK

Idea clave:
> En JPA, **`ManyToOne` es la relación fuerte**.

Error común:
🚨 mapear todo como `OneToMany` sin pensar.

---

### Lazy vs Eager loading

#### `LAZY`
- Los datos **no se cargan** hasta que se usan
- Más eficiente
- Requiere contexto de sesión/transacción

👉 **Es la opción recomendada por defecto.**

---

#### `EAGER`
- Los datos se cargan **siempre**
- Puede traer información innecesaria
- Impacta performance

Regla práctica:
> Usar `EAGER` solo si estás 100 % seguro.

---

### Problema clásico: N+1 🚨
Ocurre cuando:
1. JPA ejecuta **1 query** para obtener una lista
2. Ejecuta **N queries adicionales** para relaciones

Resultado:
👉 muchas queries → mala performance

---

### Cómo detectar N+1
- Logs de SQL
- Muchas queries similares
- Performance lenta al listar datos

---

### Cómo evitar N+1 (criterio mid)
- `JOIN FETCH` en queries
- Queries específicas
- DTOs
- Acceder a relaciones dentro de la transacción

🚫 **NO** se soluciona poniendo todo en `EAGER`.

---

### Idea clave de entrevista
> JPA no es magia: hay que entender **qué queries genera**.

Un perfil mid:
👉 piensa en queries y performance, no solo en anotaciones.

---

### Errores comunes en entrevistas
- Usar `EAGER` para “arreglar” problemas
- No entender de dónde sale el N+1
- Cargar más datos de los necesarios
- No justificar decisiones de fetch

---

### Frase que suma muchos puntos
> “Prefiero `LAZY` por defecto y controlo la carga de datos según el caso.”

---
