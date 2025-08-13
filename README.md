# 🏢 Udyam Digital Twin – MSME Registration Form

A modern web application to simulate and manage **Udyam MSME Registration**.  
Built with **Vite + React + Tailwind CSS** for the frontend and deployed on **Vercel**, with the backend running on **Render**.

---

## 🌐 Live Demo

- **Frontend (Vercel)**: [https://udyam-registration-alpha.vercel.app/](https://udyam-registration-alpha.vercel.app/)  
- **Backend API (Render)**: [https://udyam-registration-1.onrender.com/](https://udyam-registration-1.onrender.com/)

---

## 📌 Features

- 📄 **MSME Registration Form** – Aadhaar, PAN, Mobile number validation  
- ✅ **Real-time Validation** – Regex-based input checks  
- 🔄 **API Integration** – Connects frontend to backend endpoints  
- 🎨 **Responsive UI** – Tailwind CSS styling for all devices  
- ⚡ **Fast & Lightweight** – Vite bundler for blazing performance  

---

## 🛠️ Tech Stack

### **Frontend**
- **React** (Vite)
- **Tailwind CSS**
- **TypeScript**
- **Axios** for API calls

### **Backend**
- **Node.js** + **Express**
- **PostgreSQL** (Optional, if storing data)
- **dotenv** for environment variables

### **Hosting**
- **Frontend** – [Vercel](https://vercel.com/)  
- **Backend** – [Render](https://render.com/)

---

## 📂 Project Structure

udyam-digital-twin/
│
├── src/ # Frontend source code
│ ├── components/ # Reusable UI components
│ ├── pages/ # Page-level components
│ └── App.tsx # Main App component
│
├── public/ # Static assets
├── package.json # Project dependencies
├── tailwind.config.ts # Tailwind CSS config
├── vite.config.ts # Vite config
└── README.md # Project documentation

yaml
Copy
Edit

---

## 🚀 Getting Started (Local Development)

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/yourusername/udyam-digital-twin.git
cd udyam-digital-twin
2️⃣ Install Dependencies
npm install
3️⃣ Start the Frontend
npm run dev
4️⃣ Backend Setup (if running locally)
cd server
npm install
npm run dev
🌍 Deployment
Backend on Render
Create a new Web Service on Render
Connect your GitHub repo containing the backend
Set Build Command:
npm install
Set Start Command:
npm start
Deploy & note the backend API URL (e.g., https://udyam-registration-1.onrender.com)
Frontend on Vercel
Go to Vercel
Import your frontend repo
Set Environment Variable:
VITE_API_BASE=https://udyam-registration-1.onrender.com/api
Deploy 🚀
📌 API Endpoints
Method	Endpoint	Description
POST	/api/register	Submit Udyam form data
GET	/api/status/:id	Get registration status

📜 License
This project is licensed under the MIT License.
