# TARJETA DE ESTUDIO – Logging y Monitoreo en Spring Boot


## 📌 ¿Qué es Logging?

El **logging** es el registro de **eventos y mensajes** generados por la aplicación para:

* Diagnosticar errores
* Analizar comportamiento
* Auditar operaciones
* Facilitar soporte y mantenimiento

📍 Es fundamental en **entornos productivos**

---

## ☕ Logging en Spring Boot

Spring Boot incluye logging **listo para usar** basado en:

* **SLF4J** → API de logging
* **Logback** → implementación por defecto

📍 No requiere configuración inicial

---

## 🧱 Niveles de Log

* `TRACE` → muy detallado (debug profundo)
* `DEBUG` → información técnica
* `INFO` → flujo normal de la aplicación
* `WARN` → situaciones inesperadas
* `ERROR` → fallos críticos

📍 Elegir bien el nivel evita ruido innecesario

---

## 🛠️ Uso Básico en Código

* Un logger por clase
* Mensajes claros y contextuales
* Nunca usar `System.out.println`

📍 El log es parte del diseño, no un parche

---

## ⚠️ Errores Comunes en Logging

* Loggear información sensible (passwords, tokens)
* Usar `ERROR` para todo
* Logs excesivos en producción
* Mensajes poco claros
* Falta de contexto (ids, usuario, operación)

---

## 📊 ¿Qué es Monitoreo?

El **monitoreo** permite observar el **estado y salud** de la aplicación en tiempo real.

Incluye:

* Estado de la app
* Métricas
* Salud de dependencias
* Rendimiento

---

## 🩺 Monitoreo en Spring Boot

Spring Boot ofrece **Spring Boot Actuator**.

Proporciona endpoints como:

* `/actuator/health`
* `/actuator/metrics`
* `/actuator/info`
* `/actuator/env`

📍 Clave para operaciones y DevOps

---

## 🔍 Métricas Importantes

* Uso de memoria
* CPU
* Requests por segundo
* Tiempo de respuesta
* Errores 4xx / 5xx

📍 Base para alertas y escalado

---

## 🎯 Buenas Prácticas

* Logging claro, conciso y consistente
* Separar logs por entorno (dev / prod)
* Usar `INFO` para flujo normal
* Centralizar logs (ELK, Grafana, etc.)
* Proteger endpoints de Actuator
* Usar monitoreo desde el primer despliegue

---

## 📝 Nota para Spring Boot

* Logs explican **qué pasó**
* Monitoreo muestra **cómo está**
* Sin ambos, producir bugs es inevitable
* Son esenciales para microservicios y cloud

---

**Tip:**
Si no puedes saber **qué pasó** ni **cómo está tu app** sin depurar código, tu backend **no está listo para producción**.
