# Classmate AI

<div align="center">
  <img src="frontend/logos/logoheaderAi.png" alt="Classmate AI Logo" width="400">
  <br>
  <h3>Your Personal AI Learning Assistant</h3>
  <p>
    <a href="https://ganesh714.github.io/classmate/"><strong>View Live Demo »</strong></a>
    <br />
    <br />
    <a href="#features">Features</a> ·
    <a href="#tech-stack">Tech Stack</a> ·
    <a href="#installation">Installation</a>
  </p>
</div>

---

## 📖 About The Project

**Classmate AI** is a comprehensive student productivity ecosystem designed to help users learn smarter, not harder. It combines an intelligent AI assistant with essential academic tools like task management, note-taking, and attendance tracking into a single, cohesive platform.

Unlike generic study tools, Classmate utilizes **Google's Gemini AI** to not just answer questions, but to actively help structure learning goals, generate detailed study phases, and convert chat interactions into actionable tasks and notes.

## ✨ Key Features

### 🤖 Intelligent Chatbot
* **Powered by Gemini**: Integration with Google's Gemini Pro for high-quality, context-aware responses.
* **Customizable Persona**: Configure the AI's tone (Friendly, Professional, Humorous) and custom instructions via Settings.
* **Voice Interaction**: Built-in speech-to-text support for hands-free querying.
* **Smart Actions**: One-click options to copy code, save responses as **Notes**, or convert study plans directly into the **Task Manager**.
* **Markdown & Code Support**: Full rendering for mathematical formulas, tables, and syntax-highlighted code blocks.

### 📋 Smart Task Manager
* **AI Goal Generation**: Input a broad goal (e.g., "Learn Python"), and the system automatically breaks it down into structured **Phases** and detailed **Tasks**.
* **Progress Tracking**: Visual progress bars for individual goals and overall completion.
* **Organization**: Pin and highlight important tasks.

### 📝 Dynamic Notes
* **Flexible Formats**: Support for both rich text notes and checklist-style notes.
* **Organization**: Filter, search, pin, and highlight notes for easy access.
* **Attachments**: Upload and view images or PDFs directly within your notes.

### 📊 Progress Dashboard
* **Visual Analytics**: Interactive charts (powered by Chart.js) displaying goal completion rates, task statistics, and note activity.
* **Activity Log**: A timeline view of your recent actions and accomplishments.

### 📅 Attendance Calculator
* **Safe-Bunk Calculator**: Calculate how many classes you can afford to miss while maintaining your target percentage.
* **Recovery Planner**: Determine how many consecutive classes you need to attend to recover a low attendance percentage.

### 🔐 Secure & Personalized
* **Authentication**: Secure User Registration and Login system using JWT (JSON Web Tokens).
* **Dark Mode**: Fully responsive dark/light theme toggling across the entire application.
* **Profile Management**: Update user details, avatars, and passwords.

---

## 🛠️ Tech Stack

### Frontend
* **HTML5 / CSS3**: Modern, responsive design with CSS Variables for theming.
* **JavaScript (Vanilla)**: Core logic for UI interactions and API integration.
* **Libraries**: 
    * `Chart.js` (Dashboard analytics)
    * `Marked.js` (Markdown rendering)
    * `Highlight.js` (Code syntax highlighting)
    * `FontAwesome` (Icons)

### Backend
* **Framework**: **FastAPI** (Python) for high-performance async API endpoints.
* **Database**: **MongoDB** (using `Motor` for async Python drivers).
* **Authentication**: `Passlib` (Bcrypt hashing) and `Python-Jose` (JWT tokens).
* **AI Integration**: `google-genai` SDK.

### Deployment
* **Configuration**: Ready for deployment on platforms like **Render** (configuration included in `backend/render.yaml`).

---

## 🚀 Installation & Local Setup

Follow these steps to get a local copy up and running.

### Prerequisites
* Python 3.9+
* MongoDB (Local or Atlas URI)
* Google Gemini API Key

### 1. Clone the Repository
```bash
git clone https://github.com/ganesh714/classmate.git
cd classmate
````

### 2\. Backend Setup

Navigate to the backend directory and set up the environment.

```bash
cd backend

# Create virtual environment
python -m venv venv

# Activate virtual environment
# Windows:
venv\Scripts\activate
# Mac/Linux:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 3\. Configure Environment Variables

Create a `.env` file in the `backend/` directory:

```env
# backend/.env
MONGO_URI=your_mongodb_connection_string
SECRET_KEY=your_secret_jwt_key
GEMINI_API_KEY1=your_primary_gemini_api_key
GEMINI_API_KEY2=your_backup_gemini_api_key_optional
```

### 4\. Run the Backend Server

```bash
# Inside the backend/ directory
uvicorn app.main:app --reload --host 0.0.0.0 --port 8000
```

The API will be available at `http://localhost:8000`.

### 5\. Frontend Setup

Since the frontend is static HTML/JS:

1.  Open `frontend/pages/Login page.html` directly in your browser.
2.  **Note**: You may need to update the `API_URL` or `serverUrl` variable in the `<script>` tags of the HTML files if your backend runs on a port other than the hardcoded production URL (defaults to `http://localhost:8000` for local dev, or update it to point to your local instance).

-----
# ClassMate
link -- https://ganesh714.github.io/classmate1/
