# Outline Jurnal JISS - Lean Six Sigma SaaS FCR

Tanggal: 2026-07-06

## Keputusan Utama

Artikel jurnal sebaiknya menjadi versi ringkas tesis yang fokus pada satu alur kuat: Non-FCR pada layanan pelanggan SaaS diperlakukan sebagai defect proses, diprioritaskan dengan stratifikasi dan Pareto, dianalisis dengan DMAIC, lalu dibaca hasil awalnya melalui FCR, DPMO, SLA breach, dan pergerakan tag prioritas.

Yang dipangkas dari tesis: empat RQ tesis, uraian teori yang panjang, seluruh waste Lean, dan detail dashboard. Artikel cukup memakai maksimal dua RQ, satu studi kasus, dan display data yang benar-benar menjelaskan hasil.

## Sumber Yang Dipelajari

- Template JISS: `JISS Journal/template Paper Jurnal JISS Untirta-start october 2020.docx`.
- Referensi implementasi Lean Six Sigma: Laureani, Antony, and Douglas, "Lean six sigma in a call centre: A case study", International Journal of Productivity and Performance Management, 2010.
- Ringkasan tesis: `obsidian_exports/BAB 1 - Summary Pendahuluan.md` sampai `obsidian_exports/BAB 5 - Summary Simpulan dan Saran.md`.
- Data angka riset: `obsidian_exports/Data Reproduksi Perhitungan Riset.md` dan `obsidian_exports/Angka Baseline 2025 - FCR Non-FCR SLA.md`.

## Struktur Template JISS Yang Harus Diikuti

- Article type: `Original research article`.
- Title: 10-15 kata, sentence case, sebaiknya tidak menyebut nama perusahaan/lokasi.
- Front matter: title, author, affiliation, article info, abstract, keywords.
- Abstract: 150-250 kata, satu paragraf, tanpa subheading.
- Main sections: `Introduction`, `Material and method`, `Results and discussions`, `Conclusions`.
- SOTA/literature review dimasukkan ke `Introduction`, tidak perlu section `Literature review` terpisah.
- Reference style: IEEE numbered citation, minimal 30 artikel, minimal 80% jurnal, utamakan 10 tahun terakhir dan DOI jika tersedia.
- Tables and figures: harus dirujuk sebelum muncul; caption tabel di atas, caption gambar di bawah.
- Layout naskah final: mengikuti template JISS, body 10 pt, single spacing, main text dua kolom.

## Insight Dari Referensi Laureani Et Al.

Referensi Laureani et al. relevan karena sama-sama memakai Lean Six Sigma pada konteks layanan pelanggan dan menargetkan first-call resolution. Pola implementasinya:

- Define: membentuk tim lintas fungsi, membuat SIPOC, memetakan proses, dan menyepakati definisi operasional first-call resolution.
- Measure: menghitung baseline unresolved first-time calls dan DPMO sebagai pembanding sebelum-sesudah.
- Analyze: memakai Pareto untuk memilih tipe query dominan; fokus diarahkan ke kategori yang menjelaskan sebagian besar unresolved calls.
- Improve: melakukan quick wins dan pilot improvement.
- Control: menyerahkan control plan ke process owner dan memakai monitoring untuk menjaga hasil.

Angka penting dari studi itu: unresolved first-time calls turun dari 11.82% menjadi 8.45%, dan penurunan sekitar 3% diproyeksikan mengurangi 36,000 panggilan ulang per tahun.

Cara memakainya di jurnal ini: Laureani et al. menjadi pembanding metodologis. Artikel kita tidak meniru call centre telepon, tetapi memperluas logika DMAIC ke live-chat SaaS dengan Non-FCR, DPMO, issue tag, issue tracker, dan PDCA berbasis evidence operasional.

## Judul Yang Disarankan

Judul utama:

`Improving first contact resolution in SaaS customer support through Lean Six Sigma`

Alternatif:

- `Reducing non-FCR defects in SaaS customer support using DMAIC`
- `Data-driven defect reduction in SaaS customer inquiries using Lean Six Sigma`
- `A DMAIC-based approach for improving SaaS customer support resolution`

Rekomendasi: pakai judul utama. Panjangnya 12 kata, sesuai template JISS, dan langsung menjual kontribusi artikel.

