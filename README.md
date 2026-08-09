# Interview AI — AI-Powered Interview Prep Tool

I built this project to solve a real problem I kept running into — spending hours trying to figure out what questions a company might ask, what skills I'm missing, and how to actually prepare in a structured way. So I built a tool that does all of that automatically.

You paste a job description, upload your resume (or just describe yourself), and the AI generates a full interview strategy tailored to you — technical questions, behavioral questions, skill gaps, and a day-by-day prep plan. It also rewrites your resume to better match the job.

---

## What it does

- **Match Score** — tells you how well your profile fits the job (0–100)
- **Technical Questions** — with the interviewer's intention and a model answer for each
- **Behavioral Questions** — same format, focused on soft skills
- **Skill Gap Analysis** — highlights what you're missing and how critical each gap is
- **Preparation Roadmap** — a day-wise plan to get you ready
- **Resume Download** — generates a tailored, ATS-friendly resume as a PDF

---

## Tech Stack

**Frontend** — React 19, React Router v7, Vite, SCSS  
**Backend** — Node.js, Express, MongoDB (Mongoose), JWT auth  
**AI** — Google Gemini API (`@google/genai`)  
**PDF** — Puppeteer  

---

## Running locally

### Prerequisites
- Node.js 18+
- A MongoDB database (local or Atlas)
- A Google Gemini API key → [get one here](https://aistudio.google.com/apikey)

---

### 1. Clone the repo

```bash
git clone https://github.com/ManishKumar1307/Interview-GenAI-Project.git
cd Interview-GenAI-Project
```

### 2. Setup the Backend

```bash
cd Backend
npm install
```

Create a `.env` file inside `Backend/`:

```env
MONGO_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
GOOGLE_GENAI_API_KEY=your_gemini_api_key
```

Start the server:

```bash
npm run dev
```

Backend runs on `http://localhost:3000`

---

### 3. Setup the Frontend

```bash
cd Frontend
npm install
npm run dev
```

Frontend runs on `http://localhost:5173`

---

## Folder Structure

```
├── Backend/
│   ├── server.js
│   └── src/
│       ├── config/        # DB connection
│       ├── controllers/   # Auth & Interview logic
│       ├── middlewares/   # JWT auth, file upload
│       ├── models/        # User, Interview Report, Blacklist
│       ├── routes/        # API routes
│       └── services/      # Gemini AI + Puppeteer PDF
│
└── Frontend/
    └── src/
        ├── features/
        │   ├── auth/       # Login, Register
        │   └── interview/  # Home, Interview report pages
        └── style/
```

---

## Live Demo

Frontend deployed on Vercel → [interview-gen-ai-project-alpha.vercel.app](https://interview-gen-ai-project-alpha.vercel.app)

---

## Author

Made by **Manish Kumar** — [manishkumar-dev.in](https://manishkumar-dev.in/)
