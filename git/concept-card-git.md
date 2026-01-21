**TARJETA DE ESTUDIO – Git: Branching, Merge y Rebase**

---

## 📌 ¿Qué es Git?

Sistema de **control de versiones distribuido** que permite gestionar cambios en el código y colaborar en equipo de forma segura.

---

## 🌿 Branching (Ramas)

Permite trabajar en **líneas de desarrollo independientes**.

* `main / master` → código estable
* `develop` → integración
* `feature/*` → nuevas funcionalidades
* `hotfix/*` → correcciones urgentes

✔ Desarrollo paralelo
✔ Aislamiento de cambios
✔ Flujo de trabajo ordenado

---

## 🔀 Merge

**Une una rama con otra** conservando el historial.

* Crea un *merge commit*
* Mantiene la historia completa
* Puede generar conflictos

✔ Seguro
✔ Ideal para trabajo en equipo
❌ Historial más ruidoso

**Uso común:**
`feature → develop`
`develop → main`

---

## 🔁 Rebase

**Reaplica commits sobre otra rama**, reescribiendo el historial.

* Historial lineal y limpio
* No crea merge commits
* Modifica commits existentes

✔ Historial claro
❌ Riesgoso en ramas compartidas

⚠️ No usar rebase en ramas públicas

---

## 🧠 Diferencia Clave

* **Merge:** preserva historia
* **Rebase:** limpia historia

---

## 📝 Buenas Prácticas

* Commits pequeños y descriptivos
* Rebase solo en ramas locales
* Merge para integración final
* Resolver conflictos con cuidado

---

## 🎯 Nota para Full Stack

Git es esencial para:

* Trabajo colaborativo
* CI/CD
* Code reviews
* Entornos profesionales

