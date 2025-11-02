# Patrón de Arquitectura de Software - FisiConnect

### **Esquema Gráfico de la Arquitectura**

![Arquitectura de 3 Capas - FisiConnect](../../assets/recursos/3-capas.png)
*Diagrama detallado de la arquitectura en 3 capas implementada en FisiConnect*

## 📝 Descripción del Patrón

La arquitectura seleccionada para el proyecto es una **Arquitectura en 3 Capas**. Este enfoque reduce la complejidad operativa, lo cual es esencial considerando que el proyecto tiene un carácter educativo, con recursos y equipo limitado; además, facilita el aprendizaje y la comprensión del diseño sin exponer al equipo a infraestructuras avanzadas o costosas.

Se descartaron otros patrones como Cliente-Servidor y Microservicios como enfoque principal inicial. El modelo Cliente-Servidor aunque es útil, tiene limitaciones en escalabilidad, modularidad y mantenibilidad, dificultando la evolución del proyecto; y Microservicios, aunque escalables, implican una complejidad innecesaria para una solución que será utilizada con fines académicos y con bajo volumen inicial de usuarios. Por ello, la arquitectura por capas ofrece el equilibrio ideal entre claridad, simplicidad, mantenibilidad y posibilidad de evolución futura si el proyecto creciera más allá del entorno educativo.

---

### **Responsabilidades por Capa:**

| Capa | Responsabilidad |
|------|-----------------|
| **Presentación** | Interfaz de usuario y experiencia |
| **Lógica de Negocio** | Reglas de negocio y procesamiento |
| **Datos** | Almacenamiento y gestión de datos |

### **Flujo de Datos:**
1. **Capa de Presentación**: Recibe interacción del usuario y muestra datos
2. **Capa de Lógica de Negocio**: Procesa solicitudes, aplica reglas y valida
3. **Capa de Datos**: Almacena y recupera información persistentemente

---

> **Nota del Equipo ED06**: La arquitectura de 3 capas proporciona el balance perfecto entre simplicidad y robustez para FisiConnect, permitiendo un desarrollo educativo eficiente mientras se mantiene la capacidad de evolucionar en el futuro.

*Equipo ED06 - FisiConnect*

