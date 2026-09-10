## 🧠 TARJETA DE ESTUDIO – ESTRUCTURAS DE DATOS BÁSICAS (A6)

### ¿Qué es una estructura de datos?

Es una forma de **organizar y almacenar datos** para poder:

* buscarlos
* recorrerlos
* modificarlos
  de manera eficiente y clara.

En simple:
👉 *define cómo guardo los datos y cómo los uso.*

---

### Las más comunes (entrevista)

#### 📋 Lista / Array / List

Se usa cuando:

* Importa el **orden**
* Recorres los elementos completos
* Accedes por posición

Características:

* Fácil de recorrer
* Búsqueda lenta si no conoces la posición
* Permite duplicados

---

#### 🗂️ Mapa / Diccionario / Map

Se usa cuando:

* Necesitas buscar por una **clave**
* Quieres acceso rápido a un valor
* La relación es clave → valor

Características:

* Búsqueda rápida por clave
* No depende del orden
* Claves únicas

---

### Pregunta típica de entrevista

> “¿Cuándo usarías una lista y cuándo un mapa?”

Respuesta correcta:

> “Uso lista cuando necesito recorrer u ordenar; uso mapa cuando necesito buscar rápido por una clave.”

---

### Impacto en operaciones (criterio)

* **Buscar**

  * Lista → recorrer uno por uno
  * Mapa → acceso directo por clave
* **Insertar**

  * Lista → simple
  * Mapa → simple, pero clave única
* **Recorrer**

  * Lista → natural
  * Mapa → recorrer claves/valores

No hace falta Big-O:
👉 **solo entender el impacto práctico**.

---

### Error común en entrevistas

* Usar listas para búsquedas frecuentes
* Usar mapas cuando solo recorres datos
* Elegir por costumbre, no por necesidad

---

### Buena práctica

Elegir la estructura según:

* cómo se accede a los datos
* qué operación es más frecuente
* claridad del código

---

### Frase que suma puntos

> “La estructura correcta simplifica el código y mejora el rendimiento.”

---
