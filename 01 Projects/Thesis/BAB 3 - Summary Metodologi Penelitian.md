---
type: thesis-summary
chapter: BAB III
topic: Metodologi Penelitian
source: DRAFT THESIS 10 Juni.docx
created: 2026-06-16
tags:
  - thesis
  - bab-3
  - methodology
  - dmaic
  - pdca
  - fcr
  - dpmo
---

# BAB 3 - Summary Metodologi Penelitian

## Inti Satu Kalimat

BAB III menjelaskan bagaimana penelitian dijalankan: data layanan pelanggan digunakan untuk menghitung baseline FCR/Non-FCR/DPMO/SLA breach, memilih area prioritas berbasis Pareto, menganalisis root cause dengan Fishbone 6M, menjalankan Improve berbasis PDCA, lalu mengevaluasi perubahan kinerja secara hati-hati melalui Control.

## Memory Hook

Baseline 2025 -> stratifikasi dan Pareto -> root cause 6M -> PDCA Jan-Apr 2026 -> evaluasi awal Jan-May 2026 -> dashboard dan standardisasi.

## Peran BAB III dalam Riset

BAB III adalah blueprint penelitian. Jika BAB I menjelaskan mengapa FCR penting dan BAB II menjelaskan mengapa masalah tersebut sah dibaca dengan Lean Six Sigma, maka BAB III menjelaskan cara riset dijalankan secara operasional.

Fungsi terpenting BAB III adalah memastikan pembaca paham bahwa hasil BAB IV tidak muncul tiba-tiba. Pemilihan prioritas, root cause, improvement, dan evaluasi semuanya harus terlihat sebagai konsekuensi dari desain metode DMAIC.

## Storyline BAB III

BAB III dimulai dengan menetapkan objek penelitian: proses layanan pelanggan pada perusahaan SaaS, khususnya penyelesaian Customer Inquiries melalui kanal chat. FCR dipilih sebagai indikator utama karena menunjukkan kemampuan proses menyelesaikan inquiry pada kontak pertama.

Kegagalan menyelesaikan inquiry pada kontak pertama diperlakukan sebagai Non-FCR atau defect. Setiap customer inquiry diperlakukan sebagai satu unit dengan satu peluang defect. Dengan logika ini, DPMO Non-FCR dapat digunakan untuk membaca kapabilitas proses layanan pelanggan.

Setelah kerangka pengukuran ditetapkan, BAB III memperkenalkan DMAIC sebagai alur kerja. Define menetapkan ruang lingkup dan CTQ, Measure mengukur baseline dan memilih prioritas, Analyze mencari akar penyebab, Improve menjalankan perbaikan, dan Control menjaga hasil agar berkelanjutan.

Bagian pengumpulan data menegaskan bahwa penelitian menggunakan data sekunder dari log operasional. Data 2025 digunakan sebagai baseline agregat. Data Januari-April 2026 digunakan sebagai evidence implementasi PDCA, sedangkan data Januari-Mei 2026 digunakan sebagai evaluasi awal perubahan kinerja pada area prioritas.

Data yang digunakan mencakup total issue ticket, FCR, Non-FCR, SLA breach, detail produk, kategori issue, tagging alasan operasional, ticket notes, issue tracker, dan catatan eskalasi tim pengembang. Data agregat digunakan untuk menghitung baseline, sedangkan data row-level digunakan untuk stratifikasi, Pareto, root cause, dan evidence Improve.

Pada fase Define, penelitian membatasi proses dari customer inquiry diterima melalui live chat sampai inquiry selesai atau ditutup. FCR ditetapkan sebagai CTQ dan Non-FCR sebagai defect. SIPOC dan flowchart digunakan untuk memahami batas proses, aktor, input, output, dan titik potensi kegagalan.

Pada fase Measure, penelitian menghitung baseline kinerja proses menggunakan FCR, Non-FCR, DPMO, dan SLA breach. Setelah baseline diperoleh, Non-FCR distratifikasi berdasarkan produk, kategori issue, dan tagging. Pareto digunakan untuk memilih area prioritas yang kontribusi defect-nya paling besar.

Pada fase Analyze, area prioritas hasil Measure dianalisis sampai akar penyebab. Fishbone 6M digunakan sebagai kerangka: Man, Machine, Method, Material, Measurement, dan Mother Nature/Environment. Analisis didukung oleh data operasional seperti ticket notes, tagging, issue tracker, catatan eskalasi, dan contoh kasus teknis.

