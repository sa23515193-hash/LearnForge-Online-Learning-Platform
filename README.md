# LearnForge — Coursera-Inspired Learning Platform

Premium orange / charcoal / green online learning platform demo. Includes 22 sample courses, categories/search, student accounts, modules, video lessons, quiz previews, notes, progress tracking, certificate demo, free trials, admin catalog CRUD, and separate backend source.

## Structure
- `frontend/` React + Vite application for GitHub Pages preview
- `backend/` separate Express/MongoDB API source
- `.github/workflows/pages.yml` publishes only the frontend build

## Run frontend locally
```bash
cd frontend
npm install
npm run dev
```
Build: `npm run build`.

## GitHub upload / preview
Upload the whole repository root, so **both `frontend/` and `backend/` are in GitHub**. The included Actions workflow builds `frontend/` and deploys only `frontend/dist` to GitHub Pages. In GitHub go to **Settings → Pages → Build and deployment → Source: GitHub Actions**. The backend remains source code in the repo and is not executed or called by the Pages preview.

## Student demo
Use **Create account** and complete all fields. The browser stores the demo student account, enrollments, progress, and certificates in `localStorage`; it works on the same browser/device only. Do not use real passwords.

## Admin preview
Route: `/#admin-login`
- Username/email: `admin@learnforge.local`
- Password: `LearnForge@Admin2026`

These are hardcoded **demo-only frontend credentials** for preview access, not secure production authentication. Backend admin credentials are configured privately through `backend/.env`. Change the defaults before any real deployment.

## Backend setup
```bash
cd backend
npm install
# Copy .env.example to .env and configure MongoDB + secrets
npm run seed
npm run dev
```
See `backend/README.md` for API endpoints.

## Included features
- 22 courses across Development, Data Science, AI/ML, Design, Marketing, Business, Career and Security
- 3 modules per seeded course, 9 sample lessons and a knowledge check per course
- Search, category and level filters
- Detailed course preview and free-trial labels
- Full student signup fields: name, DOB, email, institute, education, major, password and confirmation
- Student dashboard, course enrollment demo, lesson video player, mark-complete progress
- Quiz interaction, lesson notes, certificate preview with print/save PDF
- Admin course create/edit/delete with module/lesson editor, students/enrollments/payments views
- Responsive layout for desktop/mobile

## Important limitations
- GitHub Pages preview intentionally uses browser-local demo data and does **not** connect to the backend. Browser accounts are not production-secure; never use a real password.
- Demo checkout does not charge money. Real Razorpay checkout needs test keys and a frontend payment integration to be configured.
- Sample video embed URLs and remote Unsplash images are illustrative; replace them with content you own or are licensed to use.
- Demo certificates are not accredited credentials.
- Backend includes email verification and reset endpoints; configure SMTP in `.env` to send emails.
