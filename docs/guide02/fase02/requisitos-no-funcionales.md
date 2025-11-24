# 🟢 Requisitos No Funcionales - FisiConnect

Atributos de calidad que guían el desarrollo, despliegue y mantenimiento del sistema.

---

## ⚡ Rendimiento

### RNF-001: Tiempo de Carga
**Descripción:** Las páginas deben cargar en tiempo óptimo para buena experiencia de usuario.

**Especificación técnica:**
- Tiempo de carga máximo de página principal: **< 2 segundos**
- Tiempo de búsqueda: **< 1 segundo**
- Descarga de archivos: A velocidad de conexión del usuario

**Métrica de verificación:**
- Lighthouse score ≥ 80
- Core Web Vitals optimizados
- Pruebas con herramientas: PageSpeed, GTmetrix

---

### RNF-002: Capacidad de Concurrencia
**Descripción:** El sistema debe soportar múltiples usuarios simultáneamente.

**Especificación técnica:**
- Soporte mínimo: **100 usuarios concurrentes**
- Arquitectura: Frontend sin estado (stateless)
- Backend escalable con FastAPI async

**Métrica de verificación:**
- Load testing con herramientas como Apache JMeter
- Monitoreo de CPU y memoria bajo carga

---

### RNF-003: Capacidad de Almacenamiento
**Descripción:** Capacidad inicial de almacenamiento de archivos.

**Especificación técnica:**
- Almacenamiento inicial: **50 GB** (archivos de usuarios)
- Escalable a futuro según demanda
- Compresión automática si es necesario

**Métrica de verificación:**
- Monitoreo mensual del espacio disponible
- Alertas cuando se alcance 80% de capacidad

---

## 🔐 Seguridad

### RNF-004: Autenticación
**Descripción:** Autenticación segura y manejo de sesiones.

**Especificación técnica:**
- **JWT (JSON Web Tokens):**
  - Expiración de 30 minutos
  - Algoritmo: HS256
  - Signature con clave privada segura
- **Hashing de contraseñas:**
  - Bcrypt con 12 rounds
  - Salt automático

**Métrica de verificación:**
- Tokens verificables y no falsificables
- Pruebas de penetración en endpoints autenticados

---

### RNF-005: Validación de Entrada
**Descripción:** Prevención de inyecciones SQL y otros ataques.

**Especificación técnica:**
- **Validación en backend:**
  - Pydantic para esquemas
  - ORM (SQLAlchemy) para prevenir SQL Injection
- **Validación en frontend:**
  - Validación de tipos en formularios
  - Mensajes de error claros

**Métrica de verificación:**
- OWASP Top 10 compliance
- Pruebas de seguridad de entrada

---

### RNF-006: Protección de Datos
**Descripción:** Protección de información sensible de usuarios.

**Especificación técnica:**
- Contraseñas hasheadas en BD
- No almacenar datos sensibles en logs
- HTTPS obligatorio en producción
- CORS configurado correctamente

**Métrica de verificación:**
- Auditoría de seguridad
- Verificación de certificados SSL/TLS

---

## 🎨 Usabilidad

### RNF-007: Diseño Responsive
**Descripción:** Interfaz adaptable a diferentes dispositivos.

**Especificación técnica:**
- **Breakpoints:**
  - Móvil: 320px - 767px
  - Tablet: 768px - 1023px
  - Desktop: 1024px+
- **Tecnologías:**
  - CSS Grid y Flexbox
  - Media queries
  - Next.js responsive

**Criterios de aceptación:**
- ✅ Interfaz legible en todos los tamaños
- ✅ Navegación funcional en móvil
- ✅ Formularios adaptados a pantalla pequeña

---

### RNF-008: Navegación Intuitiva
**Descripción:** Acciones principales accesibles con mínimos clics.

**Especificación técnica:**
- Acciones principales en ≤ 3 clics:
  - Subir material
  - Buscar material
  - Ver calificaciones
- Navegación consistente (barra superior)
- Breadcrumbs en páginas profundas

**Criterios de aceptación:**
- ✅ Usuario puede encontrar funciones rápidamente
- ✅ Menú es visible y organizado
- ✅ Links son descriptivos

---

### RNF-009: Compatibilidad de Navegadores
**Descripción:** Funciona en navegadores modernos principales.

**Especificación técnica:**
- **Navegadores soportados:**
  - Chrome 95+
  - Firefox 93+
  - Safari 15+
  - Edge 95+
- **Testing:** Cross-browser en cada versión

**Criterios de aceptación:**
- ✅ Funcionalidad completa en todos los navegadores
- ✅ Sin errores JavaScript en consola

---

## 🛠️ Mantenibilidad

### RNF-010: Código Documentado y Modular
**Descripción:** Código fácil de entender y mantener.

**Especificación técnica:**
- **Documentación:**
  - Comentarios en funciones complejas
  - Docstrings en Python
  - README con instrucciones