## Scope Artikel

- Konteks: perusahaan SaaS, proses layanan pelanggan kanal live chat.
- Unit analisis: inquiry berjenis issue.
- CTQ: First Contact Resolution (FCR).
- Defect: Non-FCR, yaitu inquiry yang tidak selesai pada kontak pertama.
- Baseline: Januari-Desember 2025.
- Improve evidence: Januari-April 2026.
- Early evaluation/control reading: Januari-Mei 2026.
- Fokus hasil: Product 1 dan enam tag prioritas: REPORT ERP, PURCHASING, INVENTORY, ACCOUNTING, FINANCE, MASTER.
- Batas klaim: descriptive process improvement, bukan pembuktian kausal statistik.

## Research Questions Artikel

RQ1. How are non-first-contact-resolution defects distributed across product and issue-tag dimensions in SaaS live-chat support?

RQ2. How can a DMAIC-based improvement process diagnose dominant Non-FCR causes and indicate early changes in FCR, DPMO, and SLA-breach performance?

Catatan: dua RQ ini sudah mencakup empat RQ tesis secara ringkas. RQ1 menampung pola distribusi dan prioritas. RQ2 menampung root cause, improve, control, dan hasil awal.

## Objective Artikel

This study aims to identify dominant Non-FCR defect patterns in SaaS live-chat customer support and evaluate early performance changes after a DMAIC-based improvement process.

## Kontribusi Ilmiah

- Mengoperasionalkan Non-FCR sebagai service-process defect pada konteks SaaS customer support.
- Menggunakan DPMO untuk membaca kapabilitas proses layanan, bukan hanya persentase operasional.
- Menunjukkan prioritisasi berbasis data melalui stratifikasi produk dan Pareto issue tag.
- Menghubungkan Fishbone 6M dengan evidence operasional seperti issue tracker, catatan eskalasi, dan status perbaikan.
- Memberikan control reading awal berbasis FCR, Non-FCR, DPMO, SLA breach, dan tag-level movement.

## Page Budget Maksimal 8 Halaman

| Halaman | Isi | Target kepadatan |
|---:|---|---|
| 1 | Title, author, abstract, keywords, awal Introduction | Abstract padat 180-220 kata. |
| 2 | Introduction lanjutan: SOTA, gap, objective, contribution | Tidak ada literature review terpisah. |
| 3 | Material and method: design, data, operational definition, DMAIC procedure | Satu tabel definisi metrik. |
| 4 | Results: Define dan Measure baseline | Satu tabel baseline agregat dan produk. |
| 5 | Results: Pareto dan Analyze root cause | Satu Pareto dan satu tabel root cause ringkas. |
| 6 | Results: Improve evidence dan Control reading | Satu tabel consolidated PDCA-control. |
| 7 | Discussion, implications, limitation | Bandingkan dengan Laureani et al. dan LSS service literature. |
| 8 | Conclusions, statements, awal References | Referensi IEEE dibuat sangat ringkas dua kolom. |

Jika 30 referensi membuat halaman 8 terlalu penuh, kurangi jumlah display item, bukan menghapus data inti.

## Outline Naskah Mengikuti Template JISS

### Front Matter

Isi:

- Original research article.
- Title.
- Author and affiliation.
- Article history mengikuti template.
- Abstract 150-250 kata.
- Keywords: Lean Six Sigma; DMAIC; first contact resolution; SaaS; customer support.

Abstract harus memuat angka berikut secara sangat selektif:

- Baseline Product 1 FCR 67.93%.
- Enam tag prioritas menyumbang 1,794 defect atau 64.42% Non-FCR Product 1.
- Early evaluation FCR naik menjadi 73.74%.
- DPMO turun dari 320,684 menjadi 262,586.
- SLA breach turun dari 20.21% menjadi 14.56%.

### 1. Introduction

Alur paragraf:

