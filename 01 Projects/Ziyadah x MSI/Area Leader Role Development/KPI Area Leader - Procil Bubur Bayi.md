---
title: KPI Area Leader - Procil Bubur Bayi
project: Ziyadah Consulting - MSI
role: Area Leader
status: draft
created: 2026-06-24
tags:
  - MSI
  - KPI
  - area-leader
  - operations
---

# KPI Area Leader - Procil Bubur Bayi

## 1. Tujuan Utama Role

Area Leader bertanggung jawab memastikan sampai dengan **10 store Procil Bubur Bayi** berjalan stabil, sesuai standar, dan mencapai target bisnis, walaupun setiap outlet **tidak memiliki outlet leader formal**.

Fokus utama role ini:

- Menjaga performa sales area.
- Menjaga standar kualitas produk, kebersihan, dan keamanan pangan.
- Memastikan eksekusi operasional harian berjalan konsisten di semua outlet.
- Menutup masalah outlet sampai selesai.
- Mencegah masalah operasional yang sama terus berulang.

Prinsip KPI:

> Satu KPI hanya mengukur satu hal. Data harus bisa dikumpulkan rutin, dihitung jelas, dan dipakai untuk mengambil keputusan operasional.

## 2. Ringkasan KPI Utama

| KPI | Bobot | Metric Utama | Review |
|---|---:|---|---|
| Sales Achievement Area | 25% | % sales area terhadap target | Mingguan, bulanan |
| Operational Compliance Score | 20% | % checklist sesuai standar | Mingguan |
| Valid Complaint Rate | 15% | Komplain valid per 1.000 transaksi | Mingguan, bulanan |
| Store Visit Coverage | 15% | % outlet aktif yang dikunjungi sesuai siklus | Mingguan |
| Corrective Action Closure Rate | 15% | % action item selesai tepat waktu | Mingguan |
| Overtime Cost Ratio | 10% | Biaya overtime terhadap total labor cost | Mingguan, bulanan |
| **Total** | **100%** |  |  |

Catatan penting:

- KPI crew reliability dihapus karena urgensinya kurang langsung sebagai KPI utama.
- Aktivitas PIC/crew tetap dicatat sebagai **sumber data operasional**, bukan KPI utama.
- `Store Visit Coverage` dan `Corrective Action Closure Rate` dipisah karena visit dan penyelesaian follow-up adalah dua perilaku kerja yang berbeda.
- `Valid Complaint Rate` digunakan karena saat ini belum ada standar SLA komplain.
- Rating Google Business dipantau sebagai external signal, bukan digabung ke KPI complaint.
- `Overtime Cost Ratio` dipakai sebagai KPI cost utama karena paling langsung dipengaruhi Area Leader melalui scheduling, kontrol shift, dan respons terhadap kekurangan manpower.
- Cost lain seperti waste, emergency purchase, transport tambahan, dan petty cash variance dipantau sebagai monitoring cost, bukan digabung ke KPI utama.

## 3. Struktur Workbook Data

Gunakan 1 Google Sheet atau Excel workbook dengan 9 sheet:

1. `Master Outlet`
2. `Daily Sales`
3. `Daily Outlet Report`
4. `Operational Audit`
5. `Complaint Log`
6. `Visit Log`
7. `Action Tracker`
8. `Google Review Snapshot`
9. `Labor Cost`

Sheet `KPI Dashboard` bisa ditambahkan sebagai output ringkasan.

### Master Outlet

Sheet ini menjadi referensi utama agar nama outlet tidak berubah-ubah.

| Field | Contoh | Keterangan |
|---|---|---|
| outlet_id | O001 | Kode unik outlet |
| outlet_name | Procil A | Nama outlet |
| area | Area 1 | Area kerja |
| status | Active | Active/Inactive |
| target_sales_daily | 1500000 | Target sales harian |
| target_sales_monthly | 45000000 | Target sales bulanan |
| visit_frequency_weekly | 1 | Target visit per minggu |
| outlet_priority | Normal | High/Normal/Low |

### Cutoff Submit Data

