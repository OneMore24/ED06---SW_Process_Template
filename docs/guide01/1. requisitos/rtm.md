# 📋 RTM - Especificación de Requisitos de Software

## 🔧 Requisitos Funcionales

Los requisitos funcionales se expresan en lenguaje técnico a partir de los requisitos mandatorios identificados para FisiConnect:

### Autenticación y Acceso
- El sistema debe autenticar usuarios mediante correo y contraseña con JWT
- El token de sesión debe expirar después de 30 minutos de inactividad
- Las contraseñas deben ser hasheadas con bcrypt (12 rounds) antes de almacenarse
- Los usuarios no autenticados no podrán subir materiales ni crear reseñas

### Gestión de Materiales
- El sistema debe permitir subida de archivos académicos (.pdf, .pptx, .mp4, .docx, .xlsx, .xls)
- El tamaño máximo de archivo permitido es de 50 MB
- Cada material debe incluir: título, descripción, carrera, asignatura, semestre
- El sistema debe validar y rechazar archivos con extensiones no permitidas
- Se debe almacenar la fecha de carga y el autor del material

### Búsqueda y Filtrado
- La búsqueda debe implementar filtros por: carrera, semestre, asignatura, tipo de archivo
- Debe permitirse búsqueda por texto en título y descripción
- Los resultados se ordenarán por: fecha (reciente), popularidad (descargas), calificación promedio
- La paginación debe mostrar 20 resultados por página

### Sistema de Calificaciones
- Los usuarios autenticados podrán calificar materiales con 1-5 estrellas
- Cada calificación puede incluir un comentario de texto opcional
- El sistema debe calcular automáticamente el promedio ponderado de calificaciones
- Se debe mostrar el nombre del usuario y fecha de cada reseña

### Estadísticas y Contadores
- El sistema debe incrementar el contador de descargas cuando un usuario descarga un material
- El sistema debe incrementar el contador de visualizaciones al abrir la página de detalles
- Se debe registrar automáticamente el número total de reseñas por material
- El perfil del usuario debe mostrar: materiales subidos, descargas recibidas, vistas totales, calificación promedio

### Sistema de Gamificación
- El sistema debe asignar puntos automáticamente:
  - 50 puntos por subir un material
  - 5 puntos al autor cada vez que su material es descargado
  - 10 puntos por recibir calificación de 4-5 estrellas
- El ranking debe actualizarse en tiempo real según puntos acumulados
- El leaderboard debe mostrar top 50 usuarios ordenados por puntos
- El perfil del usuario debe mostrar su posición en el ranking

### Interfaz de Usuario
- El dashboard principal debe mostrar materiales recientes y populares
- Cada material debe mostrarse en tarjeta con: título, autor, carrera, calificación, descargas
- La página de detalles debe incluir: metadata completa, vista previa (si aplica), botón de descarga, lista de reseñas, formulario para agregar reseña
- El perfil de usuario debe mostrar mis materiales, estadísticas y ranking

---

## 🔒 Requisitos No Funcionales

### Portabilidad
- La plataforma debe funcionar en navegadores modernos: Chrome, Firefox, Safari, Edge (últimas 2 versiones)
- El diseño debe ser **responsive** para: móviles (320px+), tablets (768px+), desktop (1024px+)
- El frontend debe estar deployable en Vercel, Netlify o similar
- El backend debe ser deployable en Railway, Heroku o AWS

### Usabilidad
- La interfaz debe ser intuitiva con navegación clara mediante barra superior
- Todos los formularios deben incluir validación en tiempo real
- Los mensajes de error deben ser descriptivos y actionables
- El contraste de colores debe cumplir con estándares WCAG AA

### Rendimiento
- El tiempo de carga de la página principal debe ser < 2 segundos
- Las búsquedas deben retornar resultados en < 1 segundo
- Las descargas deben iniciarse inmediatamente sin procesamiento previo

### Mantenibilidad
- El código debe estar documentado con comentarios explicativos
- La estructura debe seguir patrón de separación: frontend/backend/base de datos
- Las dependencias deben estar listadas en requirements.txt (Python) y package.json (Node.js)
- El versionado debe realizarse mediante Git con commits descriptivos

### Disponibilidad
- El sistema debe estar disponible mínimo el **99%** del tiempo
- Se deben implementar manejo de errores con mensajes claros al usuario
- Los errores del servidor deben registrarse en logs para debugging

### Almacenamiento
- El sistema debe soportar al menos **50 GB** de materiales en la primera fase
- Los archivos se almacenarán en el servidor con nombres únicos (UUID)
- Se debe validar el espacio en disco disponible antes de aceptar nuevas subidas

### Seguridad
- Las contraseñas deben ser hasheadas antes de almacenarse
- La autenticación debe usar JWT con expiración
- Se debe validar la entrada en todos los endpoints (Pydantic)
- Se debe prevenir inyección SQL mediante ORM (SQLAlchemy)
- Los archivos descargados deben servirse con headers seguros

### Escalabilidad
- La arquitectura debe permitir crecimiento de usuarios sin rediseño mayor
- La base de datos debe usar índices en campos de búsqueda frecuente
- La paginación debe implementarse en todas las listas de datos
- El sistema debe prepararse para cache (Redis) en futuras versiones

---

## 📊 Matriz de Trazabilidad (RTM)

| Requisito | Componente | Implementación | Estado |
|-----------|-----------|-----------------|--------|
| RF01 - Autenticación | Backend API | Endpoints /auth/register, /auth/login | ✅ |
| RF02 - Subida de materiales | Backend + Storage | POST /api/materials | ✅ |
| RF03 - Búsqueda y filtrado | Backend | GET /api/materials?filters | ✅ |
| RF04 - Calificaciones | Backend | POST /api/reviews | ✅ |
| RF05 - Reseñas | Frontend | ReviewForm component | ✅ |
| RF06 - Visualización | Frontend | Material detail page | ✅ |
| RF07 - Descarga | Backend | Download endpoint + counter | ✅ |
| RF08 - Perfil de usuario | Frontend | Profile page + API | ✅ |
| RF09 - Gamificación | Backend | Points calculation logic | ✅ |
| RF10 - Ranking | Frontend | Leaderboard page | ✅ |
| RF11 - Contadores | Backend | View/Download counters | ✅ |
| RF12 - Dashboard | Frontend | Home page | ✅ |

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025  