Pada fase Improve, penelitian memakai PDCA sebagai kerangka implementasi terbatas. Plan menentukan prioritas issue dan rencana perbaikan, Do berjalan melalui biweekly meeting Customer Service dan tim pengembang, Check memantau status issue pada tracker, dan Act menstandarkan pembelajaran melalui knowledge base, SOP, dan aturan eskalasi.

Pada fase Control, penelitian merancang mekanisme pengendalian melalui dashboard monitoring, issue tracker, standardisasi SOP, knowledge base, dan response plan. Control tidak hanya membaca apakah angka membaik, tetapi juga memastikan hasil perbaikan dapat dipantau dan dikembalikan ke siklus PDCA jika masalah muncul lagi.

BAB III ditutup dengan metode evaluasi. Evaluasi dilakukan secara bertahap: baseline 2025, implementasi PDCA Jan-Apr 2026, dan evaluasi awal Jan-May 2026. Metrik yang dipakai adalah SLA breach, FCR/Non-FCR, dan DPMO. Target FCR 90% diposisikan sebagai acuan kinerja, bukan satu-satunya ukuran keberhasilan.

## Kronologi Data

| Periode | Fungsi dalam Riset | Cara Membaca |
|---|---|---|
| Jan-Dec 2025 | Baseline agregat | Mengukur kondisi awal FCR, Non-FCR, DPMO, dan SLA breach. |
| Jan-Apr 2026 | Implementasi PDCA | Evidence bahwa Improve dijalankan melalui issue tracker, biweekly meeting, dan catatan eskalasi. |
| Jan-May 2026 | Evaluasi awal | Membaca perubahan kinerja pada area prioritas tanpa klaim kausal berlebihan. |

## Kontrak Tiap Fase DMAIC

| Fase | Tugas Utama | Output yang Diharapkan |
|---|---|---|
| Define | Menetapkan ruang lingkup, CTQ, SIPOC, dan flowchart. | FCR sebagai CTQ, Non-FCR sebagai defect, batas proses live chat. |
| Measure | Mengukur baseline dan memilih prioritas berbasis data. | Baseline FCR/Non-FCR/DPMO/SLA breach, stratifikasi, Pareto. |
| Analyze | Menemukan akar penyebab pada area prioritas. | Fishbone 6M, root cause berbasis evidence operasional. |
| Improve | Menjalankan perbaikan terbatas berbasis PDCA. | Issue prioritas, tindak lanjut, bug yang sudah dilakukan perbaikan, update knowledge base/SOP. |
| Control | Menjaga hasil dan mencegah regresi proses. | Dashboard, control plan, response plan, standardisasi, monitoring berkala. |

## Metrik Evaluasi

| Metrik | Definisi Operasional | Fungsi |
|---|---|---|
| FCR | Persentase issue ticket yang selesai pada interaksi chat pertama. | Indikator utama efektivitas proses. |
| Non-FCR | Issue ticket yang tidak selesai pada kontak pertama. | Defect layanan. |
| DPMO | Defect per satu juta opportunity. | Ukuran kapabilitas proses. |
| SLA breach | Tiket issue yang melewati batas resolusi 24 jam. | Metrik dampak pendukung. |
| Target FCR 90% | Acuan kinerja yang diharapkan. | Bukan satu-satunya indikator keberhasilan. |

## Alur Argumen

| Lokasi | Ide Utama | Fungsi dalam BAB III |
|---|---|---|
| Kerangka Penelitian | FCR menjadi indikator utama, Non-FCR menjadi defect. | Mengunci cara penelitian membaca masalah. |
| DPMO | Setiap inquiry adalah satu unit dengan satu opportunity. | Menjustifikasi pengukuran kapabilitas proses. |
| Metode Pengumpulan Data | Data 2025, Jan-Apr 2026, dan Jan-May 2026 punya fungsi berbeda. | Menjaga kronologi riset. |
| Data Row-Level | Produk, kategori issue, dan tagging digunakan untuk stratifikasi. | Membuat prioritas berbasis data, bukan asumsi. |
| Define | SIPOC dan flowchart memetakan proses layanan. | Menentukan batas masalah. |
| Measure | Baseline dan Pareto menentukan prioritas. | Menjawab pola dan distribusi variasi FCR. |
| Analyze | Fishbone 6M membaca akar penyebab. | Menjawab faktor proses penyebab Non-FCR. |
| Improve | PDCA menjalankan tindak lanjut perbaikan. | Menjelaskan implementasi Lean Six Sigma. |
| Control | Dashboard dan standardisasi menjaga hasil. | Menjawab keberlanjutan perbaikan dan SLA 24 jam. |
| Evaluasi Hasil | Baseline, implementasi, dan evaluasi awal dibandingkan hati-hati. | Menghindari overclaim kausal. |

