# 🟡 Requisitos Funcionales de Mejora - FisiConnect

Requisitos que incrementan la experiencia del usuario y el valor de la plataforma, pero el sistema funciona sin ellos.

---

## RFM-007: Perfil de Usuario

**Descripción:** Estadísticas personales y vista de "Mis materiales" para mayor motivación.

### Especificación Técnica
- **Información personal:**
  - Nombre, email, carrera, semestre
  - Avatar personalizable
- **Estadísticas en tiempo real:**
  - Total de materiales subidos
  - Total de descargas recibidas
  - Total de vistas acumuladas
  - Calificación promedio de materiales
  - Puntos totales y posición en ranking
- **Sección "Mis materiales":**
  - Lista de materiales subidos por el usuario
  - Estadísticas individuales por material
  - Filtrado y ordenamiento

### Criterios de Aceptación
- ✅ Usuario puede ver su perfil completo
- ✅ Estadísticas se calculan automáticamente
- ✅ "Mis materiales" muestra solo contenido propio
- ✅ Información se actualiza en tiempo real

**Beneficio:** Mayor motivación para compartir contenido de calidad

**Estado:** ✅ Implementado

---

## RFM-008: Sistema de Gamificación

**Descripción:** Puntos, ranking y leaderboard para incentivar participación activa.

### Especificación Técnica
- **Sistema de puntos:**
  - Subir material: +50 puntos
  - Recibir descarga: +5 puntos
  - Calificación 4-5 estrellas: +10 puntos
- **Ranking dinámico:**
  - Cálculo automático de posición (rank)
  - Actualización en tiempo real
- **Leaderboard público:**
  - Top 50 usuarios
  - Datos: nombre, carrera, puntos, rank
  - Ordenamiento descendente por puntos

### Criterios de Aceptación
- ✅ Puntos se asignan automáticamente
- ✅ Ranking se actualiza al cambiar puntos
- ✅ Leaderboard muestra top 50 correctamente
- ✅ Usuario puede ver su posición en ranking

**Beneficio:** Incentivo de participación y competencia amistosa

**Estado:** ✅ Implementado

---

## RFM-009: Dashboard Principal

**Descripción:** Interfaz con materiales recientes y populares para mejor experiencia.

### Especificación Técnica
- **Componentes principales:**
  - Barra de búsqueda prominente
  - Filtros rápidos visibles
  - Grid de materiales con tarjetas
- **Información en tarjetas:**
  - Título del material
  - Autor
  - Carrera y semestre
  - Calificación promedio (estrellas)
  - Total de descargas
  - Tipo de archivo (ícono)
- **Ordenamiento por defecto:**
  - Materiales más recientes primero
- **Paginación:**
  - 20 materiales por página

### Criterios de Aceptación
- ✅ Dashboard carga materiales automáticamente
- ✅ Tarjetas muestran información relevante
- ✅ Búsqueda y filtros son accesibles
- ✅ Paginación funciona correctamente

**Beneficio:** Mejor experiencia de usuario y navegación intuitiva

**Estado:** ✅ Implementado

---

## RFM-010: Página de Detalles

**Descripción:** Vista completa del material con información contextualizada.

### Especificación Técnica
- **Metadata completa:**
  - Título, descripción
  - Autor, carrera, asignatura, semestre
  - Fecha de subida
  - Tipo y tamaño de archivo
- **Estadísticas:**
  - Total de descargas
  - Total de visualizaciones
  - Calificación promedio
  - Número de reseñas
- **Componentes adicionales:**
  - Botón de descarga destacado
  - Vista previa de PDF (si aplica)
  - Lista completa de reseñas con paginación
  - Formulario para agregar reseña

### Criterios de Aceptación
- ✅ Página muestra toda la información del material
- ✅ Estadísticas son precisas y actualizadas
- ✅ Botón de descarga es funcional
- ✅ Reseñas se muestran correctamente

**Beneficio:** Información contextualizada para tomar decisiones

**Estado:** ✅ Implementado

---

## RFM-011: Contador de Visualizaciones

**Descripción:** Métrica de popularidad que indica cuántas veces se ha visto un material.

### Especificación Técnica
- **Incremento automático:**
  - Cada vez que se abre la página de detalles
  - Incremento en base de datos
- **Visualización:**
  - En tarjeta de material (dashboard)
  - En página de detalles
  - En perfil de usuario (vistas totales)
- **Sin duplicación:**
  - Cuenta cada visita, independiente del usuario

### Criterios de Aceptación
- ✅ Contador incrementa al abrir página de detalles
- ✅ Contador se muestra en tarjeta y detalles
- ✅ Total de vistas visible en perfil del autor

**Beneficio:** Feedback sobre impacto y popularidad

**Estado:** ✅ Implementado

---

## RFM-012: Contador de Descargas

**Descripción:** Métrica de utilidad que valida el contenido compartido.

### Especificación Técnica
- **Incremento automático:**
  - Cada vez que se hace clic en descargar
  - Incremento en base de datos
  - +5 puntos al autor del material
- **Visualización:**
  - En tarjeta de material (dashboard)
  - En página de detalles
  - En perfil de usuario (descargas totales)
- **Validación:**
  - Solo usuarios autenticados pueden descargar

### Criterios de Aceptación
- ✅ Contador incrementa al descargar
- ✅ Autor recibe +5 puntos automáticamente
- ✅ Total de descargas visible en perfil del autor
- ✅ Métrica ayuda a identificar contenido valioso

**Beneficio:** Validación de contenido y recompensa al autor

**Estado:** ✅ Implementado

---

## 📊 Resumen de Requisitos de Mejora

| ID | Requisito | Descripción | Beneficio | Estado |
|----|-----------|-------------|-----------|--------|
| **RFM-007** | Perfil de Usuario | Estadísticas personales y "Mis materiales" | Mayor motivación para compartir | ✅ |
| **RFM-008** | Sistema de Gamificación | Puntos, ranking y leaderboard | Incentivo de participación | ✅ |
| **RFM-009** | Dashboard Principal | Interfaz con materiales recientes y populares | Mejor experiencia de usuario | ✅ |
| **RFM-010** | Página de Detalles | Vista completa del material | Información contextualizada | ✅ |
| **RFM-011** | Contador de Visualizaciones | Métrica de popularidad | Feedback sobre impacto | ✅ |
| **RFM-012** | Contador de Descargas | Métrica de utilidad | Validación de contenido | ✅ |

**Total: 6 requisitos funcionales de mejora - 100% implementados**

---

## 💡 Nota

Estas funcionalidades **optimizan la experiencia** y aumentan el valor de la plataforma, pero **no son críticas** para el funcionamiento básico del sistema. Sin embargo, en FisiConnect todas fueron implementadas para ofrecer una experiencia completa y motivadora para la comunidad estudiantil.

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025

