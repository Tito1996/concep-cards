## 🧠 TARJETA DE ESTUDIO – SEGURIDAD BÁSICA (SPRING / BACKEND) (A6)

### ¿Qué es la seguridad en una aplicación?
La seguridad protege el sistema para que:
- solo **usuarios válidos** accedan
- solo **acciones permitidas** se ejecuten
- los datos estén protegidos

En simple:
👉 *no cualquiera puede hacer cualquier cosa.*

---

### Spring Security (conceptual)
Spring Security es el **framework de Spring** para manejar:
- autenticación
- autorización
- control de acceso

Idea clave (entrevista):
👉 *Spring Security se encarga de la seguridad transversal del sistema.*

---

### Autenticación vs Autorización (MUY preguntado 🚨)

#### 🔐 Autenticación
Responde a:
> **¿Quién sos?**

Ejemplos:
- login con usuario/contraseña
- token JWT válido

👉 verifica la **identidad** del usuario.

---

#### 🛂 Autorización
Responde a:
> **¿Qué podés hacer?**

Ejemplos:
- acceder a un endpoint
- ejecutar una acción específica

👉 depende de **roles o permisos**.

---

### Diferencia clave (entrevista)
> Autenticación ≠ Autorización  

Primero:
👉 te identificas (autenticación)  
Después:
👉 se valida qué acciones puedes realizar (autorización)

---

### Roles
Un **rol** representa un conjunto de permisos.

Ejemplos comunes:
- `USER`
- `ADMIN`
- `MODERATOR`

Uso típico:
👉 restringir endpoints o acciones según el rol.

---

### Manejo básico de roles
A nivel conceptual:
- Cada usuario tiene uno o más roles
- El sistema verifica el rol antes de permitir una acción

Ejemplo mental:
👉 solo `ADMIN` puede borrar usuarios.

---

### Regla de oro (entrevista 🚨)
> **No todos los usuarios deben tener los mismos permisos.**

La seguridad:
- se diseña
- no se asume

---

### Errores comunes en entrevistas
- Confundir autenticación con autorización
- Pensar que seguridad es solo login
- No considerar roles
- Proteger todo o nada (sin criterio)

---

### Buena práctica
- Autenticar al usuario
- Autorizar según roles
- Proteger solo lo necesario
- Mantener reglas claras

---

### Frase que suma muchos puntos
> “Primero autentico al usuario y luego autorizo sus acciones según su rol.”

---
