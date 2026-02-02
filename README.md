Abrir configuración de VS Code:
Presiona Ctrl + , (Windows/Linux) o Cmd + , (Mac).

Buscar “Format on Save”:
En la barra de búsqueda escribe format on save. Aparecerá la opción Editor: Format On Save.
Actívala. Esto hará que VS Code intente formatear el documento automáticamente cada vez que guardes (Ctrl + S o Cmd + S).

Seleccionar un formateador por defecto (opcional):
Aunque no tengas Prettier, VS Code tiene formateadores integrados.

Ve a Ctrl + Shift + P → escribe Format Document With... → selecciona Configure Default Formatter.

Elige el formateador de VS Code que prefieras (por ejemplo, el que dice Built-in para JavaScript/TypeScript/HTML).

extensions

error lens.
indent-rainbow.
live server.
tailwind helpers.


flujo de habitos / needed.
M3/ 4JS/US needed.
ideahub / maybe.

---

# CRUDTASK – JavaScript Module 3

## Project Overview

This project is a performance assessment for **Module 3 – JavaScript**.
The goal is to develop a web application called **CRUDTASK** for **academic task management**, where regular users can manage their own tasks and profiles, and administrators can oversee system activity and manage all tasks.

The application implements **simulated user authentication, role-based access control, protected routes, session persistence**, and **CRUD operations** using a **fake API powered by JSON Server**.

The focus of this project is on **JavaScript logic, role handling, and correct application flow**, rather than advanced backend development or deployment.

---

## Technologies Used

- HTML5
- CSS3 (including frameworks like Tailwind, Bootstrap, Materialize, Foundation, or Bulma)
- Vanilla JavaScript (ES6+)
- JSON Server (fake API)
- LocalStorage or SessionStorage
- Figma (UI designs reference)

---

## Application Roles

The system supports two types of users:

### User

- Can register, log in, and manage their own tasks.
- Can view, create, edit, and delete tasks assigned to them.
- Can mark tasks as `pending`, `in progress`, or `completed`.
- Can view and edit their own profile.
- Access restricted to user-specific views only.

### Administrator

- Can log in through the same form and is redirected to the admin dashboard.
- Can view, edit, delete, and change the status of **all tasks** in the system.
- Can see general system metrics, including total tasks, pending tasks, and completed tasks.
- Optional: view all registered users.
- Has full access to admin-only views.

**Business Rule:** Users with the `user` role cannot access admin views, and admins do not use user-specific views.

---

## Core Features

### 1. Authentication System

- User registration with automatic role assignment (`user`).
- User login with credential validation against JSON Server.
- Role-based route protection to restrict access.
- Redirect logic depending on authentication state.

### 2. Session Persistence

- Session stored in **LocalStorage** or **SessionStorage**.
- Session remains active after page reload.
- Users without active sessions are redirected to the login page.

### 3. Task Management

- List, create, edit, and delete tasks.
- Task status can be changed (`pending`, `in progress`, `completed`).
- Users can only see and manage their own tasks.
- Admins can manage all tasks.

### 4. Dashboard & Metrics (Admin)

- Shows total tasks, pending tasks, completed tasks, and overall system metrics.
- Provides task management functionality for all users.

### 5. User Profile

- View personal information.
- Logout functionality.

### 6. Data Consistency

- All CRUD operations are synchronized with JSON Server.
- Role validation ensures secure access to data.
- Users cannot manipulate data directly in the browser without proper validation.

---

## Views

| View                    |
| ----------------------- |
| Login                   |
| Register                |
| Task Management (User)  |
| Profile (User)          |
| Admin Dashboard         |
| Task Management (Admin) |
| Not Found               |

### Route Logic

- Unauthenticated users attempting protected routes are redirected to `/login`.
- Authenticated users attempting `/login` or `/register` are redirected to their corresponding dashboard.
- Role-based access is enforced on all routes.

---

## Project Structure (Example)

```
/crudtask
│
├── index.html
├── login.html
├── register.html
├── dashboard.html
├── tasks.html
├── profile.html
├── js/
│   ├── auth.js
│   ├── router.js
│   ├── tasks.js
│   ├── storage.js
│   └── api.js
│
├── db.json
├── package.json
└── README.md
```

---

## Database (JSON Server)

The project uses **JSON Server** to simulate an API.

### Example Entities

- Users
- Tasks
- Optional: System Metrics

A default administrator user can be included in `db.json`.

---

## How to Run the Project

### 1. Install Dependencies

```bash
npm install
```

### 2. Start JSON Server

```bash
npx json-server db.json --port 3000
```

### 3. Open the Application

Open `index.html` using a local server (Live Server recommended).

---

## Figma Design Reference

The visual design and component structure are defined in Figma: *https://www.figma.com/design/K3PmKIOlfEsjnbwP54Yc2x/Sin-t%C3%ADtulo?node-id=33-2&t=Q7CZdp6XFatVh7wZ-1*

---

## Author Information

- **Name:** Ulith Giraldo
- **Clan:** Turing

---

## Links

- **Github Repo:** \*\*

---
