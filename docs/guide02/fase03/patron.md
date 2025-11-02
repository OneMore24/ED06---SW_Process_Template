# Patrón de Arquitectura de Software - FisiConnect

## Patrón seleccionado: 2-Capas

## 📝 Descripción del Patrón

El patrón de 2 capas seleccionado para FisiConnect separa claramente la **capa de presentación** (frontend) de la **capa de datos** (backend + base de datos), proporcionando una arquitectura simple pero efectiva para nuestro prototipo académico. En la capa superior, React se encarga de toda la interfaz de usuario, gestionando el estado de la aplicación y la interacción con el usuario mediante componentes reutilizables. La capa inferior, implementada con FastAPI y PostgreSQL, maneja toda la lógica de negocio, validaciones, autenticación y persistencia de datos. Esta separación permite un desarrollo paralelo donde el equipo frontend puede trabajar independientemente del backend, utilizando contratos de API bien definidos. La comunicación entre capas se realiza mediante APIs RESTful, asegurando desacoplamiento y facilitando futuras evoluciones del sistema. Este patrón es ideal para proyectos académicos como FisiConnect porque reduce complejidad, acelera el desarrollo y mantiene una estructura organizada que facilita el mantenimiento y la comprensión del código por parte de todos los miembros del equipo.

---

## 🎯 Justificación Técnica

### **Ventajas para FisiConnect:**
- **Simplicidad**: Fácil de entender e implementar por el equipo estudiantil
- **Desarrollo paralelo**: Frontend y backend pueden avanzar simultáneamente
- **Mantenibilidad**: Separación clara de responsabilidades
- **Escalabilidad**: Permite evolucionar a 3 capas si el proyecto crece
- **Testing**: Facilita pruebas unitarias e integrales por separado

### **Responsabilidad por Capa:**

| Capa | Responsabilidad |
|------|-----------------|
| **Presentación** | Interfaz de usuario y experiencia |
| **Datos** | Lógica de negocio y persistencia |

---

> **Nota del Equipo ED06**: El patrón de 2 capas se alinea perfectamente con nuestros objetivos académicos y nivel de experiencia, permitiendo un desarrollo eficiente sin sacrificar la calidad arquitectónica.

*Equipo ED06 - FisiConnect*
