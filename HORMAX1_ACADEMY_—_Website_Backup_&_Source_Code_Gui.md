# HORMAX1 ACADEMY — Website Backup & Source Code Guide

## Ujeeddo

Dukumentigan wuxuu sharxayaa backup-ka dhammeystiran ee website-ka **HORMAX1 ACADEMY**. Waxaa la socda archive ZIP ah oo ka kooban source code-ka, database schema iyo migrations, frontend pages, backend API, lesson content, quiz HTML, iyo configuration files-ka mashruuca.

## Waxa ku jira website-ka

Website-ku waa learning platform Somali-first ah oo leh landing page, course catalog, student learning flow, payment proof workflow, certificate generation, certificate verification, admin dashboard, course management, student dashboard, iyo AI for Business & Productivity course.

### Frontend

Frontend-ku wuxuu ku jiraa `client/`. Waxaa ka mid ah:

- `client/src/App.tsx` — routes-ka website-ka.
- `client/src/pages/Home.tsx` — homepage, course catalog, student learning flow, quiz iyo certificate success.
- `client/src/pages/AIBusinessQuiz.tsx` — bogga AI for Business & Productivity oo cashar iyo quiz isku xira.
- `client/src/pages/Admin.tsx` — admin dashboard-ka content management.
- `client/src/pages/Payments.tsx` — student payment proof page.
- `client/src/pages/PaymentsAdmin.tsx` — admin payment review.
- `client/src/pages/PricingAdmin.tsx` — course pricing management.
- `client/src/pages/StudentDashboard.tsx` — student courses, payments, notifications iyo certificates.
- `client/src/pages/Verify.tsx` — public certificate verification.
- `client/src/content/AI-for-Business-Productivity-Cashar.md` — casharka AI ee Somali-ga ah.
- `client/public/ai-business-quiz.html` — interactive quiz-kii asalka ahaa, oo leh 20 su'aalood iyo certificate logic.

### Backend

Backend-ku wuxuu ku jiraa `server/`:

- `server/routers.ts` — tRPC API procedures ee auth, learning, courses, modules, lessons, quizzes, payments, certificates iyo verification.
- `server/db.ts` — database helpers.
- `server/email.ts` — Resend/email integration diyaar u ah marka domain iyo API key la helo.
- `server/storage.ts` — object storage helper.
- `server/_core/` — authentication, environment, tRPC, OAuth iyo framework infrastructure.

### Database

Database schema-ku wuxuu ku jiraa `drizzle/schema.ts`, migrations-kuna waxay ku jiraan `drizzle/`. Database-ku wuxuu taageeraa:

- Users iyo roles: student, admin, super_admin.
- Courses, modules iyo lessons.
- Quiz questions iyo final exams.
- Student progress iyo enrollments.
- Certificates iyo public verification.
- Payment methods, payment submissions iyo notifications.

### AI for Business & Productivity

Course-kan waxaa loo diyaariyey:

- 6 modules.
- 19 lessons Somali-first ah.
- 1 final exam.
- 20 multiple-choice questions.
- Passing score 70%.
- 3 exam attempts.
- Certificate eligibility kadib guul.

Modules-ku waa:

1. Fahamka AI iyo fursadaha ganacsiga.
2. AI ee marketing iyo customer service.
3. AI tools-ka ugu muhiimsan.
4. Prompts iyo workflows wax-ku-ool ah.
5. Data, productivity iyo Responsible AI.
6. Capstone project iyo final exam.

## Payment information currently configured

- Hormuud EVC Plus: `*799*36254225*AMOUNT#`
- eDahab: `*712*628780258*AMOUNT#`
- WhatsApp support: `+252 61 8780258`

## Email status

Certificate email code-ku wuu diyaar yahay, laakiin automatic email delivery wuxuu u baahan yahay:

1. Domain aad leedahay oo la verify-gareeyey.
2. Resend API key ama SMTP credentials.
3. Sender address, tusaale `certificates@yourdomain.com`.

Email-ka tijaabada ah ee hore loo qorsheeyey waa `maxmadow1995@gmail.com`, laakiin lama hawlgelin ilaa domain iyo sender la helo.

## Sida loo soo celiyo project-ka

1. Soo dejiso ZIP archive-ka source code-ka.
2. Ku extract garee server ama computer leh Node.js 22, pnpm iyo MySQL/TiDB.
3. Samee environment variables-ka server-ka: `DATABASE_URL`, `JWT_SECRET`, OAuth variables iyo built-in API variables.
4. Orod `pnpm install`.
5. Orod `pnpm check` si TypeScript loo hubiyo.
6. Orod `pnpm build` si production build loo sameeyo.
7. Database migrations-ka ku dabaq database-ka saxda ah adigoo raacaya `drizzle/` files iyo project deployment workflow.
8. Ku xiro domain-ka iyo email provider-ka haddii certificate email loo baahan yahay.

## Important security note

Archive-kan wuxuu ka kooban yahay source code iyo schema, laakiin **ma aha in secrets ama API keys lagu daro**. Ha wadaagin `.env`, database password, JWT secret, OAuth secret, Resend key, ama credentials meel public ah. Haddii secrets ay ku jiraan folder-kaaga local-ka, ka saar archive-ka ka hor intaadan cloud ama qof kale u dirin.

## Validation la sameeyey

- TypeScript check: passed.
- Production build: passed.
- Backend test suite: passed.
- AI course database counts: 6 modules, 19 lessons, 1 quiz, 20 questions.
- AI course page visual QA: passed.
- Final checkpoint: `66a29b24`.

## Backup contents

Archive-ka source code-ka waxaa loogu talagalay in lagu hayo meel ammaan ah sida Google Drive, Dropbox, external hard drive, ama private Git repository. PDF-kan waa documentation; ZIP-ku waa source-ka dhabta ah.

**Project:** HORMAX1 ACADEMY  
**Project path:** `/home/ubuntu/learnsoo`

---

*Backup document prepared on 12 September 2026.*

## Quick links after deployment

- Homepage: `/`
- AI course: `/ai-business-quiz`
- Certificate verification: `/verify`
- Student dashboard: `/dashboard`
- Admin dashboard: `/admin`
- Payment page: `/payments`
- Admin payments: `/admin/payments`
- Admin pricing: `/admin/pricing`

## Limitations to remember

The live deployment, database connection, OAuth configuration, and email provider are environment-specific. The ZIP preserves the application source and migrations, but it does not replace a separate export of production database records or a secure copy of environment secrets.
