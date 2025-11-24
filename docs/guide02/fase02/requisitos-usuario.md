# 👥 Requisitos de Usuario - FisiConnect

## 📊 Obtención de Requisitos

Los requisitos funcionales fueron identificados mediante **encuestas digitales** aplicadas a estudiantes de la Facultad de Ingeniería de Sistemas e Informática de la UNMSM, utilizando técnicas de recopilación de requisitos documentadas en el **Anexo A**.

---

## 🎯 Ámbito Funcional del Sistema

### Para Estudiantes (Usuarios Principales)

- **Registro y autenticación** en la plataforma
- **Subida de materiales** académicos (PDF, PPTX, videos, documentos)
- **Búsqueda y descarga** de contenidos con filtros avanzados
- **Calificación y comentarios** para validar calidad
- **Sistema de gamificación** con puntos y ranking
- **Perfil personalizado** con estadísticas

---

## ✨ Funcionalidades Principales Implementadas

### Sistema de Autenticación
- Registro con email + contraseña
- Autenticación segura con **JWT tokens**
- Validación de identidad mediante correo
- Sesiones persistentes

### Gestión de Materiales
- Subida de archivos con metadatos:
  - Título, descripción
  - Carrera, asignatura, semestre
  - Tipo de archivo (PDF, PPTX, video, documento)
- Validación de tipo y tamaño (máx. 50MB)
- Almacenamiento con nombres únicos (UUID)

### Búsqueda y Descubrimiento
- Motor de búsqueda con **filtros múltiples:**
  - Carrera (Ingeniería de Software, Sistemas, Ciencia de la Computación)
  - Semestre (1-10)
  - Asignatura
  - Tipo de archivo
- Ordenamiento por: fecha, popularidad, calificación
- **Paginación** de resultados (20 por página)

### Interacción y Colaboración
- **Calificación con estrellas** (1-5)
- **Comentarios** con validación de contenido
- **Promedio ponderado** de calificaciones
- **Historial** de reseñas por material

### Gamificación
- **Puntos por contribución:**
  - Subir material: +50 puntos
  - Recibir descarga: +5 puntos
  - Calificación alta (4-5 estrellas): +10 puntos
- **Ranking dinámico** actualizado en tiempo real
- **Leaderboard** con top 50 usuarios

### Gestión Personal
- **Perfil de usuario** con:
  - Información personal (nombre, carrera, semestre)
  - Avatar personalizable
  - Estadísticas (materiales, descargas, vistas, rating)
- **Mis materiales:** Lista de contenido propio subido
- **Panel de estadísticas:** Visualización de impacto

---

## 📋 Anexo A: Técnicas de Obtención de Requisitos

### Metodología Aplicada

**Encuestas digitales** mediante Google Forms dirigida a la comunidad estudiantil de FISI-UNMSM.

### Objetivo de la Recopilación

Identificar:
- Patrones de búsqueda y organización de materiales
- Dificultades actuales en acceso a recursos
- Necesidades específicas de filtrado
- Factores de motivación para compartir contenido

### Población Muestral

**46+ estudiantes** de pregrado de la Facultad de Ingeniería de Sistemas e Informática - UNMSM, de diferentes ciclos académicos.

### Instrumento de Recolección

Formulario digital disponible en: [https://forms.gle/vJYoqqZHxQbrZ2SXA](https://forms.gle/vJYoqqZHxQbrZ2SXA)

### Técnicas Complementarias

- **Análisis de plataformas existentes:** Google Drive, Telegram, WhatsApp groups
- **Entrevistas informales:** Conversaciones con estudiantes de diferentes ciclos
- **Prototipado iterativo:** Validación temprana con usuarios beta
- **Observación participativa:** Cómo comparten materiales actualmente

### Hallazgos Principales

**Problemas Identificados:**
- Desorganización de materiales en múltiples plataformas
- Dificultad para evaluar calidad del contenido
- Falta de motivación para compartir apuntes
- Pérdida de tiempo buscando recursos

**Soluciones Propuestas:**
- Plataforma centralizada con organización automática
- Sistema comunitario de calificaciones
- Gamificación para incentivar contribuciones
- Buscador avanzado con múltiples filtros

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025  
