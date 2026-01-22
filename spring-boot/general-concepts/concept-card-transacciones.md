## 🧠 TARJETA DE ESTUDIO – TRANSACCIONES (`@Transactional`)

### ¿Qué es una transacción?
Una transacción es un **conjunto de operaciones** que se ejecutan como **una sola unidad**.

En simple:
👉 *o se hacen todas, o no se hace ninguna.*

---

### Objetivo principal
Garantizar **consistencia de datos**.

Si algo falla en el proceso:
- no quedan datos a medias
- no hay estados inconsistentes

Esto es **crítico en sistemas reales**.

---

### `@Transactional`
`@Transactional` le indica a Spring que:
- inicie una transacción al entrar al método
- confirme los cambios si todo va bien
- haga **rollback** si ocurre un error

Idea clave:
> La transacción se maneja automáticamente.

---

### Atomicidad (concepto clave)
La atomicidad significa:
👉 *el proceso se ejecuta completo o se deshace completo.*

Ejemplo mental:
- guardar un pedido
- descontar stock
- registrar pago  

Si falla uno:
👉 **no se guarda nada**.

---

### Consistencia de datos
Las transacciones aseguran que:
- la base de datos pase de un estado válido a otro
- nunca quede en un estado intermedio inválido

Esto protege:
- reglas del negocio
- integridad del sistema

---

### ¿Dónde usar `@Transactional`? (MUY preguntado)
Un perfil mid sabe que:
- Se usa **en el service**
- No en el controller
- No en el repository (salvo casos muy específicos)

Regla práctica:
> La transacción envuelve la lógica de negocio.

---

### ¿Qué errores hacen rollback?
Por defecto:
- Excepciones **no controladas** (`RuntimeException`)

Idea clave:
👉 no todos los errores hacen rollback automáticamente.

---

### Errores comunes en entrevistas
- No saber qué es una transacción
- Usar `@Transactional` “por las dudas”
- Ponerlo en el controller
- No entender rollback

---

### Frase que suma muchos puntos
> “Uso transacciones para asegurar atomicidad y consistencia de datos en la lógica de negocio.”

---