1. SaaS bergantung pada kualitas dukungan pelanggan karena pelanggan memakai produk secara berulang dan dapat berpindah layanan.
2. Live-chat customer support menghasilkan data proses yang dapat digunakan untuk membaca kualitas penyelesaian inquiry.
3. FCR adalah CTQ karena mengukur penyelesaian pada kontak pertama.
4. Non-FCR diposisikan sebagai defect karena memicu rework, eskalasi, waiting, extra-processing, dan risiko SLA breach.
5. SOTA: Lean Six Sigma sudah diterapkan di layanan dan call centre; Laureani et al. menunjukkan DMAIC dapat meningkatkan FCR melalui SIPOC, DPMO, Pareto, improvement action, dan control plan.
6. Gap: masih terbatas studi yang membaca Non-FCR live-chat SaaS sebagai defect berbasis DPMO dan menautkannya ke issue-tag-level PDCA.
7. Objective dan dua RQ.
8. Kontribusi artikel.

Jangan masukkan terlalu banyak teori SaaS. Cukup untuk menjelaskan kenapa customer support adalah bagian dari service quality.

### 2. Material and method

Subsection yang disarankan:

#### 2.1 Research design and scope

Single-case applied process improvement menggunakan Lean Six Sigma DMAIC. Fokus pada inquiry berjenis issue dari kanal live chat. Nama perusahaan, produk, dan detail sensitif dianonimkan.

#### 2.2 Data source and analysis period

Data sekunder dari sistem operasional customer support:

- 2025 issue inquiry records untuk baseline.
- Jan-Apr 2026 follow-up records untuk evidence Improve.
- Jan-May 2026 Product 1 issue inquiry records untuk early evaluation.

#### 2.3 Operational definitions

Masukkan tabel ringkas:

| Metric | Definition | Formula/use |
|---|---|---|
| FCR | Inquiry selesai pada kontak pertama | FCR / total issue inquiry |
| Non-FCR | Inquiry tidak selesai pada kontak pertama | Defect |
| DPMO | Defect per million opportunities | Non-FCR / total inquiry x 1,000,000 |
| SLA breach | Non-FCR lebih dari 24 jam | Impact metric |
| Issue tag | Kategori issue operasional | Pareto and tag-level control |

#### 2.4 DMAIC procedure

Ringkas dalam paragraf atau tabel kecil:

- Define: CTQ, defect definition, SIPOC, inquiry flow.
- Measure: baseline, product stratification, Pareto tag.
- Analyze: Fishbone 6M pada enam tag prioritas.
- Improve: PDCA Jan-Apr 2026, issue tracker, biweekly meeting, knowledge base, escalation rules.
- Control: comparison baseline vs Jan-Apr vs Jan-May, response plan, tag-level monitoring.

#### 2.5 Analytical boundary

Tegaskan bahwa evaluasi bersifat deskriptif dan evidence-supported. Hindari klaim bahwa semua perubahan pasti disebabkan PDCA.

### 3. Results and discussions

#### 3.1 Define: CTQ and service-process defect

Isi:

- FCR sebagai CTQ.
- Non-FCR sebagai defect.
- SLA breach sebagai impact metric, bukan defect utama.
- SIPOC atau flowchart ringkas inquiry live chat.

Display opsional:

- Fig. 1. DMAIC flow for SaaS customer inquiry improvement.

Jika halaman terlalu penuh, Fig. 1 diganti narasi pendek.

#### 3.2 Measure: baseline and priority selection

Masukkan angka baseline utama:

| Area | Metric | Value |
|---|---|---:|
| Aggregate 2025 | Total issue inquiry | 39,414 |
| Aggregate 2025 | FCR | 34,675 (87.98%) |
| Aggregate 2025 | Non-FCR | 4,739 (12.02%) |
| Aggregate 2025 | DPMO Non-FCR | 120,236 |
| Aggregate 2025 | SLA breach | 3,145 (7.98%) |
| Product 1 2025 | FCR | 5,997 (67.93%) |
| Product 1 2025 | Non-FCR | 2,831 (32.07%) |
| Product 1 2025 | DPMO | 320,684 |
| Product 1 2025 | SLA breach rate | 20.21% |
| Product 2 2025 | FCR rate | 93.76% |

Narasi inti:

Product 1 menjadi priority area karena FCR jauh lebih rendah, Non-FCR rate lebih tinggi, DPMO lebih buruk, dan SLA breach rate lebih tinggi daripada Product 2.

#### 3.3 Measure continued: Pareto of Product 1 Non-FCR

Masukkan Pareto enam tag:

