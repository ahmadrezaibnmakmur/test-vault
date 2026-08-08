# Struktur Folder Project

Ini peta folder yang paling relevan untuk memahami sistem.

## Root

Root adalah area frontend dan konfigurasi project.

- `App.tsx`: pusat aplikasi frontend.
- `index.tsx`: entry React.
- `index.html`: HTML root Vite.
- `services/api.ts`: semua pemanggilan API frontend.
- `components/`: komponen umum/lama.
- `contexts/`: provider global seperti socket, theme, toast.
- `src/features/`: fitur frontend yang lebih modular.
- `src/utils/` dan `utils/`: helper logic.
- `types.ts`: tipe data utama frontend.
- `vite.config.ts`: konfigurasi Vite.
- `package.json`: script dan dependency frontend/root.

## src/features

- `tracker/`: halaman tracker.
- `workflowBuilder/`: builder workflow.
- `dashboard/`: dashboard standard dan custom.
- `publicPortal/`: public form dan public tracker.
- `navigation/`: sidebar dan navigasi.
- `labs/`: fitur lab/dev/test.

## server

Backend berada di folder `server`.

- `server/src/app.ts`: memasang Express app dan route API.
- `server/src/index.ts`: menyalakan server dan worker.
- `server/src/routes/`: semua endpoint API.
- `server/src/services/`: service backend seperti dashboard, storage, notification, SLA worker, report worker.
- `server/src/utils/`: helper backend untuk calculation, automation, SLA, validation, document generation.
- `server/src/middleware/`: auth dan security middleware.
- `server/src/socket.ts`: Socket.IO realtime.
- `server/prisma/schema.prisma`: struktur database.
- `server/package.json`: script dan dependency backend.

## docs

Folder `docs/` berisi dokumentasi teknis yang sudah ada, misalnya fitur tracker, dashboard, API, security audit, public form, dan lainnya. Vault ini lebih fokus menjelaskan logika dengan bahasa manusia, sedangkan `docs/` lama cenderung lebih teknis.

