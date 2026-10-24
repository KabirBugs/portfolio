# 3DaySolve

3DaySolve is a responsive marketplace experience for focused student-to-business projects. The current workspace contains a dependency-free browser prototype so it can be previewed immediately without installing a framework or package manager.

## Run locally

From PowerShell:

```powershell
powershell -NoProfile -ExecutionPolicy Bypass -File .\serve.ps1
```

Then open <http://localhost:4173/>.

## Included now

- Premium responsive landing page with branded motion, reduced-motion support, mobile navigation, scroll reveals, and loading state.
- Explore Projects board with search, category filtering, sorting, project detail pages, save/share actions, and project reference numbers.
- Student and business registration flows with client-side validation and local dashboard routing.
- Project submission and student application flows with duplicate-application protection.
- Contact, feedback, and newsletter forms with local persistence and reference numbers.
- Student, business, and local admin overview surfaces.
- Centralized 15% commission calculation with the required ₹500 / ₹1,000 / ₹2,000 / ₹5,000 / ₹10,000 examples on the commission page.
- Privacy, terms, about, and commission pages that avoid claiming payment processing or verified external delivery.

## Important production configuration

This empty starter workspace did not contain an existing backend, database, auth provider, Google Form URLs, field-entry IDs, or deployment configuration. The browser prototype stores records in `localStorage` so the flows can be tried without pretending that a production database or external delivery exists.

Before launch, connect:

1. A server-side database for students, businesses, projects, applications, saved projects, status history, contact, feedback, newsletter, and delivery logs.
2. Secure authentication and server-side role-based access control for student, business, and administrator roles.
3. Server-side validation, rate limiting, audit logging, and authorization checks.
4. A verified Google Forms direct-response endpoint or Google Apps Script endpoint for each destination.
5. The real URLs and verified field mappings in `google-forms.config.example.json` (copy into a private server configuration; do not expose secrets in frontend code).
6. A real payment provider only if payment collection or payouts are required. The UI currently shows calculated commission only.

No Google Form submission is claimed until the real destinations and field mappings are supplied and tested.