| Rank | Issue tag | Non-FCR 2025 | Cumulative contribution |
|---:|---|---:|---:|
| 1 | REPORT ERP | 380 | 13.64% |
| 2 | PURCHASING | 380 | 27.29% |
| 3 | INVENTORY | 377 | 40.83% |
| 4 | ACCOUNTING | 269 | 50.48% |
| 5 | FINANCE | 195 | 57.49% |
| 6 | MASTER | 193 | 64.42% |

Display:

- Fig. 2. Pareto of Product 1 Non-FCR by issue tag.

Narasi inti:

Enam tag menghasilkan 1,794 defect atau 64.42% dari Non-FCR Product 1, sehingga layak menjadi fokus Analyze dan Improve.

#### 3.4 Analyze: dominant process causes

Ringkas root cause ke satu tabel:

| Tag | Dominant pattern | Root cause dimension |
|---|---|---|
| REPORT ERP | Report mismatch, query/report calculation | Machine, Measurement |
| PURCHASING | Purchase validation and transaction integration | Machine, Method |
| INVENTORY | Stock movement and synchronization mismatch | Machine, Measurement |
| ACCOUNTING | Journal generation and technical validation | Machine, Measurement |
| FINANCE | Settlement/payment logic and data repair | Machine, Method |
| MASTER | Master data and upload/download queue | Machine, Method |

Narasi diskusi:

Root cause tidak dominan pada agen/manpower, tetapi pada Machine, Method, dan Measurement. Ini selaras dengan prinsip Laureani et al. bahwa data dan Pareto harus mengarahkan root cause, bukan asumsi awal.

#### 3.5 Improve: PDCA evidence

Masukkan evidence per tag:

| Tag | Bugs reported | Bugs fixed | Fixed rate |
|---|---:|---:|---:|
| REPORT ERP | 72 | 47 | 65% |
| PURCHASING | 66 | 49 | 74% |
| INVENTORY | 56 | 44 | 79% |
| ACCOUNTING | 55 | 31 | 56% |
| FINANCE | 35 | 27 | 77% |
| MASTER | 24 | 21 | 88% |

Narasi inti:

PDCA dilakukan melalui prioritas issue, biweekly meeting, issue tracker, tindak lanjut teknis, pembaruan knowledge base, dan aturan eskalasi. Tabel ini adalah evidence pelaksanaan Improve, bukan bukti akhir keberhasilan.

#### 3.6 Control: early performance reading

Masukkan comparison utama:

| Period | FCR | Non-FCR | DPMO | SLA breach | Avg issue inquiry/month |
|---|---:|---:|---:|---:|---:|
| Baseline 2025 | 67.93% | 2,831 (32.07%) | 320,684 | 20.21% | 735.67 |
| PDCA Jan-Apr 2026 | 72.21% | 881 (27.79%) | 277,918 | 15.39% | 792.50 |
| Early evaluation Jan-May 2026 | 73.74% | 1,064 (26.26%) | 262,586 | 14.56% | 810.40 |

Narasi inti:

- FCR Product 1 naik 5.81 percentage points dari baseline ke Jan-May 2026.
- DPMO turun 58,098 atau sekitar 18.12%.
- SLA breach rate turun 5.65 percentage points.
- Perbaikan terjadi meski rata-rata inquiry bulanan naik dari 735.67 ke 810.40.

Tambahkan tag-level reading secara ringkas:

| Tag | FCR 2025 | FCR Jan-May 2026 | Delta |
|---|---:|---:|---:|
| REPORT ERP | 54.60% | 59.21% | +4.61 pp |
| PURCHASING | 76.47% | 79.03% | +2.56 pp |
| INVENTORY | 73.36% | 75.05% | +1.69 pp |
| ACCOUNTING | 64.61% | 60.53% | -4.07 pp |
| FINANCE | 53.35% | 61.48% | +8.13 pp |
| MASTER | 75.78% | 85.84% | +10.06 pp |

Narasi diskusi:

FINANCE dan MASTER menjadi evidence terkuat karena fixed rate tinggi dan delta FCR paling besar. ACCOUNTING perlu control lanjutan karena FCR turun.

#### 3.7 Discussion against literature

Poin diskusi:

