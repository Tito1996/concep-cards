## 🧠 TARJETA DE ESTUDIO – DTOs Y MAPEO (SPRING / BACKEND)

### ¿Qué es un DTO?
Un **DTO (Data Transfer Object)** es un objeto que se usa **solo para transportar datos** entre capas o hacia el exterior (API).

En simple:
👉 *es el contrato de datos de la API.*

---

### ¿Por qué NO exponer entidades?
Las **entidades JPA**:
- Representan el **modelo interno**
- Están acopladas a la base de datos
- Tienen relaciones, lazy loading y detalles técnicos

Exponerlas:
🚨 rompe encapsulamiento  
🚨 acopla la API a la DB  
🚨 genera problemas de performance y seguridad

---

### Uso correcto de DTOs (perfil mid)
Un perfil mid:
- Usa **DTOs de request** para recibir datos
- Usa **DTOs de response** para devolver datos
- Mantiene las entidades **solo en la capa de dominio/persistencia**

Idea clave:
> *La entidad no es el contrato de la API.*

---

### Beneficios de usar DTOs
- Control total de lo que se expone
- Evita problemas de `LAZY` y N+1
- Permite cambiar el modelo interno sin romper la API
- Responses más claras y estables
- Mejor testing

---

### ¿Qué es el mapeo?
El **mapeo** es el proceso de convertir:
- DTO → Entidad (al entrar)
- Entidad → DTO (al salir)

Se puede hacer:
- Manualmente (claro y explícito)
- Con librerías (cuando el proyecto lo justifica)

Lo importante en entrevista:
👉 **entender el porqué**, no la herramienta.

---

### Regla de oro (entrevista 🚨)
> **Nunca devolver entidades JPA desde un controller.**

Si el entrevistador insiste:
👉 es una pregunta trampa.

---

### Errores comunes en entrevistas
- Devolver entidades “por rapidez”
- Usar el mismo DTO para todo
- Mapear lógica de negocio en el DTO
- No saber explicar por qué existen los DTOs

---

### Frase que suma muchos puntos
> “Uso DTOs para desacoplar la API del modelo interno y tener control sobre lo que expongo.”

---
