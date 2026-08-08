---
type: thesis-backlog-tracker
chapter: BAB IV
topic: Alignment BAB IV terhadap Acuan BAB III
source: DRAFT THESIS 10 Juni.docx
created: 2026-06-18
status: active
tags:
  - thesis
  - bab-4
  - backlog
  - dmaic
  - fcr
  - non-fcr
  - control
---

# BAB 4 - Tracker Backlog Perbaikan

## Fungsi Dokumen

Dokumen ini adalah tracker perbaikan BAB IV berdasarkan evaluasi kesesuaian terhadap acuan BAB III. Gunakan ID backlog seperti `B4-04` atau `B4-08` ketika ingin membahas, memperbaiki, atau menandai item sebagai selesai.

## Ringkasan Status

BAB IV saat ini sudah cukup selaras dengan rencana BAB III. Struktur DMAIC sudah benar, kronologi data sudah rapi, dan istilah `ticket/tiket`, `after improvement`, `fixed dev`, `FMEA`, serta `SOP` tidak ditemukan di BAB IV. Sisa backlog terutama berada pada framing istilah, kelengkapan metrik Control, dan landasan penggunaan p-value.

## Prioritas Eksekusi

1. `B4-04` - Analyze terlalu bug-centric.
2. `B4-08` - p-value muncul tanpa landasan metode.
3. `B4-07` - Tabel Control belum menampilkan Non-FCR secara eksplisit.
4. `B4-02` - Alasan pemilihan enam tag perlu dibuat lebih natural.
5. `B4-01`, `B4-03`, `B4-05`, `B4-06`, `B4-09`, `B4-10` - Perapihan framing dan terminologi.

## Task List

- [x] `B4-01` - Rapikan bahasa Define agar tidak terasa masuk ke Analyze.
- [x] `B4-02` - Perkuat alasan pemilihan enam tag prioritas.
- [x] `B4-03` - Jelaskan denominator SLA breach rate.
- [x] `B4-04` - Kurangi framing bug-centric pada Analyze.
- [x] `B4-05` - Ganti istilah `dev escalation` dengan istilah akademik yang lebih netral.
- [x] `B4-06` - Hubungkan tabel Improve dengan root cause dan PDCA secara lebih eksplisit.
- [x] `B4-07` - Tambahkan Non-FCR count/rate pada pembacaan Control.
- [x] `B4-08` - Beri landasan metode untuk p-value atau sederhanakan menjadi indikasi perubahan.
- [x] `B4-09` - Lembutkan bahasa kausal di Control.
- [x] `B4-10` - Pastikan dashboard hanya menjadi alat bantu, bukan inti argumen Control.

## Detail Backlog

### B4-01 - Define Sedikit Bocor ke Analyze

Status: Solved  
Prioritas: Medium  
Fase: Define  
Lokasi: Fase Define, paragraf setelah penjelasan SIPOC dan flowchart.

Masalah:
Kalimat "membedah titik kebocoran operasional secara spesifik" terasa terlalu analitis untuk fase Define. Define sebaiknya fokus pada ruang lingkup, CTQ, alur proses, SIPOC, dan titik keputusan proses.

Arah perbaikan:
Ubah menjadi bahasa pemetaan proses yang lebih netral, misalnya menjelaskan bahwa flowchart digunakan untuk menunjukkan alur inquiry dan titik keputusan apakah inquiry selesai pada kontak pertama atau perlu tindak lanjut.

Acceptance criteria:
- Define tidak membahas root cause.
- Define tidak memakai bahasa "membedah kebocoran" atau analisis penyebab.
- Define tetap menjelaskan CTQ, Non-FCR sebagai defect, SLA breach sebagai dampak, SIPOC, dan flowchart.

### B4-02 - Alasan Pemilihan Enam Tag Perlu Lebih Natural

Status: Solved  
Prioritas: Medium  
Fase: Measure  
Lokasi: Fase Measure, paragraf setelah Gambar 4.2 Pareto.

Masalah:
BAB IV sudah menyebut enam tag menghasilkan 1.794 defect atau 64,42% dari Non-FCR Product 1. Namun alasan "kenapa enam" masih terasa sebagai pembatasan fokus, belum sepenuhnya menjelaskan bahwa jumlah tag dipilih berdasarkan hasil Pareto dan kelayakan pendalaman analisis.

Arah perbaikan:
Jelaskan bahwa enam tag dipilih karena menjadi kelompok kontributor terbesar yang masih layak dianalisis secara mendalam dalam periode penelitian. Hindari kesan bahwa angka enam sudah ditentukan sebelum Pareto.

Acceptance criteria:
- Pemilihan tag dibaca sebagai hasil Measure, bukan keputusan awal.
- Angka 64,42% tetap dipertahankan.
- Tidak ada klaim bahwa enam tag mewakili seluruh Pareto 80%.