| Data | Submit Oleh | Waktu Submit | Validasi Oleh |
|---|---|---|---|
| Daily Sales | PIC outlet/admin/POS export | H+1 maksimal 10.00 | Area Leader/Admin |
| Daily Outlet Report | PIC shift/crew senior | Setiap hari setelah closing | Area Leader |
| Operational Audit | Area Leader | Saat visit, maksimal H+1 | Manager/Owner sampling |
| Complaint Log | CS/Admin/Area Leader | Hari yang sama saat komplain masuk | Area Leader |
| Visit Log | Area Leader | Saat visit, maksimal H+1 | Manager/Owner |
| Action Tracker | Area Leader | Setiap ada action item baru atau update status | Manager/Owner |
| Google Review Snapshot | Admin/Area Leader | Mingguan | Manager/Owner |
| Labor Cost | Admin/HR/Finance | Mingguan atau setiap payroll cut-off | Manager/Owner |

## 4. KPI 1 - Sales Achievement Area

**Tujuan:** memastikan Area Leader bertanggung jawab terhadap performa bisnis area.

| Elemen | Detail |
|---|---|
| Metric utama | % sales area terhadap target |
| Formula | Total actual sales area / total target sales area x 100% |
| Bobot | 25% |
| Target awal | 95-100% |
| Sumber data | POS report, rekap kasir, sales report harian |

### Data Yang Harus Disubmit

Sheet: `Daily Sales`

| Field | Wajib | Contoh | Catatan |
|---|---|---|---|
| date | Ya | 2026-06-24 | Tanggal transaksi |
| outlet_id | Ya | O001 | Ambil dari Master Outlet |
| actual_sales | Ya | 1450000 | Total sales harian |
| target_sales | Ya | 1500000 | Target sales harian outlet |
| transaction_count | Disarankan | 85 | Untuk membaca traffic |
| submitted_by | Ya | Nama PIC | Pengirim data |
| submit_timestamp | Ya | 2026-06-25 08:30 | Untuk cek keterlambatan |
| notes | Tidak | Hujan deras | Catatan anomali |

### Cara Submit

- Data sales dikirim setelah closing atau maksimal H+1 pukul 10.00.
- Jika ada POS, data diambil dari export POS.
- Jika belum ada POS terpusat, PIC mengisi Google Form dengan foto bukti closing.
- Area Leader mengecek outlet yang belum submit setiap pagi.

### Cara Pengolahan

Per outlet:

```text
sales_achievement_outlet = actual_sales / target_sales
```

Area:

```text
sales_achievement_area = SUM(actual_sales) / SUM(target_sales)
```

Gap sales:

```text
sales_gap = SUM(actual_sales) - SUM(target_sales)
```

Outlet underperform:

```text
outlet_underperform = sales_achievement_outlet < 90%
```

### Output Dashboard

| Output | Fungsi |
|---|---|
| Sales Achievement Area | Melihat pencapaian area |
| Sales Gap | Melihat kekurangan nominal dari target |
| Outlet Underperform | Menentukan outlet prioritas |
| Trend 7 Hari | Melihat arah performa |

## 5. KPI 2 - Operational Compliance Score

**Tujuan:** memastikan outlet menjalankan standar dasar Procil secara konsisten.

| Elemen | Detail |
|---|---|
| Metric utama | % checklist sesuai standar |
| Formula | Total item sesuai standar / total item diaudit x 100% |
| Bobot | 20% |
| Target awal | Minimal 90% |
| Sumber data | Operational audit saat visit |

### Data Yang Harus Disubmit

Sheet: `Operational Audit`

| Field | Wajib | Contoh | Catatan |
|---|---|---|---|
| audit_date | Ya | 2026-06-24 | Tanggal audit |
| outlet_id | Ya | O001 | Kode outlet |
| auditor | Ya | Area Leader | Nama auditor |
| category | Ya | Kebersihan | Kategori checklist |
| checklist_item | Ya | Area prep bersih | Item standar |
| score | Ya | 1 | 1 = sesuai, 0 = tidak sesuai |
| severity | Ya | Critical/Major/Minor | Tingkat temuan |
| evidence_link | Disarankan | Link foto | Bukti temuan |
| notes | Tidak | Area prep basah | Catatan detail |

Checklist minimal:

| Kategori | Contoh Item |
|---|---|
| Opening/Closing | Outlet buka tepat waktu, closing checklist lengkap |
| Kebersihan | Area kerja, alat, tempat sampah, storage bersih |
| Kualitas Produk | Rasa, tekstur, suhu, porsi, tampilan sesuai standar |
| Stok | Bahan utama cukup, packaging cukup, tidak expired |
| Pelayanan | Crew ramah, responsif, grooming sesuai standar |
| Transaksi | Pencatatan transaksi sesuai |

