# BMU ORBIT — Centralized Campus Ecosystem
> **"All Clubs. All Events. One Orbit."**  
> Official student platform for BML Munjal University that integrates clubs, campus events, registrations, contactless attendance check-in, local data persistence, and a full Node.js / Express / MongoDB Atlas backend.

---

## 📌 Project Architecture

BMU ORBIT features a dual-architecture designed for maximum performance and evaluation readiness:

1. **Frontend (SPA)**: Pure **HTML5, CSS3, and Vanilla JavaScript** — 11 dedicated, deep-linked views (`#home`, `#events`, `#clubs`, `#club-details`, `#event-details`, `#registration`, `#host-event`, `#myqr`, `#attendance`, `#json-manager`, `#settings`).
2. **Backend (Node.js & Express)**: RESTful API built on the **Model-Route-Controller (MRC)** pattern, connecting to an online **MongoDB Atlas** cluster via Mongoose with full CRUD operations and bcrypt user authentication.
3. **API Testing**: Pre-configured **Postman Collection** (`postman_collection.json`) for 1-click desktop testing of all endpoints.

---

## 👥 Contributors & Team Roles

This project was built collaboratively by our 5-member engineering team:

| Contributor | GitHub Profile | Workspace Branch | Assigned Feature Areas (Frontend & Backend) |
| :--- | :--- | :--- | :--- |
| **Kankanampati Chandrasekhar Gopi** *(Lead)* | [@kankanampatichandrasekhargopi25cse-ai](https://github.com/kankanampatichandrasekhargopi25cse-ai) | `chandrasekhar-workspace` | • Core App SPA Architecture & Navigation Router<br>• Responsive UI System & Search<br>• Backend Server Initialization (`index.js` / `app.js`) |
| **Naman Kumar Yadav** | [@NAMAN123924](https://github.com/NAMAN123924) | `naman-workspace` | • Campus Events Catalog & Society Showcase<br>• Dynamic Event Cards & Club Profiles<br>• Post CRUD Controller & Express Routes (`/api/v1/posts`) |
| **Uddeshya Dwivedi** | [@uddeshyadwivedi55-commits](https://github.com/uddeshyadwivedi55-commits) | `uddeshya-workspace` | • Real-Time Form Validation Engine (`@bmu.edu.in`)<br>• Vector SVG QR Code Digital Pass Generator<br>• User Authentication Model & Bcrypt Password Hashing (`user.model.js`) |
| **Bharat Gupta** | [@satyamicso](https://github.com/satyamicso) | `satyam-workspace` | • Host Event Proposal Workflow & Campus Coordination<br>• Category Workflow & Faculty Approval Logic<br>• Post Mongoose Database Schema & Models (`post.model.js`) |
| **Veerabhadra Rao** | [@VEERABHADRARAO-Cyber](https://github.com/VEERABHADRARAO-Cyber) | `veerabhadra-workspace` | • Attendance Verification Scanner Simulator & Web Audio Chimes<br>• Multi-Tier JSON Data Vault & Backup Export<br>• MongoDB Atlas Connection Module (`database.js`) & Postman Test Collection |

---

## 🏗️ Repository Structure

```
BMU-Orbit/
├── index.html                   # Main frontend SPA dashboard (11 views & modals)
├── style.css                    # Complete responsive styling & CSS variables
├── app.js                       # Vanilla JS frontend router, validation & QR engine
├── README.md                    # Project documentation & team guide
├── .gitignore                   # Excludes node_modules, .env, OS files
├── package.json                 # Backend dependencies (express, mongoose, bcrypt, dotenv, nodemon)
├── postman_collection.json      # 1-Click Postman import collection for API evaluation
├── .env.example                 # Environment variables template
├── assets/                      # Campus images and 20+ society crests
│   ├── bmu-logo-white.png
│   ├── bmu-logo-dark.png
│   ├── bmu-campus.jpg
│   └── clubs/
├── data/                        # Frontend seed JSON database
│   ├── events.json
│   ├── registrations.json
│   ├── attendance.json
│   └── proposals.json
└── backend/                     # Node.js + Express Backend Server
    └── src/
        ├── config/
        │   ├── constants.js     # Database name & configuration
        │   └── database.js      # MongoDB Atlas Mongoose connection
        ├── controllers/
        │   ├── post.controller.js # CRUD (Create, Read, Update, Delete)
        │   └── user.controller.js # Auth (Register, Login, Logout)
        ├── models/
        │   ├── post.model.js    # Mongoose Post model
        │   └── user.model.js    # Mongoose User model with bcrypt pre-save hook
        ├── routes/
        │   ├── post.route.js    # Routes for /api/v1/posts
        │   └── user.route.js    # Routes for /api/v1/users
        ├── app.js               # Express application middleware & route mounting
        └── index.js             # Server listener & database bootstrap
```

---

## 📡 Backend REST APIs

### 1. User Authentication (`/api/v1/users`)

| Method | Endpoint | Description |
| :---: | :--- | :--- |
| **POST** | `/api/v1/users/register` | Register a new user (hashes password with bcrypt) |
| **POST** | `/api/v1/users/login` | Login user (validates bcrypt password hash) |
| **POST** | `/api/v1/users/logout` | Logout user session |

### 2. Post CRUD Operations (`/api/v1/posts`)

| Operation | Method | Endpoint | Description |
| :---: | :---: | :--- | :--- |
| **Create (C)** | **POST** | `/api/v1/posts/create` | Adds a new post document to MongoDB |
| **Read (R)** | **GET** | `/api/v1/posts/getPosts` | Retrieves all post documents from MongoDB |
| **Update (U)** | **PATCH** | `/api/v1/posts/update/:id` | Updates a post document by its MongoDB `_id` |
| **Delete (D)** | **DELETE** | `/api/v1/posts/delete/:id` | Deletes a post document by its MongoDB `_id` |

---

## 🚀 How to Run on Your Laptop

### 1. Run the Frontend Dashboard
Simply double-click `index.html` or open it with VS Code Live Server in any browser.

### 2. Run the Backend Server
```bash
# 1. Install dependencies (only once)
npm install

# 2. Start the backend server
npm run dev
```
The server will start listening at: **`http://localhost:4000/`**

### 3. Test with Postman Desktop App
1. Open the **Postman Desktop App**.
2. Click **Import** (top left).
3. Select the file **`postman_collection.json`** located in the root of this repo.
4. All endpoints will load immediately with sample payloads and headers ready for evaluation!

---

## 🌐 Live Links

- **GitHub Repository**: [https://github.com/kankanampatichandrasekhargopi25cse-ai/BMU-ORBIT](https://github.com/kankanampatichandrasekhargopi25cse-ai/BMU-ORBIT)
- **Live Frontend (GitHub Pages)**: [https://kankanampatichandrasekhargopi25cse-ai.github.io/BMU-ORBIT/](https://kankanampatichandrasekhargopi25cse-ai.github.io/BMU-ORBIT/)

---

© 2026 BML Munjal University — BMU ORBIT