### B4-03 - Denominator SLA Breach Rate Belum Eksplisit

Status: Solved  
Prioritas: Medium  
Fase: Measure dan Control  
Lokasi: Narasi sekitar Tabel 4.1 dan Tabel 4.2.

Masalah:
SLA breach dan SLA breach rate sudah muncul, tetapi denominator perhitungannya belum dijelaskan dengan tegas. Pembaca perlu tahu bahwa SLA breach rate dihitung pada ruang lingkup inquiry berjenis issue yang sama.

Arah perbaikan:
Tambahkan satu kalimat pendek yang menjelaskan bahwa SLA breach rate dihitung sebagai jumlah inquiry berjenis issue yang melewati SLA 24 jam dibagi total inquiry berjenis issue pada periode yang sama.

Acceptance criteria:
- Denominator SLA breach jelas.
- SLA breach tetap diposisikan sebagai metrik dampak pendukung.
- Tidak mengubah posisi Non-FCR sebagai defect utama.

### B4-04 - Analyze Terlalu Bug-Centric

Status: Solved  
Prioritas: High  
Fase: Analyze  
Lokasi: Fase Analyze, paragraf pembuka, tabel root cause, dan narasi setelah Fishbone.

Masalah:
Istilah seperti "level bug", "Bug yang dominan", dan banyaknya penggunaan kata "bug" dapat membuat pembaca menangkap bahwa semua akar penyebab Non-FCR adalah bug. Padahal BAB III menuntut root cause berbasis evidence operasional, bukan asumsi bahwa bug adalah penyebab semua Non-FCR.

Arah perbaikan:
Gunakan istilah yang lebih netral seperti "pola issue dominan", "sub-tag dominan", atau "kelompok issue yang dilaporkan". Kata bug tetap boleh digunakan hanya ketika evidence memang menunjukkan perbaikan bug atau masalah teknis.

Acceptance criteria:
- Analyze tidak menyimpulkan semua masalah disebabkan bug.
- Tabel root cause memakai istilah netral.
- Root cause tetap berbasis evidence operasional.
- Fishbone 6M tetap dipertahankan.

### B4-05 - Istilah Dev Escalation Terlalu Internal

Status: Solved  
Prioritas: Medium  
Fase: Analyze dan Improve  
Lokasi: Paragraf data pendukung Analyze dan paragraf evidence Improve.

Masalah:
Istilah `dev escalation` muncul di BAB IV. Istilah ini bisa terasa terlalu internal dan berpotensi membingungkan pembaca tesis.

Arah perbaikan:
Ganti dengan istilah yang lebih akademik dan mudah dipahami, misalnya "catatan eskalasi teknis", "catatan tindak lanjut internal", atau "data tindak lanjut tim pengembang".

Acceptance criteria:
- Istilah internal tetap bisa dilacak sumber datanya.
- Pembaca memahami bahwa data tersebut adalah evidence operasional.
- Narasi tetap konsisten dengan istilah inquiry dan issue.

### B4-06 - Tabel Improve Perlu Lebih Terhubung ke Root Cause dan PDCA

Status: Solved  
Prioritas: Medium  
Fase: Improve  
Lokasi: Fase Improve, tabel bug dilaporkan vs bug diperbaiki dan narasi setelah tabel.

Masalah:
Fase Improve sudah memiliki Plan, Do, Check, dan Act. Namun tabel utama Improve masih lebih terlihat sebagai tabel status perbaikan bug, belum sepenuhnya menunjukkan hubungan langsung antara root cause Analyze, tindakan PDCA, dan tindak lanjut perbaikan.

Arah perbaikan:
Tambahkan penghubung naratif atau sesuaikan tabel agar setiap tag tidak hanya menunjukkan jumlah dilaporkan/diperbaiki, tetapi juga menunjukkan jenis root cause atau fokus tindak lanjut yang berasal dari Analyze.

Acceptance criteria:
- Tabel Improve terbaca sebagai evidence pelaksanaan PDCA.
- Perbaikan terlihat berasal dari hasil Analyze.
- Improve tidak dipakai sebagai bukti akhir keberhasilan; keberhasilan tetap dibaca di Control.

### B4-07 - Control Belum Menampilkan Non-FCR Secara Eksplisit

Status: Solved  
Prioritas: High  
Fase: Control  
Lokasi: Tabel 4.2 Kinerja Product 1 Baseline, Implementasi PDCA, dan Evaluasi Awal.

Masalah:
Tabel 4.2 sudah menampilkan FCR, DPMO, SLA breach, dan rata-rata inquiry per bulan. Namun checklist BAB III meminta Control membaca FCR, Non-FCR, DPMO, dan SLA breach. Non-FCR memang tersirat melalui DPMO, tetapi sebaiknya tetap ditampilkan eksplisit.

