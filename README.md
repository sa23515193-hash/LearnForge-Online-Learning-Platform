# LearnForge — Online Learning Platform 🎓

LearnForge is a Coursera-inspired online learning platform designed to make digital education accessible through an interactive and modern learning experience.

The project includes a responsive React frontend, a student learning dashboard, course browsing, learning progress tracking, quizzes, demo certificates, an administrative dashboard, and a separate Node.js/Express backend API.

The frontend can be published independently on GitHub Pages, while the backend source code remains in the same repository for local development and future deployment.

## ✨ Features

### 🎓 Student Features

* Student registration with detailed profile information.
* Full name, date of birth, email, password, and password confirmation fields.
* Institute or university information.
* Current education level and major.
* Student login and dashboard.
* Browse and search available courses.
* Filter courses by category and difficulty level.
* View course details, instructors, ratings, and lesson content.
* Enroll in courses using the frontend demo experience.
* Explore course modules and lessons.
* Watch illustrative video lessons.
* Mark lessons as completed.
* Track learning progress.
* Take sample quizzes.
* Save learning notes.
* View demo course completion certificates.
* Responsive layout for desktop, tablet, and mobile.

### 📚 Course Catalog

LearnForge includes 22 sample courses across multiple learning categories, including:

* Full Stack MERN Development
* React and TypeScript
* JavaScript
* Node.js API Development
* Advanced CSS and Responsive Design
* Python for Data Analysis
* SQL and Database Design
* Power BI
* Machine Learning
* Generative AI
* UI/UX Design
* Graphic Design
* Digital Marketing
* Search Engine Optimization
* Laravel and PHP
* C# and .NET
* Content Writing
* Freelancing
* Leadership and Communication
* Cybersecurity
* Productivity and Project Management
* Cloud Computing

Course content, instructors, ratings, and video references are sample data for demonstration.

### 🛠️ Admin Dashboard

The frontend demo includes an administrative interface for:

* Viewing dashboard statistics.
* Creating courses.
* Editing course information.
* Managing modules and lessons.
* Deleting sample courses.
* Viewing demo student records.
* Viewing enrollments.
* Viewing demo payment records.
* Resetting demonstration data.

**Important:** Frontend admin authentication is for demonstration only. It is not suitable for protecting a production application.

### 🔧 Backend API

The separate backend source includes:

* Node.js and Express.
* MongoDB and Mongoose.
* User authentication utilities.
* JWT-based authentication.
* Password hashing.
* Email verification endpoints.
* Password reset endpoints.
* Course management endpoints.
* Enrollment and progress endpoints.
* Admin routes.
* Razorpay payment order and signature-verification endpoints.
* Environment-based configuration.

Some backend functionality requires configuration and integration before it can be used in a production application.

## 🧰 Technology Stack

### Frontend

* React
* Vite
* JavaScript
* CSS
* Lucide React icons
* Browser localStorage for demonstration data

### Backend

* Node.js
* Express.js
* MongoDB
* Mongoose
* JSON Web Tokens (JWT)
* bcrypt
* Nodemailer
* Razorpay SDK
* dotenv

### Deployment

* GitHub
* GitHub Pages
* GitHub Actions

## 📁 Project Structure

```text
LearnForge-Online-Learning-Platform/
│
├── .github/
│   └── workflows/
│       └── pages.yml
│
├── frontend/
│   ├── index.html
│   ├── package.json
│   ├── vite.config.js
│   └── src/
│
├── backend/
│   ├── package.json
│   ├── .env.example
│   └── src/
│
├── .gitignore
└── README.md
```

## 🚀 Run the Frontend Locally

### Prerequisites

Install Node.js and npm on your computer.

### Step 1: Open the project folder

Open a terminal in the project root directory.

### Step 2: Navigate to the frontend

```bash
cd frontend
```

### Step 3: Install dependencies

```bash
npm install
```

### Step 4: Start the development server

```bash
npm run dev
```

Open the local address displayed in your terminal, usually:

```text
http://localhost:5173
```

### Step 5: Create a production build

```bash
npm run build
```

Vite generates the production frontend files in:

```text
frontend/dist/
```

## 🔐 Demo Administrator Login

The frontend demo provides a separate admin login screen.

**Demo route:**

```text
/#admin-login
```

**Demo email:**

```text
admin@learnforge.local
```

**Demo password:**

```text
LearnForge@Admin2026
```

