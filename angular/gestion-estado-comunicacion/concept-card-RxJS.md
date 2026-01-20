**TARJETA DE ESTUDIO – RxJS en Angular (Observables y Subjects)**

---

## 📌 ¿Qué es RxJS?

**RxJS (Reactive Extensions for JavaScript)** es una librería para **programación reactiva** basada en **flujos de datos asíncronos**.

Angular la usa de forma nativa para:

* HTTP
* Eventos
* Formularios reactivos
* Comunicación entre componentes

---

## 🔄 Observables

Un **Observable** representa un **flujo de datos en el tiempo** (0, 1 o muchos valores).

### Características

* Lazy (no se ejecuta hasta `subscribe`)
* Puede emitir múltiples valores
* Maneja asincronía y eventos
* Cancelable (`unsubscribe`)

```ts
observable.subscribe(valor => {});
```

✔ Base del HTTP en Angular
✔ Ideal para streams y eventos

---

## 📡 Subjects

Un **Subject** es un tipo especial de Observable que:

* Emite valores manualmente
* Permite **multicast** (varios subscriptores)
* Actúa como Observable y Observer

```ts
subject.next(valor);
```

---

## 🧩 Tipos de Subjects

* **Subject**
  No guarda estado

* **BehaviorSubject**
  Guarda el último valor
  Requiere valor inicial
  ✔ Muy usado para estado compartido

* **ReplaySubject**
  Re-emite valores anteriores

---

## ⚙️ Operadores RxJS (Claves)

Permiten **transformar y controlar flujos**:

* `map` → transforma datos
* `filter` → filtra valores
* `switchMap` → cancela flujos previos
* `tap` → efectos secundarios
* `catchError` → manejo de errores

📍 Se encadenan con `pipe()`

---

## 🎯 Casos de Uso Comunes

* Llamadas HTTP
* Comunicación entre componentes
* Manejo de estado simple
* Eventos del usuario
* Tiempo real

---

## ⚠️ Buenas Prácticas

* Desuscribirse en `ngOnDestroy`
* Preferir `async` pipe cuando sea posible
* Usar `BehaviorSubject` para estado
* Evitar lógica compleja en componentes

---

## 📝 Nota para Full Stack

* RxJS es clave para Angular profesional
* Equivale a programación reactiva en backend
* Impacta directamente en rendimiento y escalabilidad

---

**Tip:** Si trabajas con datos que cambian en el tiempo, RxJS no es opcional: es la solución correcta.
