# 🏗️ Clases Generadas - FisiConnect

Modelos y tablas generadas en PostgreSQL a partir del esquema definido en Fase 03.

---

## 📊 Tablas Principales

### **users**
- Almacena información de usuarios
- Campos: id, email, name, password, career, semester, points, avatar
- Índices: email (búsqueda rápida), points (ranking)

### **materials**
- Almacena materiales académicos subidos
- Campos: id, title, description, type, file_url, career, subject, semester, rating, downloads, views, user_id
- Índices: user_id, career, subject, rating, downloads

### **reviews**
- Almacena calificaciones y comentarios
- Campos: id, rating (1-5), comment, user_id, material_id
- Constraint: Un usuario, una reseña por material

---

## 🔗 Relaciones
                                                          
users (1) → (N) materials (Un usuario, múltiples materiales)                                                           
users (1) → (N) reviews (Un usuario, múltiples reseñas)                                                          
materials (1) → (N) reviews (Un material, múltiples reseñas)                                                          
                                                          
---

## 🛠️ Generación

**Herramienta:** SQLAlchemy ORM (Python)  
**Motor:** PostgreSQL 15  

Las tablas fueron creadas automáticamente mediante el esquema lógico-físico definido en Fase 03.

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025