These credentials are hardcoded for demonstration purposes. They are public within the frontend source and must never be used as production administrator credentials.

Do not enter real or sensitive information into the demonstration application.

## 🖥️ Run the Backend Locally

### Prerequisites

* Node.js and npm
* MongoDB connection string
* A configured environment file

### Step 1: Open a separate terminal

From the project root:

```bash
cd backend
```

### Step 2: Install backend dependencies

```bash
npm install
```

### Step 3: Configure environment variables

Copy `.env.example` to a new file named `.env`.

On Windows PowerShell:

```powershell
Copy-Item .env.example .env
```

Open `.env` and configure the required values, including:

* MongoDB connection string.
* A strong JWT secret.
* Frontend origin.
* Private administrator credentials.
* SMTP credentials if email functionality is required.
* Razorpay test credentials if payment testing is required.

Never commit your `.env` file or private API keys to GitHub.

### Step 4: Seed sample courses

```bash
npm run seed
```

This command requires a working MongoDB connection and the appropriate environment configuration.

### Step 5: Start the backend

```bash
npm run dev
```

The backend port and additional setup instructions are defined in the backend configuration and README.

## 🌐 Publish the Frontend on GitHub Pages

This repository includes a GitHub Actions workflow at:

```text
.github/workflows/pages.yml
```

The workflow builds and publishes only the frontend. It does not deploy or run the backend.

### Step 1: Upload the project

Upload the complete project to a public GitHub repository.

Make sure these folders are included:

* `frontend`
* `backend`
* `.github/workflows`

### Step 2: Enable GitHub Pages

1. Open your GitHub repository.
2. Click **Settings**.
3. Open **Pages**.
4. Under the build and deployment settings, select **GitHub Actions** as the source.

### Step 3: Run the deployment workflow

1. Open the **Actions** tab.
2. Select the Pages deployment workflow.
3. Wait for the build and deployment to finish.
4. Open the published website link shown in the deployment or Pages section.

Future pushes to the configured branch will trigger the workflow automatically.

**Important:** The first deployment can take a few minutes. If the workflow fails, open the Actions run and inspect the build logs.

## ⚠️ Demo Limitations

This project is a learning and demonstration project. Review these limitations before using it for real users.

* GitHub Pages hosts only static frontend files; it cannot run the Express backend.
* Frontend demonstration data is stored in browser localStorage.
* LocalStorage data belongs to the current browser and device.
* Frontend demo authentication is not production-secure.
* The frontend demo does not automatically connect to the backend API.
* Backend deployment and frontend API integration require additional configuration.
* Email verification and password-reset backend routes require suitable frontend integration and service configuration.
* Real Razorpay checkout is not fully connected to the frontend demo.
* Payment endpoints require secure server-side configuration and appropriate testing.
* Demo course videos and course content are illustrative.
* Demo completion certificates are not accredited qualifications.
* Production deployment requires security reviews, validation, error handling, and appropriate privacy protections.

## 🔒 Security Notes

* Never publish real passwords, JWT secrets, database credentials, SMTP passwords, or payment keys.
* Keep private configuration in environment variables.
* Use HTTPS in production.
* Enforce server-side authorization for administrative actions.
* Validate and sanitize user input.
* Use secure authentication and session-handling practices.
* Verify payment results on the server.
* Review email verification, password-reset, and account-recovery flows before launch.

## 🎯 Project Goals

LearnForge demonstrates how an online learning interface can be structured around student registration, course discovery, lesson navigation, progress tracking, quizzes, certificates, and administrative course management.

It also provides a starting point for connecting a React frontend to a Node.js, Express, and MongoDB backend.

## 🔮 Future Improvements

* Connect the frontend to the backend API.
* Implement secure production authentication.
* Add persistent database-backed learning progress.
* Complete Razorpay checkout integration.
* Add course reviews and ratings.
* Add instructor profiles and course creation tools.
* Add video hosting and lesson access controls.
* Implement email verification and password recovery in the UI.
* Add automated tests.
* Improve accessibility and localization.
* Add analytics and reporting.

## 👩‍💻 Author

**Sawaira Ijaz**

Computer Science Student | Web Developer

GitHub: https://github.com/sa23515193-hash

LinkedIn: https://www.linkedin.com/in/sawaira-ijaz/

Portfolio: https://sa23515193-hash.github.io/MY-CV-portfolio/

## 📄 License

No license has been added yet. Unless a license is added, standard copyright restrictions apply.
