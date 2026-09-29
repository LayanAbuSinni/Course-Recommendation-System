# 🎓 Course Recommendation System

A premium, AI-powered platform designed to provide Israeli teachers with personalized course recommendations from the **MATAK (מטח)** catalog. Leveraging **Google's Gemini 1.5 Pro AI**, the system understands teacher profiles and past experiences to suggest the most relevant professional development opportunities.

---

## 🚀 System Flow

The application follows a streamlined journey to ensure highly accurate recommendations:

1.  **Welcome**: Introduction to the platform and anonymous authentication.
2.  **Teacher Profile**: Capture of professional details (Sector, Role, Language, etc.).
3.  **Course Selection**: A searchable database of **635 real courses** where teachers mark their current or past courses.
4.  **Intelligent Chat**: A context-aware AI assistant that provides tailored recommendations based on the teacher's unique profile and selections.
5.  **Experience Survey**: An automated feedback loop to evaluate the AI's effectiveness.

---

## ✨ Key Features

-   **🤖 AI-Powered Intelligence**: Integrates **Google Gemini 1.5 Pro** for deep contextual understanding of teacher needs.
-   **📚 Extensive Catalog**: Includes **635 courses** mapped from real MATAK data, organized into **76 categories**.
-   **🔍 Advanced Search & Filter**: Real-time searching through the course catalog to find relevant professional development history.
-   **💾 Auto-Saving Results**: Automatically saves chat conversations and survey results to **Firebase Firestore** for session persistence.
-   **⚡ Performance Optimized**: Fast, responsive UI built with React and TypeScript, featuring smooth transitions and micro-animations.
-   **🛡️ Secure & Lightweight**: Uses Firebase Anonymous Authentication for a friction-free user experience while maintaining data isolation.

---

## 🛠️ Tech Stack

-   **Frontend**: React 18, TypeScript, React Router v6
-   **AI Engine**: Google Gemini API (@google/generative-ai)
-   **Backend/Database**: Firebase (Authentication & Cloud Firestore)
-   **Styling**: Vanilla CSS with modern Design Tokens (Glassmorphism & Gradients)
-   **Scripts**: Custom Node.js scripts for Excel-to-TypeScript data conversion

---

## 📁 Project Structure

```text
src/
├── components/           # Main UI Components
│   ├── Welcome.tsx      # Entry point & anonymous login
│   ├── TeacherInfo.tsx  # Profile data collection
│   ├── CourseSelection.tsx # 635 searchable courses
│   ├── Chat.tsx         # AI Chat interface
│   ├── Survey.tsx       # Post-chat feedback
│   └── ProtectedRoute.tsx # Route security
├── config/              # Configuration (Firebase, Gemini)
├── contexts/            # State Management (AuthContext)
├── data/                # Static Data (Generated course catalog)
├── types/               # TypeScript Definitions
├── App.tsx              # Routing and Keep-alive logic
└── index.css            # Global premium design system
```

---

## ⚙️ Setup & Installation

### 1. Prerequisites
- Node.js (v16+)
- npm

### 2. Configuration
Create a `.env` file in the root directory and add your credentials:

```env
# Gemini AI
REACT_APP_GEMINI_API_KEY=your_gemini_api_key

# Firebase
REACT_APP_FIREBASE_API_KEY=your_api_key
REACT_APP_FIREBASE_AUTH_DOMAIN=your_project.firebaseapp.com
REACT_APP_FIREBASE_PROJECT_ID=your_project_id
REACT_APP_FIREBASE_STORAGE_BUCKET=your_project.appspot.com
REACT_APP_FIREBASE_MESSAGING_SENDER_ID=your_sender_id
REACT_APP_FIREBASE_APP_ID=your_app_id
```

### 3. Installation
```bash
# Install dependencies
npm install

# (Optional) Update course data from Excel
npm run convert-courses
```

### 4. Running the Development Server
```bash
npm run dev
```

---

## 📦 Available Scripts

-   `npm run dev`: Starts the application in development mode.
-   `npm run build`: Bundles the app for production.
-   `npm run convert-courses`: Converts the `מיפוי קורסי מטח1 (3).xlsx` file into a usable TypeScript data file.
-   `npm start`: Serves the production build (requires `serve` package).

---

## 📊 Data Management

The system is built to be data-driven. The course list is maintained in an Excel file located in `src/components/מיפוי קורסי מטח1 (3).xlsx`. To update the system with new courses, simply replace the file and run `npm run convert-courses`.

---

## 🧪 Security & Privacy
-   **No Personal Data Required**: The system uses anonymous accounts.
-   **Secure API Handling**: Gemini API keys are handled via client-side environment variables (ensure they are restricted in the Google Cloud Console).
-   **Firestore Rules**: Database access is restricted to authenticated users only.

---

Built with ❤️ for the Teaching Community.