- Hasil mendukung Laureani et al. bahwa DMAIC dapat digunakan untuk meningkatkan first-call/contact resolution pada layanan pelanggan.
- Sama seperti call centre, Pareto membantu membatasi fokus ke query/issue dominan.
- Perbedaannya, artikel ini memakai konteks SaaS live chat, issue-tag operational logs, dan DPMO Non-FCR.
- Implikasi praktis: perusahaan SaaS tidak cukup mengukur response speed; perlu mengukur defect penyelesaian, root cause teknis-proses, dan control tag-level.
- Kehati-hatian: hasil adalah early indication, bukan klaim kausal final.

### 4. Conclusions

Jawab RQ:

- RQ1: Non-FCR tidak tersebar merata. Product 1 menjadi area prioritas dengan FCR 67.93%, Non-FCR 2,831, DPMO 320,684, dan SLA breach 20.21%. Enam tag utama menyumbang 1,794 defect atau 64.42% dari Non-FCR Product 1.
- RQ2: DMAIC membantu menelusuri root cause dominan pada Machine, Method, dan Measurement, menjalankan PDCA Jan-Apr 2026, dan menunjukkan indikasi perbaikan awal: FCR naik ke 73.74%, DPMO turun ke 262,586, dan SLA breach turun ke 14.56%.

Limitations:

- Single-case study.
- Data berasal dari log operasional internal.
- Evaluasi Jan-May 2026 masih early evaluation.
- Belum menguji kausalitas statistik.
- Belum menghubungkan hasil dengan CSAT, churn, atau complaint rate.

Future research:

- Periode Control lebih panjang.
- Gunakan SPC/control chart untuk stabilitas proses.
- Hubungkan FCR dengan CSAT atau retention.
- Validasi pada produk/perusahaan SaaS lain.

## Rencana Display Final

Versi hemat untuk 8 halaman:

| Display | Status | Isi |
|---|---|---|
| Table 1 | Wajib | Operational definitions and formulas. |
| Table 2 | Wajib | Aggregate and product-level baseline 2025. |
| Fig. 1 | Wajib | Pareto of Product 1 Non-FCR by issue tag. |
| Table 3 | Wajib | Root cause and PDCA evidence consolidated by tag. |
| Table 4 | Wajib | Baseline vs PDCA vs early evaluation metrics. |
| Table 5 | Opsional | Tag-level FCR movement. |
| Fig. 2 | Opsional | DMAIC framework or FCR-DPMO-SLA trend. |

Jika halaman penuh, gabungkan Table 3 dan tag-level delta ke satu tabel ringkas. Jangan hapus Table 2 dan Table 4 karena dua tabel itu membawa argumen data utama.

## Literatur Seed Untuk Final References

Seed minimal dari folder referensi dan thesis mapping:

- Laureani et al. 2010 - Lean Six Sigma in a call centre.
- Andini and Yudoko 2024 - Business process improvement in call center operations using LSS.
- Wahed et al. 2023 - Lean principle in a call center.
- Sisman and Orel - Six Sigma for customer complaint management.
- Adanigbo et al. - LSS framework for customer support delays.
- Kowalik 2018 - Six Sigma for service process quality.
- Lameijer et al. - LSS implementation in service/automation.
- Converso et al. - Lean service waste classification.
- Amin et al. - Lean service conceptual model.
- Seddon et al. - Rethinking Lean Service.
- Benlian et al. - SaaS service quality.
- Alotaibi - SaaS adoption.
- Hamtini 2023 - Customer-based software product guidance.
- Sakyi et al. - Customer service analytics.
- Zangari et al. - Ticket automation.

Final paper tetap perlu minimal 30 referensi sesuai template JISS.

## Checklist Sebelum Drafting Paper

- Pilih judul final.
- Konfirmasi bahasa final artikel: disarankan English penuh karena template JISS memakai English.
- Konfirmasi author, affiliation, and corresponding author.
- Anonimkan perusahaan, Product 1/Product 2, dan detail teknis sensitif.
- Validasi ulang angka dari paket data final.
- Siapkan gambar Pareto resolusi minimal 600 dpi.
- Rapikan referensi IEEE dan DOI.
- Tulis AI Usage Statement sesuai kebijakan JISS.

