# 📊 MiniERP-Lite

**Open Source Dashboard for Small Businesses**

MiniERP-Lite is an open-source, lightweight application designed to help small businesses visualize, manage, and analyze their basic information without the need for an expensive or complex ERP. This project is designed to be **easy to install, modular, and educational** for both business owners and developers.

---

## 🚀 Project Goals

- Provide a lightweight and practical management solution for small businesses
- Serve as an example of clean architecture and best practices in .NET 8
- Act as a technical portfolio project, demonstrating backend, frontend, and documentation skills
- Promote open-source collaboration

---

## 📦 Technologies Used

### Backend
- .NET 8 Minimal API
- ADO.NET + Stored Procedures
- SQL Server or MySQL
- JWT for authentication

### Frontend
- React.js + Vite
- TailwindCSS
- Axios

---

## 🧩 Main Modules

### 🛒 Sales
- Sales records by date
- Details of sold products
- Daily or monthly totals

### 📦 Inventory
- Product CRUD operations
- Low stock alerts

### 💰 Finance
- Income and expense tracking
- Categorization by type
- Monthly and overall balance

### 👤 Users and Roles
- Basic login with JWT
- Time Zone Configuration
- Currency Configuration
- Language Configuration

---

## 📁 Project Structure

```plaintext
MiniERP-Lite/
├── ERP.API         → .NET Minimal REST API with authentication
├── ERP.Models      → Shared entity classes
├── ERP.DataAccess  → Database access with ADO.NET and SPs
├── ERP.Services    → Business services and validations
├── ERP.Frontend    → React + Tailwind (responsive dashboard)
├── docs/           →  Diagrams and technical documentation
└── README.md       → This file
```
---

## 🗃️ Database Model (Summary)

- ``User``: Id, Name, Role, Email, Password
- ``Product``: Id, Name, Stock, Price
- ``Sale``: Id, Date, UserId
- ``SaleDetail``: ProductId, Quantity, UnitPrice
- ``Transaction``: Type (Income/Expense), Date, Amount

🖼️ Full diagram available at /docs/ER.drawio`

---

## 📊 Dashboard (Frontend)

- Monthly sales chart (Recharts)
- Expenses by type chart
- Low stock product table

---

## ⚙️ How to Run the Project Locally

**Requirements**:
- .NET 8 SDK
- Node.js + npm
- Local SQL Server / MySQL

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
```
## 🤝 How to Contribute
¡Toda contribución es bienvenida!

All contributions are welcome!

- Fork the repository
- Create your branch: ``git checkout -b new-feature``
- Commit your changes: ``git commit -m "Add feature X"``
- Push to your branch: ``git push origin new-feature``
- Open a Pull Request

---

## 🪪 License
This project is under the MIT license.
You are free to use it for educational or commercial purposes, as long as appropriate credit is given.

---

## 💬 Why This Project?
- This system was created to:
- Apply design patterns and clean architecture principles
- Practice REST APIs, business logic, stored procedures, and security
- Provide value to small businesses needing practical open-source solutions
- Serve as a realistic portfolio project for developers looking to stand out

---

© 2025 Brandon Zamora  
MIT License — [Ver licencia](LICENSE)