- **Modularidad:**
  - Separación frontend/backend
  - Componentes React reutilizables
  - Funciones pequeñas y enfocadas

**Criterios de aceptación:**
- ✅ Nuevo desarrollador entiende código
- ✅ Estructura clara de carpetas
- ✅ Nombres de variables descriptivos

---

### RNF-011: API RESTful con Documentación
**Descripción:** API bien documentada y fácil de consumir.

**Especificación técnica:**
- **Estándar REST:**
  - Endpoints semánticos
  - HTTP methods correctos (GET, POST, PUT)
  - Status codes apropiados
- **Documentación:**
  - Swagger/OpenAPI automático
  - Ejemplos de requests/responses
  - Accesible en `/docs`

**Criterios de aceptación:**
- ✅ Documentación en `/docs` accesible
- ✅ Todos los endpoints documentados
- ✅ Ejemplos de uso disponibles

---

### RNF-012: Logs y Monitoreo
**Descripción:** Registro de errores y actividad del sistema.

**Especificación técnica:**
- **Logs capturados:**
  - Errores no manejados
  - Operaciones críticas (login, subida)
  - Cambios en datos importantes
- **Niveles:** DEBUG, INFO, WARNING, ERROR
- **Almacenamiento:** Archivos locales o servicio de logs

**Criterios de aceptación:**
- ✅ Errores se registran con contexto
- ✅ Logs ayudan a debuggear problemas
- ✅ Sin información sensible en logs

---

## 🔄 Disponibilidad

### RNF-013: Uptime
**Descripción:** Sistema disponible la mayoría del tiempo.

**Especificación técnica:**
- Objetivo de disponibilidad: **99%**
- Equivalente a ~7 horas downtime/mes permitidas
- Monitoreo continuo del servicio

**Métrica de verificación:**
- Uptime tracker activo
- Alertas si sitio cae

---

### RNF-014: Respaldos de Base de Datos
**Descripción:** Protección de datos contra pérdida.

**Especificación técnica:**
- Backup automático: **Semanal**
- Almacenamiento: Ubicación separada del servidor
- Restauración verificada periódicamente

**Criterios de aceptación:**
- ✅ Backups se crean automáticamente
- ✅ Datos se pueden restaurar desde backup

---

### RNF-015: Manejo de Errores
**Descripción:** Sistema resiliente ante fallos.

**Especificación técnica:**
- Mensajes de error amigables al usuario
- Recuperación automática de fallos no críticos
- Validación de entrada exhaustiva
- Try-catch en operaciones críticas

**Criterios de aceptación:**
- ✅ Error no detiene toda la aplicación
- ✅ Usuario recibe mensaje claro
- ✅ Sistema se recupera sin intervención

---

## 📊 Resumen de Requisitos No Funcionales

| ID | Categoría | Requisito | Métrica | Estado |
|----|-----------|-----------|---------|--------|
| **RNF-001** | Rendimiento | Tiempo de carga | < 2 segundos | ✅ |
| **RNF-002** | Rendimiento | Concurrencia | 100+ usuarios | ✅ |
| **RNF-003** | Rendimiento | Almacenamiento | 50 GB | ✅ |
| **RNF-004** | Seguridad | Autenticación JWT | Tokens válidos | ✅ |
| **RNF-005** | Seguridad | Validación entrada | Sin SQL Injection | ✅ |
| **RNF-006** | Seguridad | Protección datos | HTTPS + bcrypt | ✅ |
| **RNF-007** | Usabilidad | Responsive | Móvil/Tablet/Desktop | ✅ |
| **RNF-008** | Usabilidad | Navegación | ≤ 3 clics | ✅ |
| **RNF-009** | Usabilidad | Compatibilidad | Chrome, Firefox, Safari | ✅ |
| **RNF-010** | Mantenibilidad | Código modular | Documentado | ✅ |
| **RNF-011** | Mantenibilidad | API REST | OpenAPI disponible | ✅ |
| **RNF-012** | Mantenibilidad | Logs | Sistema registrado | ✅ |
| **RNF-013** | Disponibilidad | Uptime | 99% | ✅ |
| **RNF-014** | Disponibilidad | Backups | Semanal | ✅ |
| **RNF-015** | Disponibilidad | Manejo errores | Resiliente | ✅ |

**Total: 15 requisitos no funcionales - 100% implementados**

---

## ⚠️ Funcionalidades No Implementadas en v1.0

| Funcionalidad | Razón | Versión |
|--------------|-------|---------|
| Moderación de contenido | Responsabilidad comunitaria por ahora | v1.1+ |
| Gestión de usuarios (admin) | No hay administradores en proyecto actual | v2.0+ |
| Sistema de notificaciones | Mejora futura | v1.1+ |
| Exportación de reportes | Análisis posterior no prioritario | v2.0+ |
| Integración OneDrive/Drive | MVP sin dependencias externas | v2.0+ |

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025 
