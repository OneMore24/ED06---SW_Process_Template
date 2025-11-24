# 🧮 Pseudocódigo - Requisitos Funcionales Críticos

Algoritmos clave representados en **PSeInt** para los requisitos funcionales mandatorios más importantes de FisiConnect.

---

## 🔐 Pseudocódigo 01: Autenticación de Usuario

**Descripción:** Algoritmo de registro y login con validación de credenciales y generación de token JWT.

![Autenticación de Usuario en PSeInt](pseudocodigo/AutenticacionUsuario.png)

**Lógica implementada:**
- Validación de formato de email
- Verificación de contraseña (mínimo 8 caracteres)
- Hashing de contraseña con bcrypt
- Generación de token JWT para sesiones
- Manejo de errores (credenciales incorrectas, usuario no existe)

**Requisito asociado:** RFM-001 - Autenticación de Usuarios

---

## 🔍 Pseudocódigo 02: Búsqueda Avanzada de Materiales

**Descripción:** Sistema de búsqueda con filtros múltiples y procesamiento optimizado de resultados.

![Búsqueda Avanzada en PSeInt](pseudocodigo/BusquedaMateriales.png)

**Lógica implementada:**
- Búsqueda por texto en título y descripción
- Aplicación de filtros simultáneos:
  - Carrera
  - Semestre
  - Asignatura
  - Tipo de archivo
- Ordenamiento de resultados (fecha, popularidad, calificación)
- Paginación de 20 resultados por página

**Requisito asociado:** RFM-003 - Búsqueda y Filtrado

---

## ⭐ Pseudocódigo 03: Sistema de Calificaciones

**Descripción:** Algoritmo de calificación de materiales y cálculo automático de promedio ponderado.

![Sistema de Calificaciones - Parte 1](pseudocodigo/CalificarMaterial_1.png)
![Sistema de Calificaciones - Parte 2](pseudocodigo/CalificarMaterial_2.png)

**Lógica implementada:**
- Validación de calificación (1-5 estrellas)
- Verificación de usuario autenticado
- Restricción: una calificación por usuario por material
- Cálculo de promedio ponderado de todas las calificaciones
- Actualización de contador de reseñas
- Asignación de puntos al autor (+10 si calificación ≥ 4)

**Requisito asociado:** RFM-005 - Sistema de Calificaciones

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025 