### Cara Submit

- Area Leader mengisi checklist saat visit outlet.
- Untuk temuan `Critical`, wajib ada foto/evidence.
- Jika ada temuan yang perlu perbaikan, buat action item terpisah di `Action Tracker`.
- Manager/owner bisa melakukan sampling audit untuk validasi.

### Cara Pengolahan

Per outlet:

```text
operational_compliance_outlet = SUM(score) / COUNT(checklist_item)
```

Area:

```text
operational_compliance_area = SUM(score semua outlet) / COUNT(checklist_item semua outlet)
```

Critical finding count:

```text
critical_finding_count = COUNT(severity = "Critical")
```

Repeat finding monitoring:

```text
repeat_finding = item/kategori yang sama muncul lagi di outlet yang sama dalam 30 hari
```

### Output Dashboard

| Output | Fungsi |
|---|---|
| Operational Compliance Score | Melihat kepatuhan standar area |
| Compliance per Outlet | Menentukan outlet yang perlu dibina |
| Critical Finding Count | Melihat risiko kualitas atau keamanan pangan |
| Repeat Finding List | Melihat masalah yang belum selesai sampai akar |

## 6. KPI 3 - Valid Complaint Rate

**Tujuan:** melihat seberapa sering pelanggan mengalami issue yang valid, dinormalisasi terhadap jumlah transaksi.

| Elemen | Detail |
|---|---|
| Metric utama | Komplain valid per 1.000 transaksi |
| Formula | Jumlah komplain valid / jumlah transaksi x 1.000 |
| Bobot | 15% |
| Target awal | Dibuat dari baseline 1-2 bulan pertama, lalu diturunkan bertahap |
| Sumber data | Complaint Log dan Daily Sales |

### Data Yang Harus Disubmit

Sheet: `Complaint Log`

| Field | Wajib | Contoh | Catatan |
|---|---|---|---|
| complaint_date | Ya | 2026-06-24 | Tanggal komplain masuk |
| outlet_id | Ya | O001 | Outlet terkait |
| channel | Ya | WhatsApp | WA/IG/Outlet/Marketplace |
| complaint_category | Ya | Tekstur produk | Kategori masalah |
| severity | Ya | Critical | Critical/Major/Minor |
| customer_issue | Ya | Bubur terlalu cair | Ringkasan komplain |
| root_cause | Jika valid | Takaran air tidak sesuai | Wajib untuk komplain valid |
| status | Ya | Open/Closed | Status penyelesaian |
| valid_complaint | Ya | Yes/No | Valid setelah dicek |
| transaction_reference | Jika ada | TRX-001 | Nomor transaksi jika tersedia |

Kategori `Critical`:

- Rasa, tekstur, atau aroma produk tidak sesuai standar.
- Produk diduga basi atau tidak layak.
- Kebersihan produk atau kemasan bermasalah.
- Kesalahan menu atau porsi untuk bayi.
- Respons crew buruk pada kasus sensitif.

### Cara Submit

- Setiap komplain dicatat di hari yang sama oleh penerima komplain.
- Jika komplain masuk ke outlet, PIC outlet wajib meneruskan ke Area Leader.
- Area Leader memberi label severity dan menentukan validitas komplain.
- Semua komplain valid harus diberi kategori dan root cause setelah dicek.
- Komplain dari Google Review dicatat di `Complaint Log` jika review menyebut issue outlet yang spesifik.

### Cara Pengolahan

Valid Complaint Rate:

```text
valid_complaint_rate = jumlah komplain valid / jumlah transaksi x 1000
```

Valid Complaint Rate per outlet:

```text
valid_complaint_rate_outlet = jumlah komplain valid outlet / jumlah transaksi outlet x 1000
```

Complaint severity mix:

```text
critical_complaint_share = jumlah komplain critical / jumlah komplain valid
```

Repeat complaint:

```text
repeat_complaint = kategori komplain yang sama muncul lagi di outlet yang sama dalam 30 hari
```

### Output Dashboard

| Output | Fungsi |
|---|---|
| Valid Complaint Rate | Melihat frekuensi issue pelanggan |
| Valid Complaint Rate per Outlet | Menentukan outlet yang paling sering bermasalah |
| Complaint Category | Melihat jenis masalah paling sering |
| Repeat Complaint | Menentukan masalah yang perlu perbaikan sistem |
| Critical Complaint Count | Menentukan issue prioritas |

