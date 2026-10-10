# LearnForge Backend API

Express + MongoDB backend, kept separate from the GitHub Pages preview.

## Run locally
1. Install Node.js LTS and MongoDB local or Atlas.
2. In this folder run `npm install`.
3. Copy `.env.example` to `.env`; update `MONGO_URI`, `JWT_SECRET`, admin credentials.
4. Run `npm run seed`, then `npm run dev`. API default: `http://localhost:5000`. Health: `/api/health`.

## Endpoints
- `POST /api/auth/register`, `POST /api/auth/login`, `GET /api/auth/verify-email/:token`
- `POST /api/auth/forgot-password`, `POST /api/auth/reset-password/:token`
- `GET /api/courses`, `GET /api/courses/:id`; admin course CRUD `POST/PUT/DELETE /api/courses`
- `GET /api/enrollments/mine`, `POST /api/enrollments/trial/:courseId`, `PATCH /api/enrollments/:id/progress`
- `POST /api/payments/create-order`, `POST /api/payments/verify`
- `POST /api/admin/login`, `GET /api/admin/users`, `GET /api/admin/enrollments`

Without SMTP configuration, email messages are logged to the backend console. Razorpay needs test keys in `.env`. Never commit `.env`.
