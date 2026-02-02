A continuación te dejo un **README.md completo, profesional y realista**, escrito en **inglés**, alineado con **pruebas técnicas académicas**, bien estructurado y **sin mencionar SPA** (se asume una aplicación web con JavaScript vanilla y routing manual). Está pensado para que un evaluador pueda **clonar, correr y entender el proyecto sin adivinar nada**.

Puedes copiarlo tal cual a tu repositorio y solo cambiar los datos personales y el nombre del proyecto cuando corresponda.

---

# Event Management Application – JavaScript Module 3

## Project Overview

This project is a performance assessment for **Module 3 – JavaScript**.  
The goal is to develop a web application for **event management**, where an event organizer can create, edit, and manage events, and visitors can view and register for available events.

The application implements **user authentication, role-based access control, protected routes, session persistence**, and **CRUD operations** using a simulated database powered by **json-server**.

The focus of this project is on **JavaScript logic**, data consistency, and correct application flow rather than advanced visual design.

---

## Technologies Used

- HTML5  
- Tailwind CSS  
- Vanilla JavaScript (ES6+)  
- json-server  
- Node.js  
- Local Storage  
- POSTMAN (API testing)

---

## Application Roles

The system supports two types of users:

### Administrator
- Can create, edit, and delete events.
- Can view all events and attendees.
- Has full access to dashboard routes.
- A default administrator user exists in `db.json`.

### Visitor
- Can view available events.
- Can register for events if capacity allows.
- Can view their own event registrations.
- Has restricted access based on role.

---

## Core Features

### 1. Authentication System
- User registration with role selection (admin / visitor).
- User login with credential validation.
- Role-based route protection.
- Redirect logic based on authentication state.

### 2. Session Persistence
- User session stored in **Local Storage**.
- Session remains active after page reload.
- Automatic redirection based on session state.

### 3. Data Consistency
- All CRUD operations are synchronized with `json-server`.
- Events and registrations are persisted in `db.json`.
- Capacity limits are enforced when registering attendees.

### 4. User Interface
- Responsive design using Tailwind CSS.
- Forms for login, registration, and event management.
- Separate views for administrators and visitors.
- Clear navigation and user feedback.

---

## Views

| View |
|----|
| Dashboard |
| Create Event |
| Edit Event |
| Login |
| Register |
| Not Found |

### Route Logic
- Unauthenticated users attempting protected routes are redirected to `not-found`.
- Authenticated users attempting `/login` or `/register` are redirected to `/dashboard`.

---

## Project Structure (Example)

```

/project-root
│
├── index.html
├── login.html
├── register.html
├── dashboard.html
├── js/
│   ├── auth.js
│   ├── router.js
│   ├── events.js
│   ├── storage.js
│   └── api.js
│
├── db.json
├── package.json
└── README.md

````

---

## Database (json-server)

The project uses **json-server** to simulate an API.

### Example Entities
- Users
- Events
- Attendees / Registrations

A default administrator user is included in `db.json`.

---

## How to Run the Project

### 1. Install Dependencies
```bash
npm install
````

### 2. Start json-server

```bash
npx json-server db.json --port 3000
```

### 3. Open the Application

Open `index.html` using a local server (Live Server recommended).

---

## API Testing

A **POSTMAN collection** is included to test:

* User authentication
* Event CRUD operations
* Event registration
* Data validation

---


## Author Information

* **Name:** Ulith Giraldo
* **Clan:** Turing

---

## Links
* **Github Repo:**

