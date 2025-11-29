<div align="center">

# 🏥 Health Management System

### A Modern Full-Stack Healthcare Platform

[![React](https://img.shields.io/badge/React-19.1.1-61DAFB?logo=react&logoColor=white)](https://reactjs.org/)
[![Node.js](https://img.shields.io/badge/Node.js-3.1.10-339933?logo=node.js&logoColor=white)](https://nodejs.org/)
[![Express](https://img.shields.io/badge/Express-5.1.0-000000?logo=express&logoColor=white)](https://expressjs.com/)
[![MongoDB](https://img.shields.io/badge/MongoDB-8.19.3-47A248?logo=mongodb&logoColor=white)](https://www.mongodb.com/)
[![TailwindCSS](https://img.shields.io/badge/Tailwind-4.1.17-06B6D4?logo=tailwindcss&logoColor=white)](https://tailwindcss.com/)
[![Vite](https://img.shields.io/badge/Vite-7.1.7-646CFF?logo=vite&logoColor=white)](https://vitejs.dev/)
[![License](https://img.shields.io/badge/License-ISC-blue.svg)](LICENSE)

<p align="center">
  <a href="#-features">Features</a> •
  <a href="#-tech-stack">Tech Stack</a> •
  <a href="#-getting-started">Getting Started</a> •
  <a href="#-project-structure">Structure</a> •
  <a href="#-api-endpoints">API</a> •
  <a href="#-contributing">Contributing</a>
</p>

</div>

---

## ✨ Features

### 🔐 Authentication & Security

- 🔒 **JWT-based Authentication** - Secure token-based user sessions
- 🛡️ **Password Encryption** - BCrypt hashing for secure password storage
- 🍪 **HTTP-only Cookies** - Protected authentication cookies
- 🔑 **Role-based Access Control** - Different permissions for users and admins

### 👤 User Management

- 📝 User registration and login
- 👨‍⚕️ Patient profile management
- 📊 Health records tracking
- 🔔 Real-time notifications with React Hot Toast

### 💊 Healthcare Features

- 📋 Medical appointment scheduling
- 📁 Health records management
- 💉 Prescription tracking
- 📈 Health analytics and reports

### 🎨 Modern UI/UX

- ⚡ Lightning-fast with Vite
- 🎨 Beautiful responsive design with Tailwind CSS
- 🌙 Clean and intuitive interface
- 📱 Mobile-friendly responsive layout

---

## 🛠️ Tech Stack

### Frontend

```javascript
{
  "framework": "React 19.1.1",
  "build-tool": "Vite 7.1.7",
  "styling": "Tailwind CSS 4.1.17",
  "routing": "React Router DOM 7.9.5",
  "state": "Zustand 5.0.8",
  "http": "Axios 1.13.2",
  "notifications": "React Hot Toast 2.6.0"
}
```

### Backend

```javascript
{
  "runtime": "Node.js 3.1.10",
  "framework": "Express 5.1.0",
  "database": "MongoDB with Mongoose 8.19.3",
  "auth": "JSON Web Token 9.0.2",
  "security": "BCrypt.js 3.0.3",
  "middleware": ["CORS", "Cookie Parser", "Dotenv"]
}
```

---

## 🚀 Getting Started

### Prerequisites

- **Node.js** (v16 or higher)
- **MongoDB** (v4.4 or higher)
- **npm** or **yarn**

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/Jenilson-BE/Health_Management.git
   cd Health_Management
   ```

2. **Install dependencies**

   **Backend Setup:**

   ```bash
   cd server
   npm install
   ```

   **Frontend Setup:**

   ```bash
   cd ../frontend
   npm install
   ```

3. **Environment Variables**

   Create a `.env` file in the `server` directory:

   ```env
   PORT=5000
   MONGODB_URI=your_mongodb_connection_string
   JWT_SECRET=your_jwt_secret_key
   NODE_ENV=development
   ```

4. **Start the Application**

   **Backend (Terminal 1):**

   ```bash
   cd server
   npm run dev
   ```

   **Frontend (Terminal 2):**

   ```bash
   cd frontend
   npm run dev
   ```

5. **Access the Application**
   - Frontend: `http://localhost:5173`
   - Backend API: `http://localhost:5000`

---

## 📁 Project Structure

```
Health_Management/
│
├── frontend/                # React Frontend
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Page components
│   │   ├── hooks/          # Custom React hooks
│   │   ├── utils/          # Utility functions
│   │   ├── styles/         # Global styles
│   │   └── App.jsx         # Root component
│   ├── public/             # Static assets
│   ├── index.html          # HTML template
│   ├── vite.config.js      # Vite configuration
│   └── package.json        # Frontend dependencies
│
├── server/                 # Express Backend
│   ├── config/            # Configuration files
│   ├── controllers/       # Route controllers
│   ├── middleware/        # Custom middleware
│   ├── models/            # MongoDB models
│   ├── routes/            # API routes
│   ├── index.js           # Server entry point
│   └── package.json       # Backend dependencies
│
└── README.md              # Project documentation
```

---

## 🔌 API Endpoints

### Authentication

| Method | Endpoint             | Description       |
| ------ | -------------------- | ----------------- |
| POST   | `/api/auth/register` | Register new user |
| POST   | `/api/auth/login`    | User login        |
| POST   | `/api/auth/logout`   | User logout       |
| GET    | `/api/auth/profile`  | Get user profile  |

### Health Records

| Method | Endpoint           | Description         |
| ------ | ------------------ | ------------------- |
| GET    | `/api/records`     | Get all records     |
| POST   | `/api/records`     | Create new record   |
| GET    | `/api/records/:id` | Get specific record |
| PUT    | `/api/records/:id` | Update record       |
| DELETE | `/api/records/:id` | Delete record       |

### Appointments

| Method | Endpoint                | Description          |
| ------ | ----------------------- | -------------------- |
| GET    | `/api/appointments`     | Get all appointments |
| POST   | `/api/appointments`     | Schedule appointment |
| PUT    | `/api/appointments/:id` | Update appointment   |
| DELETE | `/api/appointments/:id` | Cancel appointment   |

---

## 🎯 Key Features Implementation

### State Management with Zustand

```javascript
// Lightweight, fast, and scalable state management
import { create } from "zustand";

const useStore = create((set) => ({
  user: null,
  setUser: (user) => set({ user }),
}));
```

### Secure Authentication Flow

```javascript
// JWT token stored in HTTP-only cookies
// Protected routes with middleware
// Automatic token refresh mechanism
```

### Modern Styling with Tailwind CSS

```javascript
// Utility-first CSS framework
// Custom design system
// Responsive breakpoints
// Dark mode support ready
```

---

## 🧪 Development

### Available Scripts

**Frontend:**

```bash
npm run dev        # Start development server
npm run build      # Build for production
npm run preview    # Preview production build
npm run lint       # Run ESLint
```

**Backend:**

```bash
npm run dev        # Start with nodemon
npm start          # Start production server
```

---

## 🤝 Contributing

Contributions are always welcome! Here's how you can help:

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the ISC License - see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Jenilson-BE**

- GitHub: [@Jenilson-BE](https://github.com/Jenilson-BE)

---

## 🙏 Acknowledgments

- React team for the amazing framework
- MongoDB for the flexible database
- Tailwind CSS for the utility-first CSS framework
- Vite for the lightning-fast build tool
- All contributors and supporters

---

<div align="center">

### ⭐ Star this repository if you find it helpful!

**Made with ❤️ by Jenilson-BE**

</div>
