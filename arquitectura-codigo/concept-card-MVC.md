# **Arquitectura MVC (Model–View–Controller)**

---

## ¿Qué es?

La **arquitectura MVC** divide una aplicación en tres componentes principales: **Modelo, Vista y Controlador**, separando la lógica de negocio de la interfaz de usuario.

---

## Componentes

### Modelo (Model)

* Contiene los **datos** y la **lógica de negocio**.
* Gestiona el estado de la aplicación.
* No depende de la Vista.

### Vista (View)

* Muestra la información al usuario.
* Representa los datos del Modelo.
* No contiene lógica de negocio.

### Controlador (Controller)

* Recibe las acciones del usuario.
* Coordina Modelo y Vista.
* Decide qué Vista mostrar.

---

## Flujo de Funcionamiento

1. El usuario interactúa con la **Vista**.
2. La Vista envía la acción al **Controlador**.
3. El Controlador actualiza el **Modelo**.
4. El Modelo cambia su estado.
5. La Vista se actualiza con los nuevos datos.

---

## Ventajas

* Separación clara de responsabilidades.
* Facilita el mantenimiento y las pruebas.
* Permite desarrollo en paralelo.

---

## Desventajas

* Puede aumentar la complejidad.
* Controladores demasiado grandes.
* No siempre adecuado para apps pequeñas.

---

## Cuándo Usarla

* Aplicaciones web.
* Interfaces gráficas.
* Proyectos con múltiples vistas.

---

## Ejemplos de Uso

* Spring MVC
* ASP.NET MVC
* Ruby on Rails

---

## Comparación Rápida

* **MVC**: separación Modelo–Vista–Controlador.
* **Capas**: separación lógica general.
* **MVVM**: binding entre vista y modelo.

---

## Idea Clave

> MVC separa **qué se muestra**, **qué se hace** y **qué datos se manejan**.
