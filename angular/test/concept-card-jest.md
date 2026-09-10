# **Testing con Jest**

---

## ¿Qué es Jest?

**Jest** es un **framework de testing para JavaScript** desarrollado por Meta, muy usado para probar **aplicaciones frontend y backend**, especialmente con **React y Node.js**.

---

## Idea Clave

> Jest permite **verificar automáticamente** que el código funciona como se espera.

---

## Tipos de Tests en Jest

### Tests Unitarios

* Prueban funciones o componentes individuales.

### Tests de Integración

* Verifican la interacción entre módulos.

---

## Conceptos Básicos

* **test / it** → define una prueba
* **expect** → resultado esperado
* **matchers** → comparaciones (`toBe`, `toEqual`)

---

## Ejemplo Básico

```javascript
function suma(a, b) {
  return a + b;
}

test('suma dos números', () => {
  expect(suma(2, 3)).toBe(5);
});
```

---

## Matchers Comunes

* `toBe()` → igualdad estricta
* `toEqual()` → igualdad de objetos
* `toBeTruthy()` / `toBeFalsy()`
* `toContain()`

---

## Mocks y Spies

### ¿Qué son?

Simulan dependencias externas.

```javascript
jest.fn();
jest.spyOn(obj, 'metodo');
```

---

## Ventajas

* Configuración mínima.
* Ejecución rápida.
* Soporte de mocks integrado.

---

## Desventajas

* No ideal para tests end‑to‑end.
* Puede ocultar errores si se abusa de mocks.

---

## Cuándo Usar Jest

* Proyectos JavaScript.
* Aplicaciones React.
* APIs con Node.js.

---

## Comparación Rápida

* **Jest**: completo, todo en uno.
* **Mocha + Chai**: más modular.

---

## Idea Clave Final

> Jest facilita crear **tests automáticos rápidos y fiables**.