Arah perbaikan:
Tambahkan kolom Non-FCR atau Non-FCR rate pada Tabel 4.2, atau jelaskan Non-FCR secara langsung dalam narasi setelah tabel.

Acceptance criteria:
- Control membaca FCR, Non-FCR, DPMO, dan SLA breach.
- Non-FCR tidak hanya tersirat melalui DPMO.
- Pembaca bisa melihat hubungan FCR turun/naik dengan defect count/rate.

### B4-08 - P-Value Muncul Tanpa Landasan Metode

Status: Solved  
Prioritas: High  
Fase: Control  
Lokasi: Tabel evaluasi per tag pada Fase Control.

Masalah:
Tabel evaluasi per tag memakai p-value dan interpretasi signifikan, tetapi BAB III tidak menjelaskan metode uji statistik, jenis uji, asumsi, atau denominator yang digunakan. Ini bisa menjadi pertanyaan penguji.

Arah perbaikan:
Ada dua opsi:
1. Tambahkan penjelasan metode uji statistik secara singkat sebelum tabel.
2. Hilangkan p-value dan gunakan bahasa "indikasi perubahan", "membaik lebih kuat", atau "membaik moderat" berdasarkan delta FCR dan evidence Improve.

Acceptance criteria:
- Jika p-value dipertahankan, metode uji dan basis datanya jelas.
- Jika p-value dihapus, bahasa klaim menjadi lebih hati-hati.
- Control tetap mampu menjelaskan bahwa FINANCE dan MASTER menunjukkan evidence perubahan paling kuat.

### B4-09 - Bahasa Kausal di Control Perlu Dilembutkan

Status: Solved  
Prioritas: Medium  
Fase: Control  
Lokasi: Paragraf pembuka Fase Control dan paragraf penutup BAB IV.

Masalah:
Masih ada frasa seperti "sebelum improvement" dan "hasil improvement". Frasa ini tidak salah total, tetapi dapat terdengar terlalu kausal atau terlalu absolut karena Jan-Apr 2026 adalah periode implementasi PDCA dan Jan-May 2026 adalah evaluasi awal.

Arah perbaikan:
Gunakan istilah "baseline 2025", "periode implementasi PDCA", "evaluasi awal 2026", dan "indikasi perbaikan" agar klaim tetap hati-hati.

Acceptance criteria:
- Control tidak mengklaim kausalitas mutlak.
- Jan-Apr 2026 tetap disebut sebagai periode implementasi PDCA.
- Jan-May 2026 tetap disebut sebagai evaluasi awal.

### B4-10 - Dashboard Jangan Menjadi Inti Argumen Control

Status: Solved  
Prioritas: Low  
Fase: Control  
Lokasi: Paragraf setelah Tabel 4.4 Rencana Pengendalian Fase Control.

Masalah:
Dashboard monitoring muncul di akhir Control. Ini masih aman, tetapi perlu dijaga agar dashboard hanya dibaca sebagai alat bantu monitoring, bukan inti dari fase Control. Inti Control adalah pemantauan metrik dan respons terhadap deviasi.

Arah perbaikan:
Pastikan narasi menekankan bahwa dashboard hanya membantu menampilkan FCR, Non-FCR, DPMO, SLA breach, dan top issue tag secara berkala. Mekanisme utamanya tetap evaluasi metrik dan tindak lanjut ketika ada deviasi.

Acceptance criteria:
- Dashboard diposisikan sebagai media monitoring.
- Inti Control tetap pada metrik dan response plan.
- Tidak ada kesan bahwa Control selesai hanya karena ada dashboard.

## Definition of Done

BAB IV dapat dianggap selaras dengan acuan BAB III jika:

- Define tidak membahas root cause.
- Measure hanya membahas baseline, stratifikasi, dan Pareto.
- Analyze menjadi titik pertama munculnya akar penyebab.
- Improve menjadi titik pertama munculnya evidence tindakan perbaikan.
- Control membaca FCR, Non-FCR, DPMO, SLA breach, dan pergerakan tag prioritas.
- Kronologi konsisten: 2025 sebagai baseline, Jan-Apr 2026 sebagai implementasi PDCA, Jan-May 2026 sebagai evaluasi awal.
- Bahasa kausal tetap hati-hati dan berbasis evidence.
- Tidak ada istilah `ticket/tiket` di narasi tesis.

## Koneksi

- Acuan: [[BAB 3 - Summary Metodologi Penelitian]]
- Terkait: [[Relasi Metrik BAB 1-3]]
- Terkait: [[BAB 4 - Summary Hasil Penelitian]]
