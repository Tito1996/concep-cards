# **Clean Architecture**

---

## ¿Qué es?

La **Clean Architecture** es un estilo arquitectónico que organiza el software en **capas concéntricas**, donde las **dependencias siempre apuntan hacia el dominio**, manteniendo la lógica de negocio independiente de frameworks, UI y bases de datos.

---

## Objetivo Principal

* Proteger la lógica de negocio.
* Lograr independencia de frameworks y tecnologías.
* Facilitar mantenimiento, pruebas y evolución del sistema.

---

## Regla Fundamental

> **Las dependencias solo pueden ir hacia adentro**, nunca hacia afuera.

---

## Capas Principales

### Entidades (Entities)

* Reglas de negocio más generales.
* Independientes del sistema.

### Casos de Uso (Use Cases)

* Lógica específica de la aplicación.
* Orquestan las entidades.

### Adaptadores de Interfaz

* Controladores, presenters, gateways.
* Conectan el dominio con el exterior.

### Frameworks & Drivers

* UI, base de datos, frameworks, APIs externas.
* Detalles técnicos intercambiables.

---

## Flujo de Funcionamiento

1. La UI envía una solicitud.
2. Un controlador la adapta a un caso de uso.
3. El caso de uso ejecuta la lógica.
4. El resultado vuelve adaptado a la UI.

---

## Ventajas

* Alta mantenibilidad.
* Dominio altamente testeable.
* Fácil cambio de tecnologías.

---

## Desventajas

* Mayor complejidad inicial.
* Más código estructural.
* Curva de aprendizaje.

---

## Cuándo Usarla

* Proyectos grandes o de larga vida.
* Sistemas con lógica de negocio compleja.
* Equipos que priorizan calidad y testeo.

---

## Comparación Rápida

* **Clean Architecture**: dependencias estrictas hacia el dominio.
* **Hexagonal**: dominio central con puertos.
* **Capas**: dependencias jerárquicas.

---

## Idea Clave Final

> El software debe depender de **políticas de negocio**, no de detalles técnicos.
