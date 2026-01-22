## TARJETA DE ESTUDIO – Performance vs Seguridad en Concurrencia

---

## 📌 Trade-off Central

Más seguridad suele implicar:
- Más sincronización
- Menor rendimiento

Menos sincronización implica:
- Mayor riesgo
- Bugs sutiles

---

## 🧱 Decisiones Comunes

- `ConcurrentHashMap` vs `HashMap + lock`
- Inmutabilidad vs mutabilidad protegida
- Throughput vs latencia

---

## ⚠️ Error Clásico

Optimizar antes de:
- Medir
- Entender el cuello de botella

---

## 🎯 Buenas Prácticas Senior

- Medir con métricas reales
- Optimizar el 20% crítico
- Preferir claridad sobre micro-optimización

---

## 🧠 Regla Mental

**La concurrencia correcta es más valiosa que la rápida**
