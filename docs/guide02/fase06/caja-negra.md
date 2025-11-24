# 🧪 Pruebas de Caja Negra - FisiConnect

Testing funcional de requisitos mandatorios validando entradas válidas e inválidas.

---

## 📊 Matriz de Trazabilidad de Pruebas

| RF | ID | Descripción | Entrada | Esperado | Resultado |
|----|-----|---|---|---|---|
| **RFM-001** | CT01 | Registro exitoso | Email: user@unmsm.edu.pe, Pass: Pass123! | Registro creado | ✅ OK |
| **RFM-001** | CT02 | Rechazo email @gmail | Email: user@gmail.com | Error permitido | ✅ OK |
| **RFM-001** | CT03 | Rechazo contraseña corta | Pass: 123 | Error mín 8 caracteres | ✅ OK |
| **RFM-002** | CT04 | Subida PDF exitosa | material.pdf (10MB) | Archivo subido, +50 pts | ✅ OK |
| **RFM-002** | CT05 | Rechazo archivo .exe | virus.exe | Error tipo no permitido | ✅ OK |
| **RFM-002** | CT06 | Rechazo archivo > 50MB | video.mp4 (100MB) | Error tamaño máximo | ✅ OK |
| **RFM-003** | CT07 | Búsqueda con filtro | Carrera: Software, Sem: 5 | 15 materiales mostrados | ✅ OK |
| **RFM-003** | CT08 | Búsqueda por texto | "Bases de datos" | 8 resultados | ✅ OK |
| **RFM-004** | CT09 | Descarga exitosa | Clic descargar | Archivo descargado, +1 | ✅ OK |
| **RFM-004** | CT10 | Vistas incrementan | Abrir página | Contador +1 | ✅ OK |
| **RFM-005** | CT11 | Calificación 5 estrellas | Select 5 stars | +10 puntos | ✅ OK |
| **RFM-005** | CT12 | Rechazo 2da calificación | Calificar nuevamente | Error ya calificado | ✅ OK |
| **RFM-006** | CT13 | Comentario exitoso | "Material útil" | Comentario visible | ✅ OK |
| **RFM-006** | CT14 | Rechazo comentario vacío | Texto vacío | Error vacío | ✅ OK |

---

## ✅ Resumen

| Categoría | Total | Pasados | Cobertura |
|-----------|-------|---------|-----------|
| **Autenticación** | 3 | 3 | 100% |
| **Materiales** | 3 | 3 | 100% |
| **Búsqueda** | 2 | 2 | 100% |
| **Descarga** | 2 | 2 | 100% |
| **Calificaciones** | 2 | 2 | 100% |
| **Comentarios** | 2 | 2 | 100% |
| **TOTAL** | **14** | **14** | **100%** |

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025

