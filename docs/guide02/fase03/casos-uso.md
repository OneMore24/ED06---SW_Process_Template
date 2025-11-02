# Diagrama de Casos de Uso - FisiConnect

## 📊 Diagrama General de Casos de Uso

![Diagrama de Casos de Uso FisiConnect](../../assets/recursos/casos-uso.png)
*Diagrama UML de casos de uso que representa las funcionalidades principales del sistema FisiConnect*

---

## Documentación de Casos de Uso

### **Caso de Uso: Registro de Usuario con Identidad Institucional**

**ID:** CU-001  
**Actor:** Estudiante FISI  
**Descripción:** Permite el registro de nuevos usuarios mediante validación de correo institucional UNMSM  
**Precondiciones:** El usuario debe tener correo institucional @unmsm.edu.pe activo  

**Flujo Principal:**
1. El usuario accede al formulario de registro
2. Ingresa su correo institucional UNMSM
3. El sistema valida el formato del correo
4. El sistema envía correo de verificación
5. El usuario confirma su cuenta mediante el enlace
6. El sistema activa la cuenta y redirige al dashboard

**Reglas de Negocio:**
- RN-001: Solo se aceptan correos con dominio @unmsm.edu.pe
- RN-002: Cada correo solo puede registrar una cuenta
- RN-003: La verificación debe completarse en máximo 24 horas

---

### **Caso de Uso: Subir Materiales Académicos**

**ID:** CU-002  
**Actor:** Usuario registrado  
**Descripción:** Permite a usuarios autenticados subir materiales académicos a la plataforma  
**Precondiciones:** Usuario debe haber iniciado sesión  

**Flujo Principal:**
1. El usuario selecciona "Subir material"
2. Completa formulario con metadatos (título, descripción, categoría)
3. Selecciona archivo desde su dispositivo
4. El sistema valida formato y tamaño del archivo
5. El usuario confirma la publicación
6. El sistema almacena el material y notifica éxito

**Reglas de Negocio:**
- RN-004: Formatos permitidos: PDF, PPTX, DOCX, XLSX, MP4
- RN-005: Tamaño máximo por archivo: 300 MB
- RN-006: Metadatos obligatorios: título, categoría, descripción

---

### **Caso de Uso: Descargar Materiales**

**ID:** CU-003  
**Actor:** Usuario registrado  
**Descripción:** Permite descargar materiales académicos disponibles en la plataforma  
**Precondiciones:** Usuario autenticado, material disponible  

**Flujo Principal:**
1. El usuario busca material mediante filtros
2. Selecciona material de interés
3. Visualiza detalles y vista previa
4. Haz clic en "Descargar"
5. El sistema registra la descarga
6. El archivo se descarga al dispositivo

**Reglas de Negocio:**
- RN-007: Usuarios no autenticados solo ven vista previa limitada
- RN-008: Máximo 20 descargas por hora por usuario
- RN-009: Se registra estadística de descargas por material

---

### **Caso de Uso: Administrar Biblioteca Personal**

**ID:** CU-004  
**Actor:** Usuario registrado  
**Descripción:** Gestión de materiales guardados en la biblioteca personal del usuario  
**Precondiciones:** Usuario autenticado  

**Flujo Principal:**
1. El usuario accede a "Mi Biblioteca"
2. Visualiza materiales guardados organizados
3. Puede filtrar por categorías personales
4. Puede eliminar materiales de la biblioteca
5. Puede organizar en carpetas personalizadas
6. El sistema guarda los cambios en tiempo real

**Reglas de Negocio:**
- RN-010: Límite de 500 materiales en biblioteca personal
- RN-011: Los cambios se sincronizan automáticamente
- RN-012: Se mantiene historial de materiales eliminados por 30 días

---

### **Caso de Uso: Moderación de Contenido**

**ID:** CU-005  
**Actor:** Administrador  
**Descripción:** Gestión y validación de contenidos subidos por usuarios  
**Precondiciones:** Usuario con rol de administrador  

**Flujo Principal:**
1. El administrador accede al panel de moderación
2. Revisa materiales reportados o pendientes
3. Evalúa contenido según políticas
4. Aprueba, rechaza o solicita modificaciones
5. Notifica al usuario sobre la decisión
6. Actualiza estado del material en el sistema

**Reglas de Negocio:**
- RN-013: Los materiales inapropiados se rechazan inmediatamente
- RN-014: Los usuarios con 3 rechazos consecutivos son suspendidos
- RN-015: Todo material debe revisarse en máximo 48 horas

---

> **Nota del Equipo ED06**: Los casos de uso documentados representan las interacciones fundamentales entre los usuarios y el sistema FisiConnect, asegurando que todos los requisitos funcionales identificados en la Guía 01 estén adecuadamente cubiertos en el diseño del sistema.

*Equipo ED06 - FisiConnect*