### Catatan Baseline

Karena belum ada standar SLA dan kemungkinan data komplain historis belum rapi, gunakan 1-2 bulan pertama untuk membuat baseline.

Contoh:

```text
baseline_valid_complaint_rate = rata-rata valid complaint rate 8 minggu pertama
```

Setelah baseline terbentuk, target bisa dibuat seperti:

```text
target_valid_complaint_rate = baseline_valid_complaint_rate x 90%
```

Artinya target awal adalah menurunkan complaint rate 10% dari baseline.

## 7. Google Business Rating Monitoring

Bagian ini bukan KPI utama, tetapi external signal untuk membaca pengalaman pelanggan yang tidak selalu masuk ke channel komplain internal.

### Data Yang Harus Disubmit

Sheet: `Google Review Snapshot`

| Field | Wajib | Contoh | Catatan |
|---|---|---|---|
| snapshot_date | Ya | 2026-06-24 | Tanggal pengambilan data |
| outlet_id | Ya | O001 | Outlet terkait |
| google_business_name | Ya | Procil Bubur Bayi A | Nama profil Google |
| average_rating | Ya | 4.6 | Rating rata-rata saat snapshot |
| total_review_count | Ya | 248 | Total review saat snapshot |
| new_review_count | Ya | 5 | Review baru sejak snapshot sebelumnya |
| low_rating_count | Ya | 1 | Review baru dengan rating <= 3 |
| review_rating | Jika detail tersedia | 2 | Rating review individual |
| review_text | Jika detail tersedia | Bubur terlalu encer | Teks review |
| review_category | Jika detail tersedia | Produk | Produk/Pelayanan/Kebersihan/Harga/Lainnya |
| review_link | Jika tersedia | Link review | Bukti/source |

### Cara Submit

- Admin atau Area Leader mengambil snapshot rating Google Business setiap minggu.
- Jika scraping memungkinkan, data bisa diambil per outlet dan dimasukkan ke `Google Review Snapshot`.
- Jika scraping belum siap, lakukan input manual mingguan: average rating, total review count, new review count, dan low rating count.
- Review rating <= 3 wajib dibaca dan dikategorikan.
- Review yang berisi issue spesifik outlet dimasukkan juga ke `Complaint Log` sebagai sumber `Google Review`.

Catatan teknis:

- Jika memungkinkan, gunakan export/API resmi Google Business Profile atau tools yang memang diizinkan perusahaan.
- Jika memakai scraping, simpan tanggal snapshot, nama outlet, rating, teks review, dan link review agar data bisa diaudit.

### Cara Pengolahan

Average rating per outlet:

```text
google_average_rating = rating rata-rata pada snapshot terakhir
```

New low rating count:

```text
new_low_rating_count = jumlah review baru dengan rating <= 3
```

Rating movement:

```text
rating_delta = average_rating minggu ini - average_rating minggu sebelumnya
```

Review issue mix:

```text
review_issue_mix = jumlah review per kategori issue
```

### Output Dashboard

| Output | Fungsi |
|---|---|
| Google Average Rating per Outlet | Melihat persepsi publik per outlet |
| New Low Rating Count | Menandai outlet yang perlu dicek |
| Rating Delta | Melihat arah reputasi outlet |
| Review Issue Mix | Membaca tema masalah pelanggan |

## 8. KPI 4 - Store Visit Coverage

**Tujuan:** memastikan Area Leader hadir secara terencana di outlet, bukan hanya reaktif saat ada masalah.

| Elemen | Detail |
|---|---|
| Metric utama | % outlet aktif yang dikunjungi sesuai siklus |
| Formula | Jumlah outlet aktif yang memenuhi target visit / total outlet aktif x 100% |
| Bobot | 15% |
| Target awal | 100% outlet aktif memenuhi target visit |
| Sumber data | Visit Log |

### Data Yang Harus Disubmit

Sheet: `Visit Log`

| Field | Wajib | Contoh | Catatan |
|---|---|---|---|
| week_start | Ya | 2026-06-22 | Minggu rencana |
| outlet_id | Ya | O001 | Outlet dikunjungi |
| planned_visit_count | Ya | 1 | Target visit outlet minggu itu |
| actual_visit_date | Jika visit | 2026-06-24 | Tanggal aktual |
| visit_type | Ya | Routine | Routine/Issue/Sampling |
| visit_notes | Ya | Stok cup rendah | Catatan utama |
| submitted_by | Ya | Area Leader | Nama pengisi |
| submit_timestamp | Ya | 2026-06-24 16:00 | Waktu submit |

### Cara Submit

- Area Leader membuat target visit mingguan berdasarkan `Master Outlet`.
- Setiap visit dicatat maksimal H+1.
- Outlet high risk bisa punya target visit lebih tinggi.
- Visit harus tetap dicatat walaupun tidak ada temuan.

Rekomendasi target visit:

| Tipe Outlet | Target Visit |
|---|---:|
| High risk | 2-3 kali per minggu |
| Normal | 1 kali per minggu |
| Low risk | Sesuai kebijakan, minimal tetap masuk siklus kontrol |

### Cara Pengolahan

Visit count per outlet:

```text
actual_visit_count = COUNT(actual_visit_date per outlet per week)
```

Outlet meet visit target:

```text
visit_target_met = actual_visit_count >= planned_visit_count
```

Store Visit Coverage:

```text
store_visit_coverage = COUNT(outlet aktif dengan visit_target_met = Yes) / COUNT(outlet aktif)
```

### Output Dashboard

| Output | Fungsi |
|---|---|
| Store Visit Coverage | Melihat coverage kunjungan |
| Outlet Not Visited | Outlet yang tidak tersentuh |
| High Risk Visit Status | Memastikan outlet bermasalah lebih sering dikontrol |
| Visit Notes Summary | Membaca pola temuan lapangan |

## 9. KPI 5 - Corrective Action Closure Rate

**Tujuan:** memastikan temuan operasional tidak hanya dicatat, tetapi selesai tepat waktu.

| Elemen | Detail |
|---|---|
| Metric utama | % action item selesai tepat waktu |
| Formula | Jumlah action item closed on time / total action item x 100% |
| Bobot | 15% |
| Target awal | Minimal 90% |
| Sumber data | Action Tracker |

### Data Yang Harus Disubmit

Sheet: `Action Tracker`

| Field | Wajib | Contoh | Catatan |
|---|---|---|---|
| action_id | Ya | ACT-001 | ID unik action |
| created_date | Ya | 2026-06-24 | Tanggal action dibuat |
| source | Ya | Audit | Audit/Complaint/Visit/Sales |
| outlet_id | Ya | O001 | Outlet terkait |
| issue | Ya | Area prep kotor | Masalah |
| severity | Ya | Major | Critical/Major/Minor |
| action_item | Ya | Deep cleaning area prep | Tindakan |
| action_owner | Ya | PIC O001 | Pemilik tindakan |
| due_date | Ya | 2026-06-25 | Deadline |
| closed_date | Jika selesai | 2026-06-25 | Tanggal selesai |
| status | Ya | Open/Closed/Overdue | Status |
| evidence_link | Disarankan | Link foto | Bukti penyelesaian |

### Cara Submit

- Setiap temuan dari audit, komplain, visit, atau sales review yang butuh tindakan harus dibuat sebagai action item.
- Area Leader menentukan owner dan due date.
- Owner mengirim evidence saat action selesai.
- Area Leader mengubah status menjadi `Closed` setelah evidence diterima.

### Cara Pengolahan

Closed on time:

```text
closed_on_time = status = "Closed" AND closed_date <= due_date
```

Corrective Action Closure Rate:

```text
corrective_action_closure_rate = COUNT(closed_on_time = Yes) / COUNT(action_id)
```

Overdue action:

```text
overdue_action = status != "Closed" AND today > due_date
```

Critical overdue:

```text
critical_overdue = severity = "Critical" AND overdue_action = Yes
```

### Output Dashboard

| Output | Fungsi |
|---|---|
| Corrective Action Closure Rate | Melihat disiplin menutup issue |
| Overdue Action List | Menentukan follow-up prioritas |
| Critical Overdue Count | Melihat risiko tinggi |
| Repeat Source | Melihat sumber masalah terbanyak |

## 10. KPI 6 - Overtime Cost Ratio

**Tujuan:** memastikan Area Leader mengontrol biaya tenaga kerja yang muncul karena overtime.

| Elemen | Detail |
|---|---|
| Metric utama | Biaya overtime terhadap total labor cost |
| Formula | Total overtime cost / total labor cost x 100% |
| Bobot | 10% |
| Target awal | Dibuat dari baseline 1-2 bulan pertama, lalu diturunkan bertahap |
| Sumber data | Jadwal shift, attendance, payroll, dan approval overtime |

### Kenapa Metric Ini Penting

Overtime adalah cost yang paling sering muncul dari masalah operasional yang seharusnya bisa dikontrol Area Leader, misalnya:

- Scheduling tidak rapi.
- Crew kurang pada jam ramai.
- Absensi tidak cepat diantisipasi.
- Outlet terlalu bergantung pada orang tertentu.
- Closing terlalu lama karena disiplin proses lemah.
- Ada issue stok, produksi, atau pelayanan yang membuat jam kerja melebar.

Karena itu, overtime bukan hanya angka finance. Overtime adalah sinyal kualitas manpower planning dan disiplin eksekusi outlet.

### Data Yang Harus Disubmit

Sheet: `Labor Cost`

| Field | Wajib | Contoh | Catatan |
|---|---|---|---|
| period_start | Ya | 2026-06-22 | Awal periode |
| period_end | Ya | 2026-06-28 | Akhir periode |
| outlet_id | Ya | O001 | Outlet terkait |
| employee_name | Ya | Nama Crew | Nama karyawan |
| scheduled_hours | Ya | 48 | Jam kerja sesuai jadwal |
| actual_hours | Ya | 52 | Jam kerja aktual dari attendance |
| overtime_hours | Ya | 4 | Jam overtime |
| regular_labor_cost | Ya | 720000 | Biaya jam kerja normal |
| overtime_cost | Ya | 90000 | Biaya overtime |
| overtime_reason | Ya jika overtime > 0 | Crew absent | Alasan overtime |
| overtime_approved_by | Ya jika overtime > 0 | Area Leader | Approval |
| notes | Tidak | Closing event ramai | Catatan tambahan |

### Cara Submit

- Admin/HR/Finance menarik data attendance dan payroll per minggu atau per cut-off payroll.
- Area Leader wajib memberi reason untuk setiap overtime yang terjadi di outletnya.
- Overtime tanpa reason harus dianggap data tidak lengkap.
- Manager/owner melakukan review untuk outlet dengan overtime tertinggi.

### Cara Pengolahan

Overtime Cost Ratio area:

```text
overtime_cost_ratio = SUM(overtime_cost) / SUM(regular_labor_cost + overtime_cost)
```

Overtime Cost Ratio per outlet:

```text
overtime_cost_ratio_outlet = SUM(overtime_cost outlet) / SUM(total_labor_cost outlet)
```

Overtime hours per transaction:

```text
overtime_hours_per_100_transactions = SUM(overtime_hours) / SUM(transaction_count) x 100
```

Top overtime reason:

```text
top_overtime_reason = reason dengan total overtime_cost terbesar
```

### Output Dashboard

| Output | Fungsi |
|---|---|
| Overtime Cost Ratio | Melihat efisiensi labor cost area |
| Overtime Cost per Outlet | Menentukan outlet dengan overtime tinggi |
| Overtime Reason Mix | Membaca penyebab overtime terbesar |
| Overtime Hours per 100 Transactions | Membandingkan overtime secara lebih fair antar-outlet |

### Monitoring Cost Tambahan

Cost berikut sebaiknya tetap dicatat, tetapi tidak dijadikan KPI utama sampai definisi dan baseline datanya stabil.

| Cost | Cara Track | Kapan Diangkat Jadi KPI |
|---|---|---|
| Waste/spoilage bahan | Nilai waste per outlet per minggu | Jika data waste sudah konsisten dan material |
| Emergency purchase | Nilai pembelian darurat di luar plan | Jika sering terjadi karena planning stok lemah |
| Transport tambahan | Biaya kirim/ambil barang tambahan | Jika sering muncul karena koordinasi stok buruk |
| Petty cash variance | Selisih petty cash vs bukti | Jika ada risiko kontrol kas |

## 11. Skoring KPI Bulanan

Gunakan skala 1-5 untuk mengubah hasil metric menjadi skor KPI.

### Sales Achievement Area

| Hasil | Skor |
|---:|---:|
| >= 105% | 5 |
| 100-104,9% | 4 |
| 95-99,9% | 3 |
| 90-94,9% | 2 |
| < 90% | 1 |

