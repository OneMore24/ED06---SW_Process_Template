# Pseudocódigos - Requisitos Funcionales Mandatorios

## Pseudocódigo 01: Autenticación de Usuario

FUNCIÓN autenticarUsuario(correo, contraseña)
SI correo NO termina con "@unmsm.edu.pe" ENTONCES
    RETORNAR "Error: Correo institucional requerido"
FIN SI
usuario = BUSCAR_EN_BD(correo)
SI usuario NO existe ENTONCES
    RETORNAR "Error: Usuario no registrado"
FIN SI

SI verificarContraseña(contraseña, usuario.contraseña_hash) ENTONCES
    token = generarJWT(usuario.id, usuario.rol)
    RETORNAR { éxito: verdadero, token: token, usuario: usuario.datos }
SINO
    RETORNAR "Error: Credenciales incorrectas"
FIN SI
FIN FUNCIÓN

## Pseudocódigo 02: Búsqueda Avanzada de Materiales

FUNCIÓN buscarMateriales(termino_busqueda, filtros)
    resultados = []
    // Búsqueda por texto
    SI termino_busqueda NO está vacío ENTONCES
        materiales = BUSCAR_EN_BD(
            titulo CONTIENE termino_busqueda O 
            descripcion CONTIENE termino_busqueda
            )
        SINO
            materiales = OBTENER_TODOS_MATERIALES()
    FIN SI

// Aplicar filtros
PARA CADA filtro EN filtros HACER
    SI filtro.asignatura NO está vacío ENTONCES
        materiales = FILTRAR(materiales, asignatura = filtro.asignatura)
    FIN SI
    
    SI filtro.carrera NO está vacío ENTONCES
        materiales = FILTRAR(materiales, carrera = filtro.carrera)
    FIN SI
    
    SI filtro.semestre NO está vacío ENTONCES
        materiales = FILTRAR(materiales, semestre = filtro.semestre)
    FIN SI
    
    SI filtro.tipo_material NO está vacío ENTONCES
        materiales = FILTRAR(materiales, tipo = filtro.tipo_material)
    FIN SI
FIN PARA

// Ordenar por relevancia
materiales = ORDENAR_POR(materiales, 
    [calificacion_promedio DESC, fecha_subida DESC] )
    RETORNAR materiales
FIN FUNCIÓN

## Pseudocódigo 03: Sistema de Calificaciones

FUNCIÓN calificarMaterial(usuario_id, material_id, calificacion)
    // Validar rango de calificación
    SI calificacion < 1 O calificacion > 5 ENTONCES
        RETORNAR "Error: Calificación debe ser entre 1-5"
    FIN SI
    // Verificar si ya calificó
    calificacion_existente = BUSCAR_CALIFICACION(usuario_id, material_id)
    SI calificacion_existente EXISTE ENTONCES
        ACTUALIZAR_CALIFICACION(calificacion_existente.id, calificacion)
        SINO
            CREAR_CALIFICACION(usuario_id, material_id, calificacion)
    FIN SI

    // Recalcular promedio
    promedio = CALCULAR_PROMEDIO_CALIFICACIONES(material_id)
    ACTUALIZAR_PROMEDIO_MATERIAL(material_id, promedio)

    RETORNAR { éxito: verdadero, promedio_actual: promedio }
FIN FUNCIÓN

---

**Nota**: Estos pseudocódigos representan la lógica fundamental de los requisitos mandatorios más críticos del sistema FisiConnect.

*Equipo ED06 - FisiConnect*