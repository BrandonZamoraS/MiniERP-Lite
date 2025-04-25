# 📊 MiniERP-Lite

**Dashboard Open Source para Pequeños Negocios**

MiniERP-Lite es una aplicación de código abierto y bajo consumo diseñada para ayudar a pequeños negocios a visualizar, administrar y analizar su información básica sin necesidad de un ERP costoso o complejo. Este proyecto está pensado para ser **fácil de instalar, modular y educativo**, tanto para dueños de negocio como para desarrolladores.

---

## 🚀 Objetivos del proyecto

- Ofrecer una solución liviana y práctica de gestión para pequeños negocios
- Servir como ejemplo de arquitectura limpia y buenas prácticas en .NET 8
- Funcionar como proyecto de portafolio técnico, demostrando habilidades backend, frontend y de documentación
- Promover la colaboración open source

---

## 📦 Tecnologías utilizadas

### Backend
- [.NET 8 Minimal API (native AOT)](https://learn.microsoft.com/en-us/aspnet/core/fundamentals/minimal-apis)
- ADO.NET + Stored Procedures
- SQL Server o MySQL
- JWT para autenticación

### Frontend
- React.js + Vite
- TailwindCSS
- Recharts (visualización)
- Axios

---

## 🧩 Módulos principales

### 🛒 Ventas
- Registro de ventas por fecha
- Detalles de productos vendidos
- Total por día o mes

### 📦 Inventario
- CRUD de productos
- Alerta de stock bajo

### 💰 Finanzas
- Registro de ingresos y gastos
- Clasificación por tipo
- Balance mensual y general

### ✅ Tareas internas
- Lista de tareas con estado (pendiente, en curso, terminada)
- Asignación opcional a usuarios

### 👤 Usuarios y roles
- Login básico con JWT
- Roles: `Admin`, `Empleado`
- Restricción de acceso por módulo

---

## 📁 Estructura del proyecto

```plaintext
MiniERP-Lite/
├── ERP.API         → API REST .NET Minimal con autenticación
├── ERP.Modelos     → Clases de entidad compartidas
├── ERP.Datos       → Acceso a BD con ADO.NET y SPs
├── ERP.Negocio     → Servicios y validaciones de negocio
├── ERP.Frontend    → React + Tailwind (dashboard responsive)
├── docs/           → Diagramas y documentación técnica
└── README.md       → Este archivo
```
---

## 🗃️ Modelo de base de datos (resumen)

- `Usuario`: Id, Nombre, Rol, Email, Contraseña
- `Producto`: Id, Nombre, Stock, Precio
- `Venta`: Id, Fecha, UsuarioId
- `VentaDetalle`: ProductoId, Cantidad, PrecioUnitario
- `Movimiento`: Tipo (Ingreso/Gasto), Fecha, Monto
- `Tarea`: Título, Estado, FechaLimite, AsignadoA

🖼️ Diagrama completo en `/docs/ER.drawio`

---

## 📊 Dashboard (Frontend)

- Gráfico de ventas por mes (Recharts)
- Gráfico de gastos por tipo
- Tabla de productos con stock bajo
- Lista de tareas internas pendientes

---

## ⚙️ Cómo correr el proyecto localmente

**Requisitos**:
- .NET 8 SDK
- Node.js + npm
- SQL Server / MySQL local

```bash
git clone https://github.com/tuusuario/MiniERP-Lite.git
cd MiniERP-Lite

# Backend
cd ERP.API
dotnet run

# Frontend
cd ERP.Frontend
npm install
npm run dev

## 🤝 ¿Cómo contribuir?
¡Toda contribución es bienvenida!

Haz un fork del repositorio

Crea tu rama: git checkout -b nueva-funcionalidad

Haz tu commit: git commit -m "Agrega funcionalidad X"

Push a tu rama: git push origin nueva-funcionalidad

Abre un Pull Request
```
---

## 🪪 Licencia
Este proyecto está bajo la licencia MIT.
Podés usarlo libremente para fines educativos o comerciales, siempre que se incluya el crédito correspondiente.

---

## 💬 ¿Por qué este proyecto?
- Este sistema surge como una forma de:

- Aplicar patrones de diseño y arquitectura limpia

- Practicar REST APIs, lógica de negocio, SPs y seguridad

- Ofrecer valor a pequeñas empresas que necesitan soluciones prácticas y open source

- Servir como un proyecto de portafolio realista para desarrolladores que buscan destacarse

---

© 2024 Brandon Zamora  
Licencia MIT — [Ver licencia](LICENSE)
