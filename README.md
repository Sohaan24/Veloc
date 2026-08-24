<div align="center">
  <h1>🚀 Veloc</h1>
  <p><em>A Full-Stack AI Chat Assistant powered by the Groq API</em></p>

  <!-- Badges -->
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Vite-B73BFE?style=for-the-badge&logo=vite&logoColor=FFD62E" alt="Vite" />
  <img src="https://img.shields.io/badge/Node.js-43853D?style=for-the-badge&logo=node.js&logoColor=white" alt="Node.js" />
  <img src="https://img.shields.io/badge/Express.js-404D59?style=for-the-badge" alt="Express.js" />
  <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/Groq-F55036?style=for-the-badge" alt="Groq API" />
</div>

<br />

> **Veloc** is a MERN-stack chat application designed to replicate advanced AI conversational interfaces[cite: 2]. It leverages the Groq API for lightning-fast Large Language Model (LLM) inference, wrapped in a responsive React frontend[cite: 2].

## ✨ Core Features
* **AI Chat Integration:** Connects directly to LLMs via a dedicated `groqAPI.js` utility for high-speed AI responses[cite: 2].
* **Secure Authentication:** User signup and login handled securely with custom `authController.js` and `fetchUser.js` middleware[cite: 2].
* **Chat History Management:** Persists user conversations using MongoDB `Thread` and `User` models[cite: 2].
* **Dynamic UI:** A Vite-powered React frontend featuring a `Sidebar`, `Search` functionality, and a dedicated `Chat` interface[cite: 2].
* **Error Handling:** Centralized API error management via a custom `errorHandler.js` middleware[cite: 2].

## 🛠️ Tech Stack & Architecture

| Tier | Technologies Used |
| :--- | :--- |
| **Frontend** | React.js, Vite, Context API (`MyContext.jsx`)[cite: 2] |
| **Backend** | Node.js, Express.js[cite: 2] |
| **Database** | MongoDB (Mongoose schemas)[cite: 2] |
| **AI Integration**| Groq API[cite: 2] |
| **Testing**| API test suites (`api.test.js`)[cite: 2] |

## 📂 Repository Structure
```text
Veloc/
├── backend/
│   ├── controller/           # Logic for auth (authController.js) and chat (chatController.js)[cite: 2]
│   ├── middleware/           # errorHandler.js and fetchUser.js for request validation[cite: 2]
│   ├── model/                # Mongoose schemas (Thread.js, User.js)[cite: 2]
│   ├── route/                # Express API endpoints (authRoutes.js, chat.js)[cite: 2]
│   ├── test/                 # Backend testing (api.test.js)[cite: 2]
│   ├── utils/                # Helper functions including groqAPI.js and asyncHandler.js[cite: 2]
│   └── server.js             # Express application entry point[cite: 2]
└── frontend/
    ├── public/               # Static assets including vite.svg[cite: 2]
    ├── src/
    │   ├── assets/           # UI graphics including chatgpt.webp and react.svg[cite: 2]
    │   ├── App.jsx           # Main application routing[cite: 2]
    │   ├── AuthModel.jsx     # Authentication UI component[cite: 2]
    │   ├── Chat.jsx & .css   # Primary chat interface and styling[cite: 2]
    │   ├── MainLayout.jsx    # Core UI wrapper[cite: 2]
    │   ├── MyContext.jsx     # Global state management[cite: 2]
    │   ├── Search.jsx        # Search functionality component[cite: 2]
    │   ├── Sidebar.jsx & .css# Navigation and history sidebar[cite: 2]
    │   └── config.js         # Frontend configuration[cite: 2]
    └── vite.config.js        # Vite bundler configuration[cite: 2]
```

## ⚙️ Local Development Setup

### 1. Prerequisites
Ensure you have the following installed on your local machine:
* Node.js
* A MongoDB Atlas Account & Cluster
* A Groq API Key

### 2. Clone the Repository
```bash
git clone [https://github.com/Sohaan24/Veloc.git](https://github.com/Sohaan24/Veloc.git)
cd Veloc
```

### 3. Environment Variables
You must create `.env` files in both the `backend` and `frontend` directories.

**`/backend/.env`**
```env
MONGO_URI=your_mongodb_cluster_uri
JWT_SECRET=your_super_secret_key
GROQ_API_KEY=your_groq_api_key
PORT=5000
```

**`/frontend/.env`**
```env
VITE_API_URL=http://localhost:5000
```

### 4. Run the Backend
Open a terminal and navigate to the backend directory:
```bash
cd backend
npm install
npm run dev
```

### 5. Run the Frontend
Open a **new** terminal window and navigate to the frontend directory:
```bash
cd frontend
npm install
npm run dev
```
