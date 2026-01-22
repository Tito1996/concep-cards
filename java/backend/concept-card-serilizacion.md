# TARJETA DE ESTUDIO – Serialización (JSON)


## 📌 ¿Qué es la Serialización?

La **serialización** es el proceso de **convertir un objeto en un formato de texto** para poder **transmitirlo o almacenarlo**.
En aplicaciones web, el formato más común es **JSON**.

✔ Objeto → JSON
✔ Reversible (deserialización)

---

## 🔄 Deserialización

Proceso inverso:

* **JSON → Objeto**

📍 Frontend y backend realizan ambos procesos constantemente.

---

## 🧱 ¿Qué es JSON?

**JSON (JavaScript Object Notation)** es un formato:

* Ligero
* Legible
* Independiente del lenguaje

**Ejemplo:**

```json
{
  "id": 1,
  "nombre": "Ana",
  "activo": true
}
```

---

## 🧠 Uso en Aplicaciones Web

* Enviar datos por APIs REST
* Respuestas HTTP
* Requests desde frontend
* Persistencia temporal

📍 JSON es el **contrato de datos** entre sistemas

---

## ☕ Serialización en Backend (Java)

* Convierte **POJOs → JSON**
* Librerías comunes:

  * Jackson
  * Gson

✔ Automática en frameworks modernos
✔ Basada en getters/setters y anotaciones

---

## 🅰️ Serialización en Frontend (Angular)

* Convierte **objetos TypeScript → JSON**
* Uso implícito en `HttpClient`

✔ Transparente para el desarrollador
✔ Basada en objetos JS/TS

---

## ⚠️ Consideraciones Importantes

* Tipos deben coincidir frontend–backend
* Fechas y formatos requieren cuidado
* Campos sensibles deben excluirse
* Evitar objetos circulares

---

## 🎯 Buenas Prácticas

* Usar DTOs para serialización
* Mantener nombres claros y consistentes
* Versionar contratos JSON
* Validar datos al deserializar
* Documentar la estructura

---

## 📝 Nota para Full Stack

* JSON conecta Angular ↔ Java
* Errores de serialización rompen la comunicación
* Clave para APIs REST robustas

---

**Tip:**
Si el frontend y el backend no “se entienden”, revisa primero la **serialización JSON** antes que la lógica.
