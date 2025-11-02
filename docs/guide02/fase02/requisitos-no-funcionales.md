# Requisitos No Funcionales - FisiConnect

## Rendimiento
- **RNF-001**: Tiempo de carga máximo de 3 segundos por página
- **RNF-002**: Soporte para 100 usuarios concurrentes
- **RNF-003**: Capacidad de almacenamiento inicial de 10GB

## Seguridad
- **RNF-004**: Autenticación JWT con tokens de refresco
- **RNF-005**: Validación de entrada contra inyecciones SQL
- **RNF-006**: Encriptación de contraseñas con bcrypt

## Usabilidad
- **RNF-007**: Interfaz responsive (móvil, tablet, desktop)
- **RNF-008**: Navegación intuitiva con menos de 3 clics para acciones principales
- **RNF-009**: Compatibilidad con Chrome, Firefox, Safari últimos 2 versions

## Mantenibilidad
- **RNF-010**: Código documentado y modular
- **RNF-011**: API RESTful con documentación OpenAPI
- **RNF-012**: Logs de errores y actividad del sistema

## Disponibilidad
- **RNF-013**: 95% de uptime en ambiente de producción
- **RNF-014**: Backup automático semanal de base de datos
- **RNF-015**: Tolerancia a fallos en servicios críticos

---

**Criterios**: Medibles, verificables y esenciales para la calidad del sistema.

*Equipo ED06 - FisiConnect*