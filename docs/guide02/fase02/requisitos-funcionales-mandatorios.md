# 🔴 Requisitos Funcionales Mandatorios - FisiConnect

Requisitos esenciales que aseguran el funcionamiento básico del sistema. Sin estos, la plataforma no cumple su propósito.

---

## RFM-001: Autenticación de Usuarios

**Descripción:** El sistema debe permitir el registro e inicio de sesión seguro de usuarios.

### Especificación Técnica
- **Registro:**
  - Campos: email, nombre, contraseña, carrera, semestre
  - Validación de formato de email
  - Contraseña mínima de 8 caracteres
  - Hashing con bcrypt (12 rounds)
- **Login:**
  - Validación de credenciales
  - Generación de JWT con expiración de 30 minutos
  - Persistencia de sesión en navegador

### Criterios de Aceptación
- ✅ Usuario puede registrarse con datos válidos
- ✅ Contraseñas se almacenan hasheadas
- ✅ Usuario puede iniciar sesión y recibir token JWT
- ✅ Token es requerido para operaciones protegidas

**Estado:** ✅ Implementado

---

## RFM-002: Gestión de Materiales

**Descripción:** Los usuarios deben poder subir y almacenar archivos académicos con metadata.

### Especificación Técnica
- **Tipos de archivo permitidos:** `.pdf`, `.pptx`, `.ppt`, `.doc`, `.docx`, `.mp4`, `.xls`, `.xls`.
- **Tamaño máximo:** 50 MB
- **Metadata obligatoria:**
  - Título
  - Descripción
  - Carrera
  - Asignatura
  - Semestre
- **Almacenamiento:** UUID único por archivo
- **Base de datos:** Relación con usuario autor

### Criterios de Aceptación
- ✅ Usuario autenticado puede subir archivos válidos
- ✅ Archivos inválidos son rechazados con mensaje de error
- ✅ Material queda asociado al usuario que lo subió
- ✅ Sistema otorga +50 puntos al subir

**Estado:** ✅ Implementado

---

## RFM-003: Búsqueda y Filtrado

**Descripción:** Motor de búsqueda con filtros avanzados para localizar materiales.

### Especificación Técnica
- **Búsqueda por texto:** En título y descripción
- **Filtros disponibles:**
  - Carrera (Ingeniería de Software, Sistemas, Ciencia de la Computación)
  - Semestre (1-10)
  - Asignatura
  - Tipo de archivo (PDF, PPTX, Video, Documento)
- **Ordenamiento:**
  - Más reciente (fecha descendente)
  - Más populares (descargas descendente)
  - Mejor calificados (rating descendente)
- **Paginación:** 20 resultados por página

### Criterios de Aceptación
- ✅ Filtros se pueden combinar simultáneamente
- ✅ Búsqueda retorna resultados en < 1 segundo
- ✅ Ordenamiento funciona correctamente
- ✅ Paginación es fluida

**Estado:** ✅ Implementado

---

## RFM-004: Visualización y Descarga

**Descripción:** Acceso a contenidos descargables con contador de estadísticas.

### Especificación Técnica
- **Página de detalles:**
  - Metadata completa del material
  - Botón de descarga visible
  - Vista previa de PDF (si aplica)
  - Lista de reseñas
- **Contadores automáticos:**
  - Incremento de visualizaciones al abrir página
  - Incremento de descargas al hacer clic en descargar
- **Gamificación:**
  - +5 puntos al autor por cada descarga

### Criterios de Aceptación
- ✅ Cualquier usuario puede ver detalles
- ✅ Solo usuarios autenticados pueden descargar
- ✅ Contadores se actualizan automáticamente
- ✅ Puntos se otorgan al autor correctamente

**Estado:** ✅ Implementado

---

## RFM-005: Sistema de Calificaciones

**Descripción:** Valoración de materiales mediante estrellas (1-5).

### Especificación Técnica
- **Calificación:** 1 a 5 estrellas
- **Restricción:** Un usuario puede calificar un material solo una vez
- **Cálculo automático:**
  - Promedio ponderado de todas las calificaciones
  - Contador total de reseñas
- **Gamificación:**
  - +10 puntos al autor si calificación es 4-5 estrellas

### Criterios de Aceptación
- ✅ Usuario autenticado puede calificar materiales
- ✅ Promedio se calcula correctamente
- ✅ Calificación se refleja en tarjeta del material
- ✅ Puntos se otorgan según calificación

**Estado:** ✅ Implementado

---

## RFM-006: Comentarios y Reseñas

**Descripción:** Feedback comunitario sobre materiales mediante comentarios textuales.

### Especificación Técnica
- **Componentes:**
  - Campo de texto para comentario
  - Comentario asociado a calificación por estrellas
  - Registro de usuario y fecha
- **Visualización:**
  - Lista de comentarios ordenados por fecha (más recientes primero)
  - Nombre del usuario visible en cada comentario
  - Fecha de publicación
- **Validación:**
  - Comentario no puede estar vacío
  - Usuario debe estar autenticado

### Criterios de Aceptación
- ✅ Usuario autenticado puede dejar comentarios
- ✅ Comentario se guarda con calificación y usuario
- ✅ Lista de comentarios se actualiza automáticamente
- ✅ Comentarios se muestran con nombre y fecha

**Estado:** ✅ Implementado

---

## 📊 Resumen de Requisitos Mandatorios

| ID | Requisito | Descripción | Estado |
|----|-----------|-------------|--------|
| **RFM-001** | Autenticación de Usuarios | Registro e inicio de sesión seguro | ✅ |
| **RFM-002** | Gestión de Materiales | Subida y almacenamiento de archivos académicos | ✅ |
| **RFM-003** | Búsqueda y Filtrado | Motor de búsqueda con filtros avanzados | ✅ |
| **RFM-004** | Visualización y Descarga | Acceso a contenidos descargables | ✅ |
| **RFM-005** | Sistema de Calificaciones | Valoración de materiales mediante estrellas | ✅ |
| **RFM-006** | Comentarios y Reseñas | Feedback comunitario sobre materiales | ✅ |

**Total: 6 requisitos funcionales mandatorios - 100% implementados**

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025

