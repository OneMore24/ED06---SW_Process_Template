# 📦 Módulos del Sistema - FisiConnect

Descripción de los módulos principales que componen el prototipo FisiConnect, organizados por capa arquitectónica.

---

## 🏗️ Arquitectura General
                                                                                                
┌─────────────────────────────────────┐                                                                                                 
│ FRONTEND (Next.js) │                                                                                                
│ - Componentes UI │                                                                                                
│ - Páginas │                                                                                                
│ - Context API │                                                                                                
└──────────────┬──────────────────────┘                                                                                                
│ HTTP/REST API                                                                                                
┌──────────────▼──────────────────────┐                                                                                                
│ BACKEND (FastAPI) │                                                                                                
│ - Routers (Endpoints) │                                                                                                
│ - CRUD Operations │                                                                                                
│ - Modelos │                                                                                                
└──────────────┬──────────────────────┘                                                                                                
│ SQLAlchemy ORM                                                                                                
┌──────────────▼──────────────────────┐                                                                                                
│ BASE DE DATOS (PostgreSQL) │                                                                                                
│ - users, materials, reviews │                                                                                                
└─────────────────────────────────────┘                                                                                                
                                                                                                
---

## 🎨 Módulos Frontend

### **1. Módulo de Autenticación**
**Rutas:**
- `/login` - Inicio de sesión
- `/register` - Registro de usuario

**Componentes:**
- `LoginForm` - Formulario de login
- `RegisterForm` - Formulario de registro
- `AuthContext` - Gestión de sesión con JWT

**Funcionalidad:**
- Validación de credenciales
- Registro de nuevos usuarios
- Persistencia de token JWT
- Redirección según estado de autenticación

---

### **2. Módulo de Materiales**
**Rutas:**
- `/` - Dashboard principal
- `/materials/:id` - Detalle de material
- `/upload` - Subir material

**Componentes:**
- `MaterialCard` - Tarjeta de material
- `SearchFilters` - Filtros de búsqueda
- `FileUploadZone` - Zona de subida de archivos
- `MaterialDetail` - Vista detallada

**Funcionalidad:**
- Listado de materiales con paginación
- Búsqueda con filtros múltiples
- Subida de archivos con validación
- Descarga de materiales
- Visualización de detalles completos

---

### **3. Módulo de Reseñas**
**Componentes:**
- `ReviewForm` - Formulario de calificación
- `ReviewCard` - Tarjeta de reseña
- `RatingStars` - Estrellas interactivas

**Funcionalidad:**
- Calificar materiales (1-5 estrellas)
- Agregar comentarios
- Visualizar reseñas de otros usuarios
- Cálculo automático de promedio

---

### **4. Módulo de Gamificación**
**Rutas:**
- `/leaderboard` - Ranking de usuarios

**Componentes:**
- `Leaderboard` - Tabla de clasificación
- `PointsNotification` - Notificación de puntos
- `BadgeDisplay` - Insignias (futuro)

**Funcionalidad:**
- Mostrar top 50 usuarios
- Visualizar puntos propios
- Ver posición en ranking

---

### **5. Módulo de Perfil**
**Rutas:**
- `/profile` - Perfil de usuario

**Componentes:**
- `ProfileStats` - Estadísticas personales
- `MyMaterials` - Lista de materiales propios
- `AvatarUpload` - Subida de avatar

**Funcionalidad:**
- Ver estadísticas (materiales, descargas, vistas)
- Gestionar materiales propios
- Actualizar información personal

---

## ⚙️ Módulos Backend

### **1. Módulo de Autenticación (auth.py)**
**Endpoints:**
- `POST /auth/register` - Registrar usuario
- `POST /auth/login` - Iniciar sesión

**Funcionalidad:**
- Hashing de contraseñas con bcrypt
- Generación de JWT tokens
- Validación de credenciales

---

### **2. Módulo de Materiales (materials.py)**
**Endpoints:**
- `GET /api/materials` - Listar materiales con filtros
- `GET /api/materials/{id}` - Obtener detalle
- `POST /api/materials` - Subir material
- `GET /api/materials/{id}/download` - Descargar archivo

**Funcionalidad:**
- CRUD completo de materiales
- Búsqueda con filtros dinámicos
- Incremento de contadores (vistas, descargas)
- Asignación de puntos al autor

---

### **3. Módulo de Reseñas (reviews.py)**
**Endpoints:**
- `GET /api/materials/{id}/reviews` - Listar reseñas
- `POST /api/reviews` - Crear reseña

**Funcionalidad:**
- Guardar calificaciones y comentarios
- Validar usuario autenticado
- Restricción: una reseña por usuario por material
- Actualizar promedio de calificación
- Asignar puntos al autor (+10 si rating ≥ 4)

---

### **4. Módulo de Usuarios (users.py)**
**Endpoints:**
- `GET /api/users/me` - Perfil actual
- `GET /api/users/leaderboard` - Top 50 ranking
- `GET /api/users/{id}` - Perfil de usuario
- `PUT /api/users/me` - Actualizar perfil

**Funcionalidad:**
- Obtener datos de usuario
- Calcular estadísticas en tiempo real
- Generar ranking dinámico
- Actualizar información personal

---

## 🗄️ Módulo de Base de Datos

### **Modelos (models/)**
- `User` - Usuarios del sistema
- `Material` - Materiales académicos
- `Review` - Calificaciones y comentarios

### **CRUD (crud/)**
- `crud_user.py` - Operaciones de usuarios
- `crud_material.py` - Operaciones de materiales
- `crud_review.py` - Operaciones de reseñas

**Funcionalidad:**
- Abstracción de operaciones de BD
- Queries optimizados con SQLAlchemy
- Manejo de relaciones entre tablas

---

## 📊 Diagrama de Módulos
                                                                                               
FRONTEND MODULES                                                                                               
├── Auth Module (Login/Register)                                                                                               
├── Materials Module (Dashboard/Detail/Upload)                                                                                               
├── Reviews Module (Rating/Comments)                                                                                               
├── Gamification Module (Leaderboard/Points)                                                                                               
└── Profile Module (Stats/My Materials)                                                                                               
                                                                                               
BACKEND MODULES                                                                                               
├── Auth Module (JWT/bcrypt)                                                                                               
├── Materials Module (CRUD/Search/Download)                                                                                               
├── Reviews Module (CRUD/Rating Calc)                                                                                               
└── Users Module (Profile/Leaderboard/Stats)                                                                                               
                                                                                               
DATABASE LAYER                                                                                               
└── Models + CRUD Operations                                                                                               
                                                                                                                                                                            
---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025
