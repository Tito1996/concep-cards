## 🧠 TARJETA DE ESTUDIO – CONFIGURACIÓN BÁSICA (SPRING BOOT) (A6)

### ¿Dónde se configura Spring Boot?
La configuración principal vive en:
- `application.properties`
- `application.yml`

Ahí se definen **valores de entorno** y **comportamiento de la app**.

Idea clave:
👉 *la configuración va fuera del código.*

---

### ¿Por qué es importante la configuración?
Permite:
- Cambiar comportamiento sin recompilar
- Adaptar la app a distintos entornos (dev, test, prod)
- Evitar valores hardcodeados

En entrevistas:
👉 evalúan si sabes **dónde y por qué** configurar cosas.

---

### Puerto de la aplicación
Define **en qué puerto escucha el servidor**.

Concepto:
- La app levanta un servidor embebido
- El puerto puede cambiar según el entorno

Uso típico:
👉 evitar conflictos o cumplir reglas de infraestructura.

Error común:
🚨 pensar que el puerto es “parte del código”.

---

### Conexión a base de datos
La configuración incluye:
- URL de la base de datos
- Usuario
- Contraseña
- Driver

Idea clave:
> Spring Boot usa esta info para crear automáticamente la conexión.

La app **no debería saber** estos valores directamente.

---

### Regla de oro (entrevista 🚨)
> **Nunca hardcodear datos sensibles en el código.**

La configuración:
- se externaliza
- se versiona con cuidado
- puede variar por entorno

---

### Errores comunes en entrevistas
- No saber dónde se configura la DB
- Mezclar configuración con lógica
- Hardcodear usuario/clave
- No entender para qué sirve `application.properties`

---

### Buena práctica
- Usar `application.properties` / `yml`
- Separar configuración por entorno
- Mantener el código independiente del entorno

---

### Frase que suma puntos
> “Spring Boot se adapta al entorno a través de configuración, no cambiando el código.”

---
