# Kamus Data Utama

## Workflow

Workflow adalah cetakan proses.

Analogi: kalau ticket adalah "form pengajuan yang sudah diisi", workflow adalah "template form dan aturan prosesnya".

Workflow menyimpan:

- status;
- field;
- form setting;
- tracker setting;
- permission;
- SLA;
- automation;
- dashboard config;
- public form setting.

## Ticket

Ticket adalah record nyata di dalam workflow.

Satu ticket menyimpan:

- workflow mana yang memilikinya;
- status sekarang;
- judul/search text;
- assignee;
- priority;
- custom field di `customData`;
- parent ticket jika ada hierarchy/grouping;
- SLA deadline;
- history dan komentar.

## Field dinamis

Field dinamis didefinisikan di `Workflow.fields`.

Saat ticket dibuat, nilai field dinamis disimpan terutama di `Ticket.customData`.

Beberapa field juga disalin ke kolom khusus seperti `custom_text_1` atau `custom_select_1` untuk performa pencarian/filter.

## Status dan transition

Status disimpan di workflow sebagai daftar. Aturan perpindahan status disimpan di `statusTransitions`.

Contoh konsep:

- Draft boleh ke Review.
- Review boleh ke Approved atau Rejected.
- Approved tidak boleh kembali ke Draft, kecuali aturan mengizinkan.

Saat update ticket, backend perlu mengecek apakah perpindahan status valid dan apakah ada aturan tambahan.

## SLA

SLA memakai:

- status ticket;
- waktu masuk status (`statusEnteredAt`);
- konfigurasi SLA di workflow/status;
- working hours config.

Backend menghitung `slaDeadline` dan menyimpan log di `TicketSLALog`.

## Automation

Automation adalah aturan "kalau terjadi X, lakukan Y".

Trigger bisa:

- ticket dibuat;
- status berubah;
- tombol manual ditekan.

Action bisa berupa webhook, generate dokumen, minta lokasi, chaining automation, atau aksi lain sesuai konfigurasi.

## Notification

Notification muncul terutama dari mention/komentar dan event lain yang ditujukan ke user tertentu.

Frontend mendengarkan notification lewat API dan Socket.IO.

