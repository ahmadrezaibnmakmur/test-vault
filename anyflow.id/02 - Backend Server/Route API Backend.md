# Route API Backend

Route API adalah pintu masuk request ke backend. Semua dipasang di `server/src/app.ts`.

## Peta route utama

| Prefix API | File backend | Fungsi manusiawi |
|---|---|---|
| `/api/auth` | `routes/auth.ts` | Login, Google callback, cek user aktif |
| `/api/workflows` | `routes/workflows.ts` | CRUD workflow, status, field, archive, duplicate |
| `/api/tickets` | `routes/tickets.ts` | CRUD ticket, filter tracker, history, komentar, bulk action |
| `/api/roles` | `routes/roles.ts` | Role user |
| `/api/users` | `routes/users.ts` | User management |
| `/api/departments` | `routes/departments.ts` | Department |
| `/api/master-tables` | `routes/masterTableRoutes.ts` | Master data table |
| `/api/master-table-folders` | `routes/masterTableFolderRoutes.ts` | Folder master data |
| `/api/webhooks` | `routes/webhooks.ts` | Webhook integration |
| `/api/ai` | `routes/ai.ts` | Fitur AI |
| `/api/reports` | `routes/reports.ts` | Report/export |
| `/api/automations` | `routes/automations.ts` | Automation dan log |
| `/api/dashboard` | `routes/dashboard.ts` | Statistik dashboard |
| `/api/api-keys` | `routes/apiKeys.ts` | API key external |
| `/api/storage` | `routes/storage.ts` | Upload/file storage |
| `/api/public` | `routes/publicRoutes.ts` | Public form |
| `/api/public/tracker` | `routes/publicTracker.ts` | Public tracking ticket |
| `/api/notifications` | `routes/notifications.ts` | Notification |
| `/api/custom-dashboards` | `routes/customDashboardRoutes.ts` | Dashboard custom |
| `/api/document-templates` | `routes/documentTemplates.ts` | Template dokumen |
| `/api/calculation-rules` | `routes/calculationRules.ts` | Formula/kalkulasi |
| `/api/system-settings` | `routes/systemSettings.ts` | Setting global, branding |
| `/api/system` | `routes/systemDiagnostics.ts` | Diagnostic sistem |
| `/api/v2` | `api-v2/index.ts` | API ticket versi baru |

## Route yang paling sering terkait tracker

Tracker paling banyak memakai:

- `GET /api/workflows`: mengambil daftar workflow.
- `GET /api/tickets`: mengambil ticket berdasarkan workflow, status, search, filter, pagination, parent.
- `GET /api/tickets/:id`: mengambil detail satu ticket.
- `POST /api/tickets`: membuat ticket.
- `PUT /api/tickets/:id`: update ticket.
- `DELETE /api/tickets/:id`: hapus ticket.
- `GET /api/tickets/:id/history`: history ticket.
- `POST /api/tickets/:id/comments`: komentar.
- `POST /api/tickets/wip-limit/check`: cek batas WIP.
- `POST /api/tickets/batch`: ambil banyak ticket sekaligus.
- `POST /api/tickets/batch-resolve`: resolve shortId ke data singkat.
- `GET /api/tickets/grouped/:workflowId`: group ticket berdasarkan parent.
- `POST /api/tickets/batch-subtask-progress`: progress subtask.

