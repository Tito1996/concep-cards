**TARJETA DE ESTUDIO – Asincronía en TypeScript**
**Tema:** Promises y Observables

---

## 📌 ¿Qué es la Asincronía?

La asincronía permite **ejecutar tareas que no se completan de inmediato** (HTTP, timers, I/O) **sin bloquear** la ejecución del programa.

Es fundamental en aplicaciones web modernas.

---

## 🔹 Promises

Representan **un único valor futuro** (éxito o error).

### Estados

* `pending` → en proceso
* `fulfilled` → resuelta
* `rejected` → fallida

### Uso típico

```ts
fetchData()
  .then(data => {})
  .catch(error => {});
```

### Características

✔ Se ejecutan una vez
✔ Simples de usar
❌ No cancelables
❌ Poco flexibles para flujos complejos

---

## 🔹 async / await

Sintaxis moderna sobre Promises.

```ts
async function cargar() {
  const data = await fetchData();
}
```

✔ Código más legible
✔ Manejo claro de errores (`try/catch`)
📍 Recomendado para lógica secuencial

---

## 🔸 Observables

Representan **flujos de datos en el tiempo** (0, 1 o muchos valores).

Muy usados con **RxJS**.

### Características

* Emiten múltiples valores
* Se pueden cancelar (`unsubscribe`)
* Soportan operadores (`map`, `filter`, `switchMap`)

```ts
observable.subscribe(valor => {});
```

✔ Muy potentes
✔ Ideales para eventos y streams
❌ Curva de aprendizaje mayor

---

## 🧠 Comparación Rápida

* **Promise:** un solo resultado
* **Observable:** múltiples valores
* **Promise:** eager (se ejecuta sola)
* **Observable:** lazy (se ejecuta al subscribirse)

---

## 🎯 ¿Cuándo usar cada uno?

* **Promise / async-await:**
  → Lógica simple, llamadas únicas

* **Observable:**
  → HTTP en Angular, eventos, streams, tiempo real

---

## ⚠️ Buenas Prácticas

* Preferir `async/await` con Promises
* Desuscribirse siempre de Observables
* Evitar mezclar Promises y Observables sin criterio
* Manejar errores explícitamente

---

## 📝 Nota para Full Stack

* TypeScript + asincronía = base de Angular
* Backend Java trabaja de forma similar (async / reactive)
* Clave para rendimiento y UX

---

**Tip:** Si necesitas cancelar, transformar o combinar flujos de datos, no uses Promises: usa Observables.
