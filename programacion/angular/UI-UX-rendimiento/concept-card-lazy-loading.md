**TARJETA DE ESTUDIO – Lazy Loading de Módulos en Angular**

---

## 📌 ¿Qué es Lazy Loading?

El **Lazy Loading** es una técnica que permite **cargar módulos solo cuando se necesitan**, en lugar de cargar toda la aplicación al inicio.

Mejora **rendimiento**, **tiempo de carga inicial** y **escalabilidad**.

---

## 🚀 ¿Cómo funciona?

* Angular carga inicialmente solo el **módulo raíz**
* Los **módulos lazy** se cargan al navegar a su ruta
* Se descargan como **chunks independientes**

📍 Basado en el sistema de **Routing**

---

## 🧱 Módulos Lazy

Un módulo puede marcarse como lazy si:

* Tiene su propio `RoutingModule`
* Se carga usando `loadChildren`

✔ Separación por funcionalidades
✔ Mejor organización del código

---

## 🧭 Configuración Básica

* Ruta con `loadChildren`
* Import dinámico del módulo
* Eliminación de imports directos en `AppModule`

📍 Un módulo lazy **no se importa** en el módulo raíz

---

## 🎯 Beneficios Clave

* Menor bundle inicial
* Carga más rápida
* Mejor experiencia de usuario
* Escalabilidad en aplicaciones grandes

---

## ⚠️ Consideraciones Importantes

* Evitar servicios singleton duplicados
* Cuidar el scope de los servicios
* No usar Lazy Loading para módulos pequeños sin sentido
* Requiere una buena estructura de rutas

---

## 📝 Buenas Prácticas

* Lazy Loading por **feature**
* Combinar con **Guards**
* Usar **PreloadingStrategy** para módulos críticos
* Mantener módulos cohesionados

---

## 📝 Nota para Full Stack

* Ideal para aplicaciones empresariales
* Reduce carga innecesaria al backend
* Mejora UX en SPAs complejas

---

**Tip:**
Si tu aplicación Angular crece y no usas Lazy Loading, el problema no es el rendimiento: es la arquitectura.
