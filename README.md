# 💬 Chatting Application

A real-time **full-stack chat application** built with a **React + Vite** frontend and a **Node.js + Express** backend — supporting instant messaging and live online status via Socket.io.

---

## ✨ Features

- 🔐 User Registration & Login (JWT Authentication)
- 💬 Real-time messaging with **Socket.io**
- 👥 One-to-one private chat
- 🟢 Online / Offline user status indicator
- 📜 Chat history persistence
- 📱 Responsive design — works on mobile & desktop
- 🚪 Logout functionality

---

## 🗂️ Project Structure

```
Chatting-Application/
│
├── backend/
│   ├── src/
│   │   ├── controllers/      # Route handler logic
│   │   ├── models/           # Database models (User, Message)
│   │   ├── routes/           # API route definitions
│   │   ├── middleware/       # JWT auth middleware
│   │   ├── socket/           # Socket.io real-time logic
│   │   └── server.js         # Express + Socket.io entry point
│   ├── package-lock.json
│   └── package.json          # Backend dependencies
│
├── frontend/
│   ├── public/               # Static assets
│   ├── src/
│   │   ├── components/       # Reusable UI components
│   │   ├── pages/            # Login, Register, Chat pages
│   │   └── App.jsx           # Root component
│   ├── eslint.config.js      # ESLint configuration
│   ├── index.html            # HTML entry point
│   ├── vite.config.js        # Vite configuration
│   ├── package-lock.json
│   └── package.json          # Frontend dependencies
│
├── .gitignore
├── package.json              # Root dependencies
└── README.md                 # Project documentation
```

---

## 🛠️ Tech Stack

### Frontend
| Technology | Purpose |
|------------|---------|
| React.js | UI framework |
| Vite | Fast build tool & dev server |
| Socket.io-client | Real-time messaging |
| Axios | HTTP API requests |
| ESLint | Code linting |

### Backend
| Technology | Purpose |
|------------|---------|
| Node.js | Runtime environment |
| Express.js | REST API server |
| Socket.io | WebSocket real-time engine |
| MongoDB + Mongoose | Database & ORM |
| JWT | Authentication tokens |
| bcryptjs | Password hashing |

---

## ⚙️ Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) v16+
- [MongoDB](https://www.mongodb.com/) (local or Atlas)
- npm

---

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/Chatting-Application.git
cd Chatting-Application
```

---

### 2. Setup Backend

```bash
cd backend
npm install
```

Create a `.env` file inside the `backend/` folder:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret_key
```

Start the backend:

```bash
npm start
```

> ✅ Backend runs on: `http://localhost:5000`

---

### 3. Setup Frontend

```bash
cd ../frontend
npm install
npm run dev
```

> ✅ Frontend runs on: `http://localhost:5173` (Vite default port)

---

### 4. Open the App

Visit `http://localhost:5173`, register an account, and start chatting!

---

## 🔌 API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/auth/register` | Register a new user |
| POST | `/api/auth/login` | Login and receive JWT token |
| GET | `/api/users` | Get all users |
| GET | `/api/messages/:id` | Get chat messages with a user |
| POST | `/api/messages` | Send a new message |

---

## 🔄 Socket.io Events

| Event | Direction | Description |
|-------|-----------|-------------|
| `connection` | Server | User connects |
| `addUser` | Client → Server | Register user to socket |
| `getUsers` | Server → Client | Broadcast online users |
| `sendMessage` | Client → Server | Send a chat message |
| `getMessage` | Server → Client | Receive a chat message |
| `disconnect` | Server | User goes offline |

---

## 🚀 Deployment

### Backend → [Render](https://render.com) or [Railway](https://railway.app)
1. Push code to GitHub
2. Create a new Web Service and connect your repo
3. Set environment variables (`PORT`, `MONGO_URI`, `JWT_SECRET`)
4. Deploy!

### Frontend → [Vercel](https://vercel.com)
1. Push frontend folder to GitHub
2. Import project on Vercel
3. Set `VITE_API_URL=https://your-backend-url.com` in environment variables
4. Deploy!

---

## 🙌 Contributing

1. Fork the project
2. Create your branch: `git checkout -b feature/your-feature`
3. Commit changes: `git commit -m "Add your feature"`
4. Push: `git push origin feature/your-feature`
5. Open a Pull Request

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).

---

## ⭐ Show Your Support

If you like this project, give it a **⭐ star** on GitHub — it means a lot!

---

## 👤 Author

Made with ❤️ by **[Divyanshu Gupta](https://github.com/divyanshugupta72688)**
