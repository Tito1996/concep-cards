🧠 TARJETA DE ESTUDIO – MUTABILIDAD vs INMUTABILIDAD (A6)

¿Qué es mutabilidad?

Un dato mutable puede cambiar su estado después de ser creado.

Ejemplo conceptual: 👉 crear algo y luego modificarlo.


---

¿Qué es inmutabilidad?

Un dato inmutable no puede cambiar una vez creado.
Si “cambia”, en realidad se crea uno nuevo.

Ejemplo conceptual: 👉 modificar = crear una nueva versión.


---

Diferencia clave (entrevista)

Mutable: se modifica el mismo objeto

Inmutable: se crea un objeto nuevo


Esto impacta directamente en:

Bugs

Concurrencia

Legibilidad

Seguridad del código



---

¿Por qué la inmutabilidad es importante?

Evita efectos colaterales

Reduce bugs difíciles de rastrear

Hace el código más predecible

Es más segura en entornos concurrentes


Frase clave:

> “Si no cambia, no puede romperse.”




---

Cuándo usar cada una

Usar mutabilidad cuando:

El estado realmente debe cambiar

El rendimiento es crítico

El ciclo de vida está bien controlado


Preferir inmutabilidad cuando:

Compartes datos entre capas o hilos

Quieres código más seguro y claro

El dato representa un valor, no un proceso



---

Error común de junior

Modificar objetos compartidos sin darse cuenta: 👉 un cambio afecta a otros lugares del sistema.


---

Buena práctica

Preferir inmutabilidad por defecto

Hacer mutable solo cuando sea necesario

Limitar el alcance de lo mutable



---

Frase que suma puntos

> “La inmutabilidad reduce el estado compartido y los bugs asociados.”




---