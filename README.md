# Static Code Analyzer — Frontend

A React-based web application for analyzing JavaScript source files. Paste or upload code, view quality metrics, manage analysis rules, organize projects, and export reports as PDF — all with dark/light theme support.

---

## Features

- **Code Analysis** — submit `.js` files and instantly see LOC, LLOC, SLOC, cyclomatic complexity, maintainability index, and comment statistics
- **Visual Charts** — bar, line, and pie charts powered by Chart.js to compare metrics across files
- **Analysis History** — browse and revisit all past analyses
- **Output Reports** — view detailed per-file breakdowns and export them to PDF
- **Rules Management** — create and toggle custom code quality rules with search support
- **Project Management** — group analyses into projects with PDF export per project
- **User Authentication** — register, login, and protected dashboard
- **Dark / Light Theme** — persistent theme toggle across the entire app
- **Voice Support** — Microsoft Cognitive Services Speech SDK integration
- **Toast Notifications** — real-time feedback on all actions

---

## Tech Stack

| Layer | Technology |
|---|---|
| Framework | React 18 |
| Build Tool | Vite 8 |
| Routing | React Router DOM v6 |
| UI | Bootstrap 5 + React Bootstrap |
| Charts | Chart.js + react-chartjs-2 |
| PDF Export | jsPDF + jspdf-autotable |
| Forms | Formik + Yup |
| Notifications | React Toastify |
| Icons | React Icons |
| Print | react-to-print |
| Speech | Microsoft Cognitive Services Speech SDK |

---

## Project Structure

```
Code-Analyzer/
├── public/
├── src/
│   ├── assets/             # Images and static assets
│   ├── components/
│   │   ├── Footer.jsx
│   │   ├── Layout.jsx
│   │   └── Navbar.jsx
│   ├── context/
│   │   ├── AuthContext.jsx     # Global auth state
│   │   ├── ThemeContext.jsx    # Dark/light theme
│   │   └── ToastContext.jsx    # Toast notification helper
│   ├── pages/
│   │   ├── Home.jsx            # Landing page
│   │   ├── Main.jsx            # Dashboard
│   │   ├── Login.jsx
│   │   ├── Register.jsx
│   │   ├── CodeAnalyzer.jsx    # Core analysis input
│   │   ├── OutputAnalysis.jsx  # Results + PDF export
│   │   ├── AnalysisGraph.jsx   # Chart visualizations
│   │   ├── HistoryPage.jsx     # Past analyses
│   │   ├── ManageRules.jsx     # Rules CRUD
│   │   ├── ProjectManagement.jsx
│   │   ├── AboutUs.jsx
│   │   └── Resources.jsx
│   ├── App.jsx
│   ├── main.jsx
│   └── index.css
├── .env                    # Environment variables
├── eslint.config.js
├── index.html
└── vite.config.js
```

---

## Getting Started

### Prerequisites

- Node.js v18+
- Backend server running (see [Code-Analyzer-Backend](../Code-Analyzer-Backend/README.md))

### Installation

```bash
git clone <repo-url>
cd Code-Analyzer
npm install
```

### Environment Variables

Create a `.env` file in the project root:

```env
VITE_API_URL=http://localhost:4000/api
```

> Never commit real API keys or tokens to `.env` — add `.env` to `.gitignore`.

### Run

```bash
# Development server
npm run dev

# Production build
npm run build

# Preview production build locally
npm run preview
```

The app starts on `http://localhost:5173`.

---

## Pages Overview

| Route | Page | Description |
|---|---|---|
| `/` | Home | Landing page |
| `/login` | Login | User login |
| `/register` | Register | New account |
| `/home-page` | Main | Dashboard after login |
| `/code-analyzer` | CodeAnalyzer | Submit code for analysis |
| `/manage-output` | OutputAnalysis | View results, export PDF |
| `/analysis-graph` | AnalysisGraph | Chart view of metrics |
| `/history-page` | HistoryPage | Browse analysis history |
| `/manage-rules` | ManageRules | Create and manage rules |
| `/project-management` | ProjectManagement | Manage projects |
| `/about-us` | AboutUs | About the project |
| `/resources` | Resources | Documentation & links |

---

## Available Scripts

| Script | Description |
|---|---|
| `npm run dev` | Start Vite development server |
| `npm run build` | Build for production |
| `npm run preview` | Preview production build |
| `npm run lint` | Run ESLint |
