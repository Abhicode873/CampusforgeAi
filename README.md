🚀 CampusForge AI - Engineering Students' AI Companion
AI-powered research, project management, and career acceleration for engineering students

🎯 Overview
CampusForge AI is an AI-powered platform designed for engineering college students. It helps you find project ideas, manage team projects, organize assignments, track productivity, build your LinkedIn[...]

✨ Main Features
1. 🔍 DeepSearch AI - Research & Project Ideas
Find comprehensive project ideas with difficulty levels, tech stacks, and implementation roadmaps for subjects like DBMS, DSA, Operating Systems, etc.

2. 📋 Assignment AI - Smart Task Breakdown
Transform assignments into structured plans with subtasks, study schedules, milestones, and resources with specialised functionality for each subjects like ML, Web Dev, DBMS etc.

3. 📊 Project Hub - Kanban Board
Manage team projects with visual Kanban boards (Research → Planning → In Progress → Testing → Launch). Assign tasks, set deadlines, and track progress.

4. 📈 Productivity Dashboard - Analytics & Insights
Track your productivity score, focus level, consistency, burnout risk, and get personalized study recommendations.

5. 💬 LinkedIn AI Persona - Content Generation (Unique feature)
Define your unique voice and generate LinkedIn posts with hashtags, optimal posting times, and engagement predictions.

6. 🔧 GitHub AI Assistant - Code Analysis ( Unique feature )
Upload your projects, get AI analysis for architecture quality, security issues, performance tips, and refactoring suggestions. Upload project zip: 1.Give the github personal access token and username 2.Give repo-name and upload zip file
3.Model analyses zip and generates Readme File. 4.Pushes the project to remote github repository with self-generated readme.md

🛠️ Tech Stack
Frontend: React 18 + Vite + Lucide Icons + Recharts
Backend: Node.js + Express + SQLite
AI: Google Gemini 3.5 Flash API
Security: JWT Authentication + bcryptjs Password Hashing

📦 Installation
Prerequisites
Node.js 20+ (Download)
Google Gemini API Key (Free at Google AI Studio)
Step 1: Clone & Setup Backend
git clone https://github.com/yourusername/campusforge-ai.git
cd campusforge-ai/server

npm install

# Create .env file
cat > .env << EOF
PORT=5000
GEMINI_API_KEY=your_gemini_api_key_here
JWT_SECRET=your_jwt_secret_key_here
NODE_ENV=development
EOF

npm start
Expected Output:

Connected to SQLite database.
Server is running on port 5000
Step 2: Setup Frontend
cd ../Client

npm install

# Create .env file
cat > .env << EOF
VITE_BACKEND_URL=http://localhost:5000/api
EOF

npm run dev
Expected Output:

VITE v5.1.0 ready in 289 ms
➜ Local: http://localhost:5173/
Step 3: Access Application
Open browser and go to: http://localhost:5173/

🔐 Environment Variables
Backend .env:
PORT=5000
NODE_ENV=development
GEMINI_API_KEY=your_google_gemini_api_key_here
JWT_SECRET=your_secret_key_here
CORS_ORIGIN=http://localhost:5173
Frontend .env:
VITE_BACKEND_URL=http://localhost:5000/api
Get Gemini API Key:

Visit Google AI Studio
Click "Get API Key" → "Create API Key"
Free tier: 60 requests/minute
📂 Project Structure
campusforge-ai/
├── Client/                    # React Frontend
│   ├── src/
│   │   ├── App.jsx           # Main component (6 tabs)
│   │   └── main.jsx          # Entry point
│   ├── package.json
│   └── vite.config.js
│
├── server/                    # Express Backend
│   ├── server.js             # Main server
│   ├── db.js                 # Database setup
│   ├── middleware/
│   │   └── authMiddleware.js # JWT validation
│   ├── routes/
│   │   ├── auth.js           # Auth endpoints
│   │   ├── ai.js             # AI features
│   │   ├── user.js           # User profile
│   │   ├── linkedin.js       # LinkedIn AI
│   │   └── github.js         # GitHub AI
│   └── package.json
│
└── README.md
🚀 Usage Guide
DeepSearch AI
Select subject (DBMS, DSA, OS, etc.)
Choose mode (Mini Project / Assignment / Exam Prep)
Enter your topic
Get project ideas, tech stack, roadmap, and exam tips
Project Hub
Enter project name and team size
Click "AI Generate Tasks"
Manage tasks in Kanban board
Assign team members and track progress
Assignment AI
Paste assignment description
Get breakdown into subtasks
View study schedule and deadlines
Download as reference
Productivity Dashboard
View productivity score (0-100)
Check focus, consistency, burnout risk
Get weekly study recommendations
Compare on leaderboard
LinkedIn AI
Create your persona (tone, style, vocabulary)
Generate posts matching your voice
Get hashtags and posting times
Share on LinkedIn
GitHub AI
Connect GitHub account
Upload your project (ZIP)
Get code analysis report
View refactoring suggestions
Push automatically to github
📡 API Endpoints
POST   /api/auth/signup             → Register
POST   /api/auth/login              → Login

POST   /api/ai/deepsearch           → Research
POST   /api/ai/assignment           → Assignment plan
POST   /api/ai/projecthub           → Kanban tasks

POST   /api/linkedin/profile        → Save persona
POST   /api/linkedin/generate       → Generate post

POST   /api/github/connect          → Connect account
POST   /api/github/upload-project   → Upload & analyze

GET    /api/user/profile            → Get profile
🤝 How to Contribute
1. Fork & Clone
git clone https://github.com/yourusername/campusforge-ai.git
cd campusforge-ai
2. Create Feature Branch
git checkout -b feature/your-feature-name
3. Make Changes & Test
# Make your changes
# Test locally
npm run dev  # Frontend
npm start    # Backend
4. Commit & Push
git add .
git commit -m "✨ feat: add awesome feature"
git push origin feature/your-feature-name
5. Create Pull Request
Provide clear description of changes
Include screenshots if UI changes
Follow existing code style
