# **Arquitectura MVVM (Model–View–ViewModel)**

---

## ¿Qué es?

La **arquitectura MVVM** separa la aplicación en **Modelo, Vista y ViewModel**, facilitando la vinculación automática (*data binding*) entre la Vista y la lógica de presentación.

---

## Componentes

### Modelo (Model)

* Contiene los **datos** y la **lógica de negocio**.
* Es independiente de la interfaz de usuario.

### Vista (View)

* Interfaz gráfica que muestra la información.
* No contiene lógica de negocio.
* Se enlaza al ViewModel mediante *data binding*.

### ViewModel

* Expone datos y acciones de la Vista.
* No conoce directamente a la Vista.
* Convierte datos del Modelo en información presentable.

---

## Flujo de Funcionamiento

1. El usuario interactúa con la **Vista**.
2. La Vista se comunica con el **ViewModel** mediante *data binding*.
3. El ViewModel consulta o actualiza el **Modelo**.
4. Los cambios se reflejan automáticamente en la Vista.

---

## Características Principales

* Uso intensivo de **data binding**.
* Separación clara entre UI y lógica.
* Alta testabilidad del ViewModel.

---

## Ventajas

* Facilita pruebas unitarias.
* Reduce el código en la Vista.
* Ideal para interfaces complejas y reactivas.

---

## Desventajas

* Curva de aprendizaje.
* Dependencia del framework.
* Puede ser excesivo para apps simples.

---

## Cuándo Usarla

* Aplicaciones con UI rica y dinámica.
* Frameworks con *binding* nativo.
* Proyectos orientados a testabilidad.

---

## Ejemplos de Uso

* WPF / UWP (C#)
* Android (ViewModel + LiveData)
* Angular

---

## Comparación Rápida

* **MVVM**: Vista enlazada al ViewModel.
* **MVC**: Controlador gestiona la interacción.
* **MVP**: Vista comunica directamente con Presenter.

---

## Idea Clave

> MVVM elimina la lógica de la Vista usando **data binding** y ViewModels testables.
