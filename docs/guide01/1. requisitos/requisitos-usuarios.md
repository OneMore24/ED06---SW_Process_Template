# 👥 Requisitos de Usuario

## 📊 Obtención de Requisitos

Los requisitos funcionales fueron identificados mediante **encuestas digitales** aplicadas a estudiantes de la Facultad de Ingeniería de Sistemas e Informática de la UNMSM, utilizando técnicas de recopilación de requisitos documentadas en el **Anexo A**.

---

## 🎯 Ámbito Funcional del Sistema

### Funcionalidades para Estudiantes

El sistema FisiConnect está diseñado exclusivamente para estudiantes, quienes pueden:

- **Registro y autenticación** en la plataforma
- **Subida de materiales** académicos (PDF, PPTX, videos, documentos)
- **Búsqueda avanzada** con filtros múltiples
- **Visualización y descarga** de contenidos
- **Sistema de calificaciones** con estrellas y comentarios
- **Perfil personalizado** con estadísticas de contribución
- **Competencia amistosa** mediante sistema de puntos y ranking

---

## ✨ Funcionalidades Principales Implementadas

### Sistema de Autenticación
- **Registro con email** y contraseña
- **Validación segura** mediante JWT tokens
- **Persistencia de sesión** en navegador

### Gestión de Materiales
- **Subida de archivos** con validación de tipo y tamaño (máx. 50MB)
- **Metadatos completos**: título, descripción, carrera, asignatura, semestre
- **Organización automática** por categorías
- **Contador de descargas y visualizaciones**

### Búsqueda Avanzada
- **Filtros múltiples**: carrera, semestre, asignatura, tipo de archivo
- **Búsqueda por texto** en título y descripción
- **Ordenamiento** por fecha, popularidad y calificación
- **Paginación eficiente** (20 resultados por página)

### Sistema de Evaluación
- **Calificación con estrellas** (1-5)
- **Comentarios detallados** de usuarios
- **Promedio ponderado** de calificaciones
- **Historial completo** de reseñas

### Gamificación
- **Sistema de puntos** por contribuciones:
  - Subir material: +50 puntos
  - Recibir descarga: +5 puntos
  - Calificación alta: +10 puntos
- **Ranking dinámico** actualizado en tiempo real
- **Leaderboard público** con top 50 usuarios

### Perfil de Usuario
- **Estadísticas personales**:
  - Materiales subidos
  - Descargas recibidas
  - Vistas acumuladas
  - Calificación promedio
- **Mis materiales**: Lista de contenido propio
- **Avatar personalizable**

---

## 📋 Anexo A: Técnicas de Obtención de Requisitos

### Metodología Aplicada
**Encuestas digitales** mediante Google Forms dirigidas a la comunidad estudiantil de FISI-UNMSM

### Objetivo de la Recopilación
Identificar:
- Patrones de estudio y organización de materiales
- Dificultades para encontrar recursos académicos de calidad
- Necesidades específicas de filtrado y búsqueda
- Factores de motivación para compartir contenido

### Población Muestral
**46+ estudiantes** de pregrado de la Facultad de Ingeniería de Sistemas e Informática - UNMSM

### Instrumento de Recolección
Formulario digital disponible en: [https://forms.gle/vJYoqqZHxQbrZ2SXA](https://forms.gle/vJYoqqZHxQbrZ2SXA)

### Técnicas Complementarias
- **Análisis de plataformas existentes**: Google Drive compartido, grupos de WhatsApp, Telegram
- **Entrevistas informales**: Conversaciones con estudiantes de diferentes ciclos
- **Prototipado iterativo**: Validación temprana con usuarios beta
- **Observación de flujos actuales**: Cómo comparten materiales actualmente

### Hallazgos Principales

**Problemas Identificados:**
- Desorganización de materiales compartidos en grupos
- Dificultad para evaluar calidad de contenido
- Falta de motivación para compartir apuntes
- Búsqueda ineficiente (archivos perdidos en chats)

**Soluciones Propuestas:**
- Plataforma centralizada con organización automática
- Sistema de calificaciones comunitario
- Gamificación con puntos y rankings
- Buscador avanzado con múltiples filtros

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025  
