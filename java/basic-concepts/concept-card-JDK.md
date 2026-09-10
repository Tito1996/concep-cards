# TARJETA DE ESTUDIO – JVM, JDK y JRE (Java)


## 📌 Visión General

En el ecosistema Java existen **tres componentes clave** que cumplen roles distintos pero complementarios:

**JVM** → ejecuta
**JRE** → ejecuta + librerías
**JDK** → desarrolla + ejecuta

---

## 🧠 JVM – Java Virtual Machine

Es la **máquina virtual** que ejecuta el **bytecode Java**.

### Funciones principales

* Ejecutar `.class`
* Gestión de memoria (Heap, Stack)
* Garbage Collection
* Independencia del sistema operativo

✔ “Write once, run anywhere”
✔ No incluye herramientas de desarrollo

---

## 📦 JRE – Java Runtime Environment

Entorno necesario para **ejecutar aplicaciones Java**.

### Incluye

* JVM
* Librerías estándar de Java
* Archivos de soporte

✔ Sirve para **usuarios finales**
❌ No permite compilar código

---

## 🛠️ JDK – Java Development Kit

Kit completo para **desarrollar aplicaciones Java**.

### Incluye

* JRE (y JVM)
* Compilador `javac`
* Debugger
* Herramientas de build y análisis

✔ Necesario para programar en Java
✔ Usado por desarrolladores

---

## 🔁 Relación entre ellos

* **JDK** ⟶ incluye **JRE**
* **JRE** ⟶ incluye **JVM**
* **JVM** ⟶ ejecuta el bytecode

---

## 🧭 ¿Cuál necesito?

* Ejecutar una app Java → **JRE**
* Desarrollar en Java → **JDK**
* Ejecutar bytecode → **JVM** (implícita)

📍 En la práctica, los desarrolladores **instalan solo JDK**

---

## 📝 Nota para Full Stack

* Backend Java (Spring, APIs) requiere JDK
* Entender JVM ayuda a optimizar rendimiento
* Base para despliegues y contenedores

---

**Tip:**
Si compilas código Java, necesitas **JDK**.
Si solo lo ejecutas, basta con **JRE**.
