# RQ Statement Mapping BAB 5

File ini memetakan empat rumusan masalah penelitian ke jawaban eksplisit yang sudah muncul di BAB 5. Gunakan sebagai checklist saat membaca atau merevisi bagian `5.1 Simpulan` dan `5.2 Saran`.

Related:
- [[BAB 5 - Summary Simpulan dan Saran]]
- [[BAB 4 - Summary Hasil Penelitian]]
- [[BAB 3 - Summary Metodologi Penelitian]]

## Ringkasan Status

BAB 5 sudah menjawab keempat rumusan masalah secara eksplisit. RQ1 sampai RQ4 sudah memiliki statement jawaban di bagian `5.1 Simpulan`, sedangkan RQ4 diperkuat lagi oleh bagian `5.2 Saran`.

## Mapping RQ ke BAB 5

| RQ | Fokus pertanyaan | Lokasi jawaban di BAB 5 | Statement jawaban inti |
|---|---|---|---|
| RQ1 | Bagaimana pola dan distribusi variasi FCR berdasarkan karakteristik inquiry? | `5.1 Simpulan`, paragraf baseline dan stratifikasi produk. | Variasi FCR tidak tersebar merata. Product 1 menjadi area prioritas karena FCR lebih rendah, Non-FCR lebih tinggi, dan SLA breach lebih besar dibanding Product 2. |
| RQ2 | Faktor proses apa yang berkontribusi terhadap variasi FCR? | `5.1 Simpulan`, paragraf Pareto dan Fishbone. | Enam tag utama Product 1 menjadi kontributor Non-FCR terbesar. Faktor dominan berada pada Machine, Method, dan Measurement, terutama mismatch report, journal/settlement, stock, validasi transaksi, logic sistem, manual query, dan manual repair. |
| RQ3 | Bagaimana penerapan Lean Six Sigma DMAIC dalam meningkatkan dan menstabilkan FCR? | `5.1 Simpulan`, paragraf penerapan DMAIC dan evaluasi awal. | DMAIC digunakan secara berurutan: Define menetapkan CTQ dan alur proses, Measure menetapkan baseline dan prioritas, Analyze mencari akar penyebab, Improve menjalankan PDCA, dan Control membaca pergerakan FCR, Non-FCR, DPMO, SLA breach, tag, dan pola issue. |
| RQ4 | Usulan perbaikan berkelanjutan apa yang mendukung konsistensi SLA 24 jam? | `5.1 Simpulan` paragraf akhir dan `5.2 Saran`. | Perbaikan berkelanjutan diarahkan pada monitoring FCR, Non-FCR, DPMO, SLA breach, issue tracker, response plan, knowledge base, aturan eskalasi, dan forum PDCA rutin antara Customer Service dan tim pengembang. |

## Statement Eksplisit per RQ

### RQ1

Temuan baseline dan stratifikasi menjawab rumusan masalah pertama karena menunjukkan bahwa variasi FCR dipengaruhi oleh karakteristik inquiry, terutama produk dan kompleksitas issue. Product 1 menjadi area prioritas karena memiliki FCR paling rendah dan kontribusi Non-FCR paling besar.

### RQ2

Temuan Pareto dan Fishbone menjawab rumusan masalah kedua karena menunjukkan bahwa variasi FCR terutama dipengaruhi oleh faktor Machine, Method, dan Measurement. Faktor tersebut muncul dalam bentuk mismatch data, logic sistem, validasi transaksi, journal/settlement, stock, dan kebutuhan eskalasi teknis.

### RQ3

Penerapan DMAIC menjawab rumusan masalah ketiga karena penelitian tidak hanya mengukur baseline, tetapi juga menurunkan masalah ke area prioritas, mengidentifikasi akar penyebab, menjalankan PDCA, dan mengevaluasi hasil awal melalui metrik FCR, Non-FCR, DPMO, SLA breach, tag, dan pola issue.

### RQ4

Usulan monitoring dan standardisasi menjawab rumusan masalah keempat karena hasil penelitian diterjemahkan menjadi mekanisme kontrol berkelanjutan. Fokusnya adalah menjaga konsistensi FCR dan mendukung SLA 24 jam melalui pemantauan metrik, issue tracker, response plan, knowledge base, aturan eskalasi, dan PDCA rutin.

## Catatan Sinkronisasi

BAB 5 perlu tetap selaras dengan framing terakhir BAB 4:

- Tabel Improve hanya menampilkan pola issue yang masuk sebagai hasil perbaikan efektif.
- Tabel Control per pola hanya membaca pola yang sama dengan Tabel Improve.
- Hindari klaim bahwa seluruh bug yang tercatat di log teknis otomatis selesai pada level akar masalah.
- Gunakan framing sederhana: pola yang masuk Improve dan menunjukkan FCR positif dibaca sebagai hasil perbaikan; pola lain tidak perlu menjadi klaim utama di BAB 5.

