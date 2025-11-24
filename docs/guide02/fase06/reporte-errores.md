# 🐛 Reporte de Errores - FisiConnect

Informe de defectos encontrados durante testing, su estado y resolución.

---

## 📋 Anexo 2: Informe de Errores Encontrados

| ID | Descripción | Pasos | Fecha | Tester | Estado | Corregido por | Fecha Cierre | Prioridad |
|----|-------------|-------|-------|--------|--------|---------------|--------------|-----------|
| **ERR-001** | Login: Token JWT expira sin refrescar | 1. Login exitoso 2. Esperar 30 min 3. Intentar acción | 2025-11-15 | Alan | ✅ Cerrado | Alan | 2025-11-17 | Alta |
| **ERR-002** | Subida: No valida extensión .rar | 1. Seleccionar archivo.rar 2. Subir | 2025-11-16 | Marco | ✅ Cerrado | Alan | 2025-11-17 | Media |
| **ERR-003** | Búsqueda: Filtro semestre retorna duplicados | 1. Filtrar por semestre 5 2. Ver resultados | 2025-11-16 | Alan | ✅ Cerrado | Alan | 2025-11-18 | Media |
| **ERR-004** | Calificación: Promedio no actualiza inmediato | 1. Calificar material 2. Recargar página | 2025-11-17 | Marco | ✅ Cerrado | Alan | 2025-11-18 | Baja |
| **ERR-005** | Descarga: Contador se duplica en concurrencia | 1. 2 usuarios descargan simultáneamente | 2025-11-17 | Alan | ✅ Cerrado | Alan | 2025-11-19 | Alta |
| **ERR-006** | Ranking: Orden incorrecto con puntos iguales | 1. Usuarios con 100 pts 2. Ver ranking | 2025-11-18 | Marco | ✅ Cerrado | Alan | 2025-11-19 | Baja |
| **ERR-007** | Perfil: Avatar no carga en Safari | 1. Login en Safari 2. Ver perfil | 2025-11-18 | Milton | ✅ Cerrado | Milton | 2025-11-19 | Media |
| **ERR-008** | UI: Responsive rompe en 320px | 1. Abrir en móvil 320px | 2025-11-19 | Milton | ✅ Cerrado | Milton | 2025-11-20 | Media |
| **ERR-009** | API: Error 500 si comentario tiene emoji | 1. Comentario: "Muy bueno 🎉" 2. Guardar | 2025-11-19 | Alan | ✅ Cerrado | Alan | 2025-11-20 | Alta |
| **ERR-010** | BD: Consulta búsqueda lenta > 5 segundos | 1. Búsqueda con 4+ filtros | 2025-11-20 | Marco | ✅ Cerrado | Alan | 2025-11-21 | Crítico |

---

## 📊 Estadísticas de Errores

| Métrica | Valor |
|---------|-------|
| **Total Defectos** | 10 |
| **Cerrados** | 10 (100%) |
| **Pendientes** | 0 |
| **Críticos** | 1 |
| **Altos** | 3 |
| **Medios** | 4 |
| **Bajos** | 2 |

---

## 🔧 Errores por Categoría

### **Autenticación (1)**
- ERR-001: Token JWT sin refresh

### **Materiales (2)**
- ERR-002: Validación extensión .rar
- ERR-005: Contador descarga duplicado

### **Búsqueda (1)**
- ERR-003: Resultados duplicados en filtro

### **Calificaciones (1)**
- ERR-004: Promedio no actualiza

### **Ranking (1)**
- ERR-006: Orden incorrecto

### **UI/UX (2)**
- ERR-007: Avatar no carga Safari
- ERR-008: Responsive 320px

### **API/BD (2)**
- ERR-009: Error emoji en comentarios
- ERR-010: Query búsqueda lento

---

## ✅ Estado Final

**Todos los errores han sido identificados, documentados y corregidos.**

El sistema FisiConnect pasó exitosamente testing de caja negra con 100% de defectos resueltos antes de entrega final.

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025