## Mapping RQ ke Metode

| RQ | Dijawab oleh | Bukti yang Diharapkan di BAB IV |
|---|---|---|
| RQ1: pola dan distribusi FCR | Measure | Baseline FCR, Non-FCR, DPMO, SLA breach, Pareto. |
| RQ2: faktor proses penyebab variasi FCR | Analyze | Fishbone 6M dan root cause berbasis data operasional. |
| RQ3: penerapan DMAIC untuk meningkatkan dan menstabilkan FCR | Improve | PDCA, biweekly meeting, issue tracker, bug yang sudah dilakukan perbaikan. |
| RQ4: perbaikan berkelanjutan untuk SLA 24 jam | Control | Dashboard, control plan, SOP, knowledge base, response plan. |

## Benang Merah ke BAB IV

BAB IV harus membuktikan bahwa blueprint BAB III benar-benar dijalankan. Karena BAB III menetapkan baseline 2025, BAB IV perlu menunjukkan baseline FCR, Non-FCR, DPMO, dan SLA breach. Karena BAB III menetapkan stratifikasi dan Pareto, BAB IV perlu menunjukkan area prioritas dan issue tag utama. Karena BAB III menetapkan Fishbone 6M, BAB IV perlu memakai kategori 6M yang sama. Karena BAB III menetapkan PDCA, BAB IV perlu menunjukkan evidence implementasi Jan-Apr 2026. Karena BAB III menetapkan Control, BAB IV perlu menunjukkan evaluasi awal dan mekanisme monitoring.

## Backlog Terkait BAB III

| Backlog | Status | Makna untuk BAB III |
|---|---|---|
| BL-02 | Selesai | Data 2025, Jan-Apr 2026, dan Jan-May 2026 sudah dibedakan fungsinya. |
| BL-06 | Selesai | Improve memakai PDCA, bukan FMEA. |
| BL-09 | Selesai | Ekstraksi metrik sudah ditempatkan pada Measure, bukan Define. |
| BL-10 | Selesai | Fishbone memakai 6M secara konsisten. |
| BL-13 | Selesai | Target FCR 90% diposisikan sebagai acuan, bukan satu-satunya ukuran keberhasilan. |
| BL-14 | Selesai | Root cause ditopang data pendukung seperti ticket notes, tagging, issue tracker, dan catatan eskalasi. |
| BL-15 | Selesai | Improve diperkuat dengan evidence issue tracker dan bug yang sudah dilakukan perbaikan. |

## Catatan Koherensi

- BAB III harus tetap terbaca sebagai desain metode, bukan hasil penelitian. Product 1 dan tag spesifik sebaiknya dibaca sebagai output fase Measure di BAB IV; di BAB III cukup aman memakai frasa "area prioritas hasil Measure" bila ingin menjaga kronologi.
- Measure tidak boleh membahas root cause, bug, PDCA, atau hasil perbaikan. Measure cukup baseline, stratifikasi, dan Pareto.
- Analyze adalah titik pertama untuk membahas bug, root cause, Fishbone, dan data pendukung teknis.
- Improve adalah titik pertama untuk membahas bug dilaporkan vs bug yang sudah dilakukan perbaikan.
- Control adalah tempat membaca tren 2025 vs 2026, evaluasi awal, tag-level evidence, dan sustainability.
- Judul BAB masih tertulis `METODE/METODOLOGI PENELITIAN`; secara formal lebih rapi jika dipilih salah satu.
- Caption gambar seperti `Gambar 3. 1` dapat dirapikan menjadi `Gambar 3.1`.

## Ringkasan Super Singkat

BAB III adalah rencana eksekusi DMAIC. Penelitian memakai data 2025 sebagai baseline, data Jan-Apr 2026 sebagai evidence implementasi PDCA, dan data Jan-May 2026 sebagai evaluasi awal. Define menetapkan FCR sebagai CTQ dan Non-FCR sebagai defect. Measure menghitung baseline dan memilih area prioritas lewat Pareto. Analyze mencari akar penyebab dengan Fishbone 6M. Improve menjalankan PDCA melalui issue tracker dan biweekly meeting. Control menggunakan dashboard, SOP, knowledge base, dan response plan untuk menjaga hasil. Evaluasi dilakukan dengan FCR, Non-FCR, DPMO, dan SLA breach secara hati-hati agar tidak overclaim.

## Koneksi

- Sebelumnya: [[BAB 2 - Summary Tinjauan Pustaka]]
- Berikutnya: [[BAB 4 - Summary Hasil Penelitian]]
