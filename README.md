# 🏢 Udyam Registration - 

A responsive, modern recreation of the **first two steps** of the [Udyam Registration](https://udyamregistration.gov.in/UdyamRegistration.aspx) process.https://udyam-registration-alpha.vercel.app/  
Includes **web scraping** of the original fields, **dynamic form rendering**, **real-time validation**, and **backend integration** with PostgreSQL.

---

## 📌 Features

### 1. Web Scraping
- Scraped **Step 1** (Aadhaar + OTP Validation) and **Step 2** (PAN Validation) form fields.
- Extracted:
  - Field labels
  - Input types
  - Validation rules (regex, required fields)
  - Dropdown options
- Output stored as a **JSON schema** for dynamic rendering.

### 2. Responsive UI Development
- **Mobile-first** design using React/Next.js + TailwindCSS.
- Dynamic form rendering from the scraped JSON schema.
- Real-time client-side validation:
  - Aadhaar: `^[0-9]{12}$`
  - PAN: `^[A-Z]{5}[0-9]{4}[A-Z]{1}$`
- Step progress tracker (Step 1 → Step 2).
- Auto-fill **City/State** based on PIN code using PostPin API.

### 3. Backend Integration
- REST API (Node.js + Express + Prisma ORM) with:
  - Validation against scraped rules.
  - PostgreSQL storage.
- Database schema matches official Udyam fields.

### 4. Testing
- Jest unit tests for validation logic.
- API integration tests (e.g., invalid Aadhaar returns `400`).
- High edge-case coverage.

---

## 📂 Project Structure

udyam-assignment/
├─ frontend/ # Next.js + Tailwind CSS (UI)
├─ backend/ # Node.js + Express + Prisma (API)
├─ tests/ # Jest tests (frontend & backend)
├─ infra/ # Dockerfiles & docker-compose
├─ scripts/ # DB seed/migration scripts
├─ README.md
└─ .env.example



---

## 🚀 Getting Started

### 1️⃣ Clone the repository
```bash
git clone https://github.com/<your-username>/udyam-assignment.git
cd udyam-assignment
2️⃣ Set up environment variables
Copy .env.example to .env in both frontend and backend folders.

Backend .env
DATABASE_URL=postgresql://user:pass@localhost:5432/udyam
PORT=5000
POSTPIN_API_KEY=your_api_key

NEXT_PUBLIC_API_BASE=http://localhost:5000/api
3️⃣ Install dependencies

# Frontend
cd frontend
npm install

# Backend
cd ../backend
npm install
4️⃣ Database setup

# Run migrations (Prisma)
npx prisma migrate dev
5️⃣ Run the application
bash
Copy
Edit
# Backend
cd backend
npm run dev

# Frontend (in new terminal)
cd frontend
npm run dev
Frontend: http://localhost:3000
Backend API: http://localhost:5000/api

🧪 Running Tests

# Frontend tests
cd frontend
npm test

# Backend tests
cd backend
npm test
📡 API Endpoints
Method	Endpoint	Description
POST	/api/validate	Validate form data against rules
POST	/api/submit	Store submission in DB
GET	/api/schema	Fetch scraped JSON schema

Example request:

curl -X POST http://localhost:5000/api/validate \
-H "Content-Type: application/json" \
-d '{"aadhaar":"123412341234"}'


📸 Screenshots
Step 1 (Aadhaar)	Step 2 (PAN)

🐳 Docker Setup
bash
Copy
Edit
docker-compose up --build
This spins up:

Frontend (Next.js)

Backend (Node.js)

PostgreSQL

✅ Evaluation Checklist
 Scraped Step 1 & Step 2 fields with validation

 Dynamic form rendering from schema

 Responsive mobile-first UI

 Real-time Aadhaar/PAN validation

 Progress tracker

 Backend validation & Postgres storage

 Unit + API tests

 Dockerized deployment

📜 License
MIT License — free to use and modify.

