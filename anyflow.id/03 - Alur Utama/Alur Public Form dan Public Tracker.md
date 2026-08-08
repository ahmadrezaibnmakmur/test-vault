# Alur Public Form dan Public Tracker

Ada dua halaman publik utama:

- `/form/:slug`: form publik untuk submit ticket.
- `/track/:token`: halaman publik untuk melacak ticket.

Halaman ini berbeda dari halaman internal karena tidak selalu butuh login.

## Public Form

File frontend:

- `src/features/publicPortal/components/PublicForm.tsx`

API frontend:

- `publicFormApi.getBySlug(slug)`
- `publicFormApi.submit(slug, data)`
- `publicFormApi.getOptions(slug, fieldId, query)`

Backend:

- `GET /api/public/forms/:slug`
- `POST /api/public/forms/:slug/submit`
- `GET /api/public/forms/:slug/options/:fieldId`

Alur:

```mermaid
sequenceDiagram
  participant Visitor
  participant PublicForm
  participant Backend as /api/public/forms/:slug
  participant DB as Database
  Visitor->>PublicForm: buka link form
  PublicForm->>Backend: ambil konfigurasi form
  Backend-->>PublicForm: workflow + field publik
  Visitor->>PublicForm: submit
  PublicForm->>Backend: submit form
  Backend->>DB: buat ticket
  Backend-->>PublicForm: sukses + tracking info
```

## Public Tracker

File frontend:

- `src/features/publicPortal/components/PublicTicketTracker.tsx`

Backend:

- `GET /api/public/tracker/track/:token`

Public tracker memakai `trackingToken` pada ticket, bukan token login user.

Tujuannya supaya orang luar bisa melihat status ticket tertentu tanpa akses ke seluruh aplikasi internal.

