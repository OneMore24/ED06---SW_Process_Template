# 🖥️ Requisitos de Hardware y Software

Se especifican los recursos técnicos necesarios para el desarrollo de FisiConnect.

---

## 💻 Hardware Mínimo Requerido

| Componente | Especificación |
|-----------|---|
| **RAM** | 8 GB (16 GB recomendado) |
| **Procesador** | Intel Core i5 / AMD Ryzen 5 o superior |
| **Almacenamiento** | 256 GB SSD |
| **Conectividad** | Internet 5 Mbps estable |

---

## 📦 Stack Tecnológico

### Frontend
- **Framework:** Next.js 14 (App Router)
- **Lenguaje:** TypeScript 5
- **Estilos:** Tailwind CSS 3
- **Componentes:** shadcn/ui
- **HTTP Client:** Fetch API nativa

### Backend
- **Framework:** FastAPI 0.104+
- **Lenguaje:** Python 3.11+
- **Base de Datos:** PostgreSQL 15
- **ORM:** SQLAlchemy 2.0
- **Autenticación:** JWT (python-jose)
- **Validación:** Pydantic V2

### Herramientas de Desarrollo
- **Editor:** Visual Studio Code
- **Versionado:** Git + GitHub
- **API Testing:** Postman
- **Base de Datos:** DBeaver / pgAdmin
- **Deployment:** Vercel (frontend), Railway (backend)

---
                                                                               
## 📋 Dependencias del Proyecto
                                                                               
### Frontend (package.json)                                                                               
next@14.0+                                                                               
react@18.0+                                                                               
typescript@5.0+                                                                               
tailwindcss@3.0+                                                                               
shadcn/ui@latest                                                                               
                                                                               
### Backend (requirements.txt)                                                                               
fastapi==0.104+                                                                               
sqlalchemy==2.0+                                                                               
psycopg2-binary==2.9+                                                                               
python-jose==3.3+                                                                               
passlib==1.7+                                                                               
python-dotenv==1.0+                                                                               
                                                                               
---

## 🎓 Desafíos Formativos

El stack tecnológico seleccionado representa un **desafío significativo** para el equipo:
- **TypeScript:** Tipado estático en JavaScript
- **FastAPI:** Framework moderno asíncrono
- **SQLAlchemy ORM:** Abstracción de base de datos
- **JWT:** Autenticación sin sesiones
- **Arquitectura Full Stack:** Integración frontend-backend

---

**Elaborado por:** Equipo ED06 - FisiConnect  
**Fecha:** Noviembre 2025 

