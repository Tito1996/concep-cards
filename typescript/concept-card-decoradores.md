**TARJETA DE ESTUDIO – Decoradores en TypeScript**

---

## 📌 ¿Qué es un Decorador en TypeScript?

Un **decorador** es una **función especial** que se usa para **añadir metadatos o modificar el comportamiento** de clases y sus miembros **en tiempo de diseño**, no en ejecución directa.

Son una característica avanzada usada para **arquitectura y metaprogramación**.

---

## 🧩 Tipos de Decoradores en TypeScript

### 🧱 Decorador de Clase

Se aplica a una clase completa.

**Uso común:**

* Añadir metadatos
* Modificar o extender la clase

```ts
function Logger(constructor: Function) {}
```

---

### 🧰 Decorador de Propiedad

Se aplica a atributos de una clase.

**Uso común:**

* Validaciones
* Configuración
* Metadatos

```ts
function Required(target: any, propertyKey: string) {}
```

---

### 🧠 Decorador de Método

Se aplica a métodos.

**Uso común:**

* Logging
* Control de acceso
* Medición de ejecución

```ts
function Log(target: any, key: string, descriptor: PropertyDescriptor) {}
```

---

### 🧾 Decorador de Parámetro

Se aplica a parámetros de un método.

**Uso común:**

* Metadatos
* Validaciones específicas

---

## ⚙️ Características Clave

* Se ejecutan al **definirse la clase**
* No forman parte del estándar JavaScript (experimental)
* Requieren configuración (`experimentalDecorators`)
* Muy usados por frameworks

---

## 🎯 ¿Para qué sirven?

* Separar configuración de lógica
* Aplicar comportamiento reutilizable
* Evitar código repetitivo
* Facilitar arquitecturas declarativas

---

## ⚠️ Buenas Prácticas

* Usarlos con moderación
* No abusar para lógica de negocio
* Mantenerlos simples y claros
* Documentarlos bien

---

## 📝 Nota para Full Stack

* Angular, NestJS y otros frameworks se basan en decoradores
* Entenderlos mejora la comprensión del framework
* Clave para arquitectura avanzada en TypeScript

---

**Tip:** Si un decorador contiene mucha lógica, probablemente debería ser un servicio o una función independiente.
