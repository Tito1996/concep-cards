## 🧠 TARJETA DE ESTUDIO – BUENAS PRÁCTICAS BACKEND

### ¿Qué son las buenas prácticas backend?
Son **decisiones técnicas** que hacen que una API sea:
- fácil de mantener
- fácil de entender
- segura
- confiable en producción

Idea clave:
👉 *no se trata solo de que funcione, sino de que sea sostenible.*

---

### 🔍 Logs útiles
Los logs deben:
- ayudar a entender qué pasó
- servir para debug en producción
- aportar contexto (qué, cuándo, dónde)

Buenas prácticas:
- loggear eventos importantes
- evitar logs innecesarios
- no loggear datos sensibles

Idea clave:
> Un buen log responde “qué pasó” sin leer el código.

---

### ⚠️ Manejo de errores claro
Un backend sólido:
- maneja errores de forma controlada
- devuelve códigos HTTP correctos
- no expone detalles internos

Buenas prácticas:
- errores consistentes
- mensajes claros
- centralizar manejo de excepciones

👉 los errores **también son parte del flujo normal**.

---

### 🔁 APIs predecibles
Una API predecible:
- usa los mismos formatos de response
- respeta códigos HTTP
- se comporta igual ante casos similares

Beneficio:
👉 el cliente sabe qué esperar sin adivinar.

---

### 🧪 Código testeable
Código testeable es código que:
- tiene responsabilidades claras
- depende poco de implementaciones concretas
- puede probarse sin levantar todo el sistema

Buenas prácticas:
- lógica en services
- dependencias inyectadas
- métodos pequeños y claros

Idea clave:
> Si es difícil de testear, está mal diseñado.

---

### Diferencia clave junior vs mid
- **Junior:** el backend funciona  
- **Mid:** el backend es mantenible, predecible y confiable  

Esto **define seniority** en entrevistas.

---

### Errores comunes en entrevistas
- No pensar en logs
- Tratar errores como excepciones raras
- APIs inconsistentes
- Código imposible de testear

---

### Frase que suma muchos puntos
> “Un buen backend es claro para humanos, no solo para máquinas.”

---
