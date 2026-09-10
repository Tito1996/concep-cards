**TARJETA DE ESTUDIO – Ciclo de Vida de Componentes (Angular)**

---

## 📌 ¿Qué es el Ciclo de Vida de un Componente?

Conjunto de **etapas por las que pasa un componente Angular** desde que se crea hasta que se destruye.
Angular expone estas etapas mediante **hooks** (métodos especiales).

---

## 🔄 Hooks Principales

### 🟢 `ngOnInit()`

* Se ejecuta **una sola vez** al iniciar el componente
* Ideal para:

  * Cargar datos iniciales
  * Llamar APIs
  * Inicializar lógica

✔ Hook más usado

---

### 🔁 `ngOnChanges()`

* Se ejecuta cuando **cambian los @Input()**
* Recibe los valores anteriores y nuevos

✔ Útil para reaccionar a cambios externos

---

### 👀 `ngDoCheck()`

* Detecta cambios manualmente
* Se ejecuta con mucha frecuencia

⚠️ Usar con cuidado (impacta rendimiento)

---

### 🧱 `ngAfterViewInit()`

* Se ejecuta cuando la **vista y sus hijos están listos**
* Ideal para acceder al DOM o ViewChild

---

### 🔄 `ngAfterContentInit()`

* Se ejecuta cuando el contenido proyectado (`ng-content`) está listo

---

### 🔴 `ngOnDestroy()`

* Se ejecuta antes de destruir el componente
* Ideal para:

  * Cancelar suscripciones
  * Liberar recursos
  * Evitar memory leaks

✔ Muy importante en Observables

---

## 🧠 Orden Simplificado

1. Constructor
2. `ngOnChanges()`
3. `ngOnInit()`
4. Hooks de vista/contenido
5. `ngOnDestroy()`

---

## 🎯 Buenas Prácticas

* Lógica inicial → `ngOnInit`
* Limpieza → `ngOnDestroy`
* Evitar lógica pesada en hooks frecuentes
* Desuscribirse siempre de Observables

---

## 📝 Nota para Full Stack

* Clave para manejar datos asincrónicos
* Fundamental para rendimiento y estabilidad
* Evita errores comunes en SPAs grandes

---

**Tip:** Si tienes memory leaks en Angular, revisa primero `ngOnDestroy()`.
