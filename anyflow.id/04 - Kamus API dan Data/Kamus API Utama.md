# Kamus API Utama

Catatan ini adalah kamus cepat endpoint API.

## Workflow

Frontend: `workflowApi`

- `GET /api/workflows`: daftar workflow.
- `GET /api/workflows/:id`: detail workflow.
- `POST /api/workflows`: buat workflow.
- `PUT /api/workflows/:id`: update workflow.
- `DELETE /api/workflows/:id`: hapus workflow.
- `PATCH /api/workflows/:id/archive`: archive.
- `PATCH /api/workflows/:id/unarchive`: unarchive.
- `POST /api/workflows/:id/duplicate`: duplicate.
- `POST /api/workflows/:id/rename-status`: rename status dan migrasi data terkait.
- `POST /api/workflows/:id/rename-field`: rename field dan migrasi data terkait.
- `POST /api/workflows/:id/delete-field`: delete field dan cleanup data terkait.

## Ticket

Frontend: `ticketApi`

- `GET /api/tickets`: daftar ticket dengan filter.
- `GET /api/tickets/:id`: detail ticket.
- `POST /api/tickets`: buat ticket.
- `PUT /api/tickets/:id`: update ticket.
- `DELETE /api/tickets/:id`: hapus ticket.
- `POST /api/tickets/batch`: ambil banyak ticket berdasarkan ID.
- `POST /api/tickets/bulk-create`: import/buat banyak ticket.
- `POST /api/tickets/bulk-delete`: hapus banyak ticket.
- `POST /api/tickets/bulk-migrate`: pindahkan banyak ticket ke status tertentu.
- `GET /api/tickets/:id/history`: history ticket.
- `POST /api/tickets/:id/comments`: tambah komentar.
- `PUT /api/tickets/:id/comments/:commentId`: edit komentar.
- `DELETE /api/tickets/:id/comments/:commentId`: hapus komentar.
- `POST /api/tickets/wip-limit/check`: cek WIP limit.
- `GET /api/tickets/grouped/:workflowId`: daftar grouping parent.
- `POST /api/tickets/batch-subtask-progress`: progress child/subtask.
- `GET /api/tickets/:id/lineage`: garis keturunan parent-child.

## Automation

Frontend: `automationApi`

- `GET /api/automations?workflowId=...`: daftar automation.
- `GET /api/automations/:id`: detail automation.
- `POST /api/automations`: buat automation.
- `PUT /api/automations/:id`: update automation.
- `DELETE /api/automations/:id`: hapus automation.
- `POST /api/automations/:id/duplicate`: duplicate.
- `GET /api/automations/:id/logs`: log automation.
- `POST /api/automations/:id/retry/:logId`: retry log.
- `POST /api/automations/:id/trigger_manual`: trigger manual dari ticket.
- `GET /api/automations/logs/global`: log global untuk super admin.
- `GET /api/automations/stats`: statistik automation.

## Dashboard

Frontend: `dashboardApi`

- `GET /api/dashboard/:workflowId/stats`: KPI statistik.
- `GET /api/dashboard/:workflowId/trends`: trend waktu.
- `GET /api/dashboard/:workflowId/funnel`: funnel status.
- `GET /api/dashboard/:workflowId/workload`: workload user/status.
- `POST /api/dashboard/:workflowId/pivot`: pivot custom.
- `POST /api/dashboard/:workflowId/kpi`: KPI custom.

## Public

Frontend: `publicFormApi`

- `GET /api/public/forms/:slug`: ambil konfigurasi public form.
- `POST /api/public/forms/:slug/submit`: submit public form.
- `GET /api/public/forms/:slug/options/:fieldId`: opsi field publik.
- `GET /api/public/tracker/track/:token`: lacak ticket publik.

