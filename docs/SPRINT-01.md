# Sprint 01: Planificación y Fundación del Proyecto

Este documento detalla los objetivos, historias de usuario y tareas técnicas planificadas para el **Sprint 1** del sistema **Solicitud de Repuestos CPS**.

---

## 🎯 Objetivos del Sprint

1. **Establecer la Arquitectura Base**: Configurar el entorno de desarrollo local, base de datos y estructura de carpetas.
2. **Autenticación y Roles**: Implementar el sistema de inicio de sesión y gestión de roles básicos (Solicitante, Aprobador, Almacén).
3. **Módulo de Solicitud (Básico)**: Permitir a un usuario solicitante crear una solicitud de repuesto simple y ver su historial de solicitudes.

---

## 👥 Roles del Sistema

- **🧑‍💼 Solicitante (Operador/Técnico)**: Persona que necesita el repuesto y registra la solicitud.
- **🧑‍💻 Aprobador (Supervisor/Jefe)**: Persona encargada de revisar, autorizar o rechazar la solicitud.
- **📦 Administrador de Almacén**: Encargado de despachar el repuesto una vez aprobado.

---

## 📖 Historias de Usuario

### HU-01: Inicio de Sesión Seguro
> **Como** usuario del sistema (Solicitante, Aprobador, Almacén),  
> **quiero** iniciar sesión con mis credenciales,  
> **para** acceder a las funciones correspondientes a mi rol.

*   **Criterios de Aceptación:**
    *   [ ] Formulario con campos de correo/usuario y contraseña.
    *   [ ] Validación de credenciales contra la base de datos.
    *   [ ] Redirección automática según el rol asignado.
    *   [ ] Mensaje claro en caso de credenciales incorrectas.

### HU-02: Creación de Solicitud de Repuesto
> **Como** Solicitante,  
> **quiero** registrar una nueva solicitud de repuesto especificando cantidad, número de parte y descripción,  
> **para** que pueda ser revisada por mi supervisor.

*   **Criterios de Aceptación:**
    *   [ ] Formulario con campos: Código de máquina/equipo, Número de parte, Descripción, Cantidad, Prioridad (Alta/Media/Baja).
    *   [ ] Guardar la solicitud con estado inicial `Pendiente`.
    *   [ ] Validar que todos los campos obligatorios estén llenos antes del envío.

### HU-03: Historial de Solicitudes
> **Como** Solicitante,  
> **quiero** ver una lista de mis solicitudes realizadas y su estado actual,  
> **para** hacer seguimiento del proceso.

*   **Criterios de Aceptación:**
    *   [ ] Tabla/Lista que muestre: ID, Fecha, Máquina, Estado (`Pendiente`, `Aprobado`, `Rechazado`, `Despachado`).
    *   [ ] Filtros básicos por estado de solicitud.

---

## 🛠️ Tareas Técnicas

### 🏗️ Infraestructura y Arquitectura
- [ ] Definir el stack tecnológico definitivo (ej. React + Node.js, Next.js, Django, etc.).
- [ ] Diseñar el esquema de base de datos relacional (Tablas: `Usuarios`, `Roles`, `Solicitudes`, `Detalle_Solicitudes`).
- [ ] Configurar las variables de entorno y conexión a la base de datos.

### 🔑 Backend (API)
- [ ] Crear los endpoints de autenticación (`/api/auth/login`, `/api/auth/logout`).
- [ ] Crear el endpoint para registrar solicitudes (`POST /api/solicitudes`).
- [ ] Crear el endpoint para obtener el historial del usuario (`GET /api/solicitudes/usuario/:id`).

### 🎨 Frontend (UI/UX)
- [ ] Implementar la pantalla de Login con diseño responsive y moderno.
- [ ] Crear la vista del Dashboard principal del Solicitante.
- [ ] Diseñar e implementar el formulario de solicitud con validaciones interactivas.
- [ ] Crear la tabla del historial de solicitudes con estados visuales coloridos.

---

## 📈 Entregables del Sprint
*   [ ] Base de datos local configurada y migrada.
*   [ ] Código del backend y frontend integrado en la rama `main`.
*   [ ] Despliegue de prueba local o en staging.
