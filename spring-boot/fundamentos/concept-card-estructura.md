# 🧠 TARJETA DE ESTUDIO – ESTRUCTURA DE UN PROYECTO SPRING BOOT (A6)

### ¿Cómo se organiza un proyecto Spring Boot?
Spring Boot sigue una **estructura por capas** y **convenciones claras** para que el proyecto sea:
- fácil de entender
- fácil de mantener
- fácil de escalar

Idea clave:
👉 *Spring Boot espera que ordenes el código de una forma concreta.*

---

### Clase principal (`@SpringBootApplication`)
- Es el **punto de entrada** de la aplicación
- Contiene el método `main`
- Arranca el contexto de Spring

Función principal:
👉 iniciar la aplicación y escanear componentes.

Buena práctica:
> esta clase suele estar en el **paquete raíz**.

---

### Paquetes más comunes

#### `controller`
- Recibe las peticiones HTTP
- Devuelve respuestas
- **No** contiene lógica de negocio

👉 solo orquesta entrada y salida.

---

#### `service`
- Contiene la **lógica de negocio**
- Aplica reglas del dominio
- Coordina repositorios

👉 aquí vive “lo importante”.

---

#### `repository`
- Acceso a base de datos
- Interfaces JPA
- Sin lógica de negocio

👉 solo persistencia.

---

### Convención sobre configuración
Spring Boot:
- Detecta clases por anotaciones
- Auto-configura componentes comunes
- Reduce configuración manual

Idea clave:
> si sigues la estructura estándar, Spring Boot “hace lo correcto” por defecto.

---

### ¿Por qué esta estructura importa? (entrevista)
- Facilita lectura del proyecto
- Evita mezclar responsabilidades
- Permite testing más simple
- Hace el proyecto escalable

---

### Errores comunes en entrevistas
- Lógica de negocio en controllers
- Repositorios con lógica compleja
- Paquetes sin orden
- Clase principal en un paquete incorrecto

---

### Frase que suma puntos
> “En Spring Boot, cada capa tiene una responsabilidad clara.”

---