### Operational Compliance Score

| Hasil | Skor |
|---:|---:|
| >= 97% | 5 |
| 93-96,9% | 4 |
| 90-92,9% | 3 |
| 85-89,9% | 2 |
| < 85% | 1 |

### Valid Complaint Rate

| Hasil | Skor |
|---|---:|
| <= 80% dari baseline | 5 |
| > 80-90% dari baseline | 4 |
| > 90-100% dari baseline | 3 |
| > 100-120% dari baseline | 2 |
| > 120% dari baseline | 1 |

### Store Visit Coverage

| Hasil | Skor |
|---:|---:|
| 100% | 5 |
| 95-99,9% | 4 |
| 90-94,9% | 3 |
| 80-89,9% | 2 |
| < 80% | 1 |

### Corrective Action Closure Rate

| Hasil | Skor |
|---:|---:|
| >= 97% | 5 |
| 93-96,9% | 4 |
| 90-92,9% | 3 |
| 80-89,9% | 2 |
| < 80% | 1 |

### Overtime Cost Ratio

| Hasil | Skor |
|---|---:|
| <= 80% dari baseline | 5 |
| > 80-90% dari baseline | 4 |
| > 90-100% dari baseline | 3 |
| > 100-120% dari baseline | 2 |
| > 120% dari baseline | 1 |

### Guardrail Critical Issue

Guardrail ini bukan KPI tambahan, tetapi aturan eskalasi agar issue kritikal tidak tertutup oleh skor rata-rata.

| Kondisi | Tindakan |
|---|---|
| Ada critical complaint belum ditindaklanjuti | Review khusus dengan manager/owner |
| Ada critical finding berulang di outlet yang sama | Wajib root cause review |
| Ada critical action overdue | Wajib eskalasi hari yang sama |

### Formula Skor Akhir

```text
final_score =
(sales_score x 25%) +
(compliance_score x 20%) +
(valid_complaint_rate_score x 15%) +
(store_visit_score x 15%) +
(action_closure_score x 15%) +
(overtime_cost_ratio_score x 10%)
```

Interpretasi:

| Final Score | Interpretasi |
|---:|---|
| 4,50-5,00 | Excellent |
| 4,00-4,49 | Good |
| 3,00-3,99 | Meets expectation |
| 2,00-2,99 | Below expectation |
| < 2,00 | Critical |

## 12. Template Dashboard Mingguan

| KPI | Actual | Target | Status | Outlet Prioritas | Root Cause Utama | Next Action | Owner | Due Date |
|---|---:|---:|---|---|---|---|---|---|
| Sales Achievement Area |  |  |  |  |  |  |  |  |
| Operational Compliance Score |  |  |  |  |  |  |  |  |
| Valid Complaint Rate |  |  |  |  |  |  |  |  |
| Store Visit Coverage |  |  |  |  |  |  |  |  |
| Corrective Action Closure Rate |  |  |  |  |  |  |  |  |
| Overtime Cost Ratio |  |  |  |  |  |  |  |  |

Status:

- Green: sesuai target.
- Yellow: sedikit di bawah target atau ada risiko.
- Red: jauh di bawah target atau ada issue critical.

## 13. Template Penilaian Bulanan

| KPI | Bobot | Actual | Skor 1-5 | Skor Tertimbang | Catatan |
|---|---:|---:|---:|---:|---|
| Sales Achievement Area | 25% |  |  |  |  |
| Operational Compliance Score | 20% |  |  |  |  |
| Valid Complaint Rate | 15% |  |  |  |  |
| Store Visit Coverage | 15% |  |  |  |  |
| Corrective Action Closure Rate | 15% |  |  |  |  |
| Overtime Cost Ratio | 10% |  |  |  |  |
| **Total** | **100%** |  |  |  |  |

## 14. Catatan Implementasi

Untuk 1-2 bulan pertama, KPI sebaiknya dipakai sebagai alat membangun ritme kerja, bukan langsung sebagai alat hukuman.

Prioritas awal Area Leader:

1. Membuat baseline performa setiap outlet.
2. Membuat format laporan outlet harian sederhana.
3. Menentukan siklus visit tiap outlet.
4. Mengunci checklist audit standar.
5. Menutup temuan operasional paling kritikal.

Setelah ritme stabil, KPI bisa digunakan lebih formal untuk evaluasi bulanan.
