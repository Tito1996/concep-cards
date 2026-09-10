## 🧠 TARJETA DE ESTUDIO – ESTRUCTURA BÁSICA DE UN PROGRAMA JAVA

### ¿Cómo está organizado un programa Java?

En Java, **todo el código vive dentro de clases**.
No existen funciones sueltas como en otros lenguajes.

Idea clave:
👉 *si no está dentro de una clase, no existe para Java.*

---

### ¿Qué es una clase?

Una clase es un **contenedor** que agrupa:

* Datos (atributos)
* Comportamiento (métodos)

En un programa simple, la clase principal:
👉 contiene el punto de inicio de la aplicación.

---

### ¿Qué es el método `main`?

El método `main` es el **punto de entrada** del programa.

Es lo primero que Java ejecuta cuando arrancas la aplicación.

Conceptualmente:
👉 *“Java empieza a ejecutar desde `main`.”*

---

### ¿Para qué sirve `main`?

* Iniciar la aplicación
* Crear objetos
* Llamar a otros métodos
* Coordinar el flujo inicial

No debería contener lógica compleja.

---

### ¿Cómo se ejecuta un programa Java?

1. El código se **compila** (`.java` → `.class`)
2. La JVM busca el método `main`
3. Empieza la ejecución desde ahí
4. El programa termina cuando `main` finaliza

---

### Idea clave de entrevista

> Java no ejecuta clases, **ejecuta el método `main`** de una clase.

---

### Errores comunes de junior

* Pensar que cualquier método se ejecuta solo
* Poner toda la lógica en `main`
* No entender por dónde empieza el programa

---

### Buena práctica

Usar `main` solo para:

* arrancar
* delegar
* coordinar

La lógica real va en otros métodos/clases.

---

### Frase que suma puntos

> “El método `main` arranca la aplicación, no contiene la lógica del negocio.”

---
