# ☕ JAVA — Principios básicos de diseño (A5)

## Principios básicos de diseño

Los principios de diseño buscan **código mantenible, extensible y robusto**
más allá de que “funcione”.

### Principios fundamentales

### 1️⃣ Single Responsibility (SRP)
Una clase debe tener **una sola razón para cambiar**.

❌ Clases que hacen de todo  
✅ Clases pequeñas y enfocadas

### 2️⃣ Abierto/Cerrado (OCP)
El código debe estar:
- **Abierto a extensión**
- **Cerrado a modificación**

Se logra con herencia y polimorfismo.

### 3️⃣ Sustitución de Liskov (LSP)
Una subclase debe poder reemplazar a su clase base
sin romper el comportamiento esperado.

### 4️⃣ Segregación de Interfaces (ISP)
Interfaces pequeñas y específicas
❌ Interfaces “Dios”

### 5️⃣ Inversión de Dependencias (DIP)
Depender de **abstracciones**, no de implementaciones.

### Principio transversal
✅ Alta cohesión  
✅ Bajo acoplamiento

### Beneficio real
Menos bugs, menos miedo al cambio
