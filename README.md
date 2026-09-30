# CareerAI - AI-Powered Career Readiness Platform

A full-stack, enterprise-grade web application designed to accelerate student career readiness through transcript analysis, skill benchmarking, ATS resume review, AI mock interview simulations, and intelligent opportunity matching.

---

## 🛠️ Tech Stack

- **Frontend**: React 18, Tailwind CSS, Lucide Icons, Canvas-Confetti, Vite.
- **Backend**: Node.js, Express.js, REST API architecture.
- **Data & Schema**: Relational SQL Schema (`backend/db/schema.sql`) and structured JSON data layer (`backend/data/dummyData.json`).
- **AI Engine**: Intelligent heuristic and rule-based diagnostic engine (`backend/services/aiService.js`) with support for LLMs.

---

## 🌟 Key Features & Dashboard Modules

### 1. 👤 Student Profile & Academic Transcripts
- **Profile Overview**: Displays student bio, university, degree, graduation year, cumulative GPA (3.84/4.00), and total credits.
- **Academic Transcripts**: Detailed semester-by-semester courses with credit weighting, letter grades, grade points, and semester GPA calculations.
- **Skills & Course Endorsements**: Categorized technical skills (Languages, AI & ML, Frameworks, Backend, Databases, DevOps & Cloud) with proficiency bars and verified coursework tags.
- **Target Role Manager**: Easily add, remove, and select primary career objectives (e.g., AI/ML Engineer, Full Stack Developer, Cloud Architect).

### 2. 📊 Skill Gap & Benchmark Analysis
- **Live Industry Benchmarks**: Evaluates student competencies against real market requirements for target roles.
- **Career Readiness Score**: Dynamic percentage gauge (e.g., 85% "Job Ready") with category weighting.
- **Skill Gap Matrix**:
  - **Mastered Competencies**: High proficiency with course verification.
  - **Developing Skills**: Skills in progress with points needed to hit benchmark.
  - **Missing Critical Gaps**: High-priority missing skills ranked by industry demand.
- **Personalized Upskilling Roadmap**: Curated courses, certifications, and hands-on projects with durations and syllabus links.

### 3. 📄 AI Resume & ATS Review
- **ATS Diagnostic Score**: Composite 0-100 score analyzing:
  - Keyword density & alignment with target role.
  - Quantifiable impact metrics (percentages, dollar amounts, throughput).
  - Action verb vigor (power verbs vs weak passive verbs).
  - Single-column parser compliance.
- **Keyword Gap Checklist**: Highlights detected keywords vs missing high-priority terms.
- **AI Bullet Point Enhancer (STAR Method)**: Compares weak bullets with AI-generated high-impact accomplishments, explaining the architectural rationale behind the improvement.

### 4. 🎙️ AI Mock Interview Simulator
- **Role-Based Question Bank**: Questions for AI/ML Engineer, Full Stack Developer, and Cloud Architect.
- **Interactive Practice**: Real-time timer, architectural hint toggles, text and simulated voice response.
- **Instant AI Scorecard**: Multi-dimensional grading covering Technical Depth, Communication & Clarity, and Problem Solving.
- **Exemplary Model Answers**: 1-click comparison against 100% benchmark solutions.
- **Performance History**: Tracks progress over time.

### 5. 💼 Opportunities & Direct Match Engine
- **Dynamic Student Match Scores**: Real-time percentage match (e.g. 94% Match) computed by matching the student's verified skills against job requirements.
- **Granular Filters**: Filter by Type (Internship vs Full-time), Workplace (Remote, Hybrid, Onsite), and Match Threshold.
- **Skill Tag Highlights**: Matched skills in green, missing skills in red.
- **Application Tracker**: 1-click status updates (Saved, Applied, Interviewing) with pipeline metrics.

---

## 🚀 Getting Started

### Prerequisites
- Node.js (v18 or newer recommended, tested on Node v24)
- npm

### Installation & Run

1. **Install Dependencies**:
   ```bash
   # In root directory
   npm run install:all
   ```

2. **Start Both Backend and Frontend**:
   ```bash
   npm run dev
   ```
   - **Frontend**: [http://localhost:3000](http://localhost:3000)
   - **Backend API**: [http://localhost:5000](http://localhost:5000)
   - **API Health Check**: [http://localhost:5000/api/health](http://localhost:5000/api/health)

---

## 📂 Project Structure

```
CareerAI/
├── backend/
│   ├── data/
│   │   └── dummyData.json         # Comprehensive student, job, and interview data
│   ├── db/
│   │   └── schema.sql             # Relational database schema
│   ├── routes/
│   │   ├── interview.js           # Mock interview endpoints
│   │   ├── opportunities.js       # Job board & match engine endpoints
│   │   ├── resume.js              # ATS analysis & bullet optimizer endpoints
│   │   ├── skills.js              # Skill gap & roadmap endpoints
│   │   └── students.js            # Student profile & transcript endpoints
│   ├── services/
│   │   └── aiService.js           # Core algorithmic scoring & ATS evaluation
│   ├── package.json
│   └── server.js                  # Express API server entrypoint
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   │   ├── Header.jsx         # Top navbar with readiness gauge
│   │   │   └── Sidebar.jsx        # Responsive navigation sidebar
│   │   ├── pages/
│   │   │   ├── MockInterview.jsx  # AI interview simulator
│   │   │   ├── Opportunities.jsx  # Jobs & match engine
│   │   │   ├── ResumeReview.jsx   # ATS scanner & bullet enhancer
│   │   │   ├── SkillAnalysis.jsx  # Skill gap & upskilling roadmap
│   │   │   └── StudentProfile.jsx # Profile, transcripts, and verified skills
│   │   ├── services/
│   │   │   └── api.js             # API client
│   │   ├── App.jsx                # Main application component
│   │   ├── index.css              # Tailwind styles & theme
│   │   └── main.jsx               # React DOM entry
│   ├── index.html
│   ├── package.json
│   ├── tailwind.config.js
│   └── vite.config.js
├── package.json
└── README.md
```
