# Sprint 1: Reemplazar Google Forms y Google Sheets por un Sistema Web

Este documento detalla los objetivos, roles, funcionalidades y estados definidos para el **Sprint 1** del sistema **Solicitud de Repuestos CPS**, con el propósito de migrar el flujo actual basado en Google Forms y Google Sheets a una plataforma web propia y centralizada.

---

## 🎯 Objetivo

*   **Reemplazar Google Forms y Google Sheets por un sistema web dinámico**, mejorando el control, la trazabilidad de los estados de solicitud y la experiencia de usuario.

---

## 👥 Roles del Sistema

*   **👑 Administrador**: Gestión integral del sistema, control de usuarios/clientes y supervisión de solicitudes.
*   **🧑‍🔧 Técnico**: Personal que realiza las solicitudes de repuestos en campo o taller y realiza su seguimiento.
*   **📦 Almacenista**: Responsable de la gestión física de los repuestos, actualización de inventarios y despacho.

---

## 🛠️ Funcionalidades Planificadas

### 🔑 Autenticación (Login)
*   **Iniciar sesión**: Acceso seguro al sistema mediante credenciales de usuario.
*   **Cerrar sesión**: Salida segura del sistema para proteger la sesión del usuario.

### 🏢 Gestión de Clientes
*   **Crear**: Registrar nuevos clientes en el sistema.
*   **Editar**: Modificar la información de clientes existentes.
*   **Eliminar**: Dar de baja o eliminar registros de clientes.

### 📝 Gestión de Solicitudes
*   **Crear solicitud**: Formulario para registrar una nueva necesidad de repuesto.
*   **Adjuntar foto**: Permitir la carga de imágenes como referencia visual del repuesto solicitado.
*   **Cambiar estado**: Flujo de transición para actualizar el progreso de la solicitud.
*   **Ver historial**: Registro cronológico de los cambios y movimientos de cada solicitud.

---

## 🚦 Flujo de Estados

Las solicitudes pasarán por los siguientes estados definidos en el flujo de trabajo:

1.  **⏳ Pendiente**: Estado inicial tras el registro de la solicitud por parte del Técnico.
2.  **🔍 En revisión**: La solicitud está siendo evaluada por el equipo de supervisión o compras.
3.  **🛒 En compra**: Se ha procedido a la adquisición externa del repuesto requerido.
4.  **✅ Aprobado**: La solicitud ha sido autorizada y está lista para despacho.
5.  **🚚 Entregado**: El repuesto ha sido despachado y entregado al solicitante.
6.  **❌ Cancelado**: La solicitud ha sido anulada o rechazada.

---

## 📈 Tareas Técnicas del Sprint

### 🏗️ Base de Datos e Infraestructura
*   [ ] Diseñar el modelo de datos relacional para `Usuarios`, `Clientes`, `Solicitudes`, `Historial_Estados` y `Fotos`.
*   [ ] Configurar el almacenamiento de archivos (Local o Cloud Storage) para las fotos adjuntas.

### 🔑 Desarrollo Backend
*   [ ] Endpoints de Login y Logout.
*   [ ] CRUD completo de Clientes (`GET`, `POST`, `PUT`, `DELETE` `/api/clientes`).
*   [ ] Rutas de Solicitudes (Creación con upload de fotos, listado general, actualización de estado y consulta de historial).

### 🎨 Frontend (UI/UX)
*   [ ] Pantallas de inicio de sesión con diseño moderno y adaptativo (móvil y escritorio).
*   [ ] Módulo de administración de Clientes (tabla dinámica con formulario interactivo).
*   [ ] Formulario de creación de Solicitudes con previsualización de la foto adjunta.
*   [ ] Panel de control (Dashboard) con filtros por Estado y visualización de historial.
