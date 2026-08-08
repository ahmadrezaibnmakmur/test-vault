---
type: project-impact-summary
created: 2026-06-19
project: OKR Automate Disbursement
tags:
  - okr
  - disbursement
  - project-impact
  - process-improvement
  - dmaic
  - control-chart
  - statistical-validation
---

# Project Impact Summary - OKR Automate Disbursement

> [!summary]
> Project ini berdampak kuat karena mengubah proses disbursement dari proses semi-automated yang masih bergantung pada manual checking, reconciliation, dan data adjustment menjadi proses yang lebih stabil, terkendali, dan predictable. Data control period menunjukkan lead time turun dan menjadi konsisten di `14:00`, sementara adjustment rate turun sekitar `82%` dibanding periode sebelum automatic.

![[impact_kpi_cards.svg]]

## Executive Takeaway

Auto Disburse menyelesaikan dua masalah utama sekaligus:

1. **Lead time disbursement tidak stabil.** Sebelum automatic, rata-rata lead time adalah `15.73 jam`, dengan `24.6%` hari selesai setelah jam `17:00`. Setelah automatic mulai `2026-03-12`, semua hari observasi selesai di `14:00`.
2. **Data issue menciptakan rework.** Sebelum automatic, adjustment rate total adalah `0.32%`; setelah automatic turun menjadi `0.06%`. Ini bukan sekadar perbaikan waktu transfer, tetapi perbaikan sistem operasi disbursement.

Secara statistik, improvement ini kuat:

- Mean lead time turun `1.73 jam` dengan bootstrap 95% CI sekitar `-2.13` sampai `-1.34` jam.
- Daily adjustment rate turun `0.267 percentage point` dengan bootstrap 95% CI sekitar `-0.360` sampai `-0.183` percentage point.
- Permutation test untuk perbedaan before vs after menghasilkan `p < 0.001` untuk lead time maupun adjustment rate.
- Sebelum automatic, korelasi antara lead time dan adjustment rate cukup kuat: Pearson `r = 0.65`, permutation `p < 0.001`.

## Business Problem Solved

Konteks project dari deck menyebut bahwa proses disbursement masih semi-automated. Transfer paling cepat dilakukan H+1 dari tanggal transaksi, biasanya sore, dan khusus hari Senin bisa mundur sampai malam. Finance masih perlu melakukan manual checking sebelum transfer, sedangkan reconciliation dibutuhkan karena berbagai data issue transaksi. Ini menyebabkan lead time meningkat dan dependency antar tim tetap tinggi.

Masalah operasional yang dipecahkan:

- Manual checking oleh Finance sebelum transfer.
- Manual reconciliation menggunakan Excel/macro.
- Manual adjustment saat ada discrepancy.
- Manual compiling dan formatting report.
- Dependency ke Data/Finance saat data transaksi bermasalah.
- Risiko error seperti duplicate disbursement, incorrect amount, refund masih masuk data, MDR/discount mismatch, dan bank account issue.

Sumber konteks: [[01 - OKR Automate Disbursement Deck Context]] dan [[deck_extraction]].

## Quantitative Impact

![[before_after_impact.svg]]

| Metric | Before Automatic | After Automatic | Impact |
|---|---:|---:|---:|
| Average lead time | `15.73h` | `14.00h` | `-1.73h` |
| Share of days after 17:00 | `24.6%` | `0.0%` | Eliminated |
| Total adjustment rate | `0.32%` | `0.06%` | `-82.4%` relative |
| Observed days | `138` | `55` | Control period available |

Interpretasi bisnis:

- Proses tidak hanya lebih cepat, tetapi juga lebih **predictable**.
- Jam `14:00` menjadi operating standard baru.
- Hilangnya late-disbursement tail menurunkan risiko complaint dan escalation.
- Penurunan adjustment rate menunjukkan upstream data quality dan control process membaik.

## Trend Evidence

![[monthly_lead_adjustment_trend.svg]]

Terdapat tiga fase yang terlihat dari data:

| Phase | Days | Avg Lead Time | Adjustment Rate |
|---|---:|---:|---:|
| Early observed period, Aug-Sep 2025 | `28` | `17.02h` | `0.89%` |
| Stabilized pre-auto, Oct 2025-Mar 11 2026 | `110` | `15.40h` | `0.20%` |
| Automatic, Mar 12-May 2026 | `55` | `14.00h` | `0.06%` |

Ini menunjukkan improvement bertahap:

- Fase awal masih menunjukkan lead time tinggi dan adjustment rate relatif tinggi.
- Fase stabilisasi menurunkan adjustment rate secara besar, sejalan dengan improvement seperti bulk download, report formatting, access limitation, contract mapping, bank account change limitation, SOP, dan data cleaning.
- Fase automatic mengunci lead time di `14:00`, sehingga variasi operasional hilang.

## Weekday Risk Removed

![[weekday_lead_time_pattern.svg]]

Sebelum automatic, hari Senin adalah risk point utama:

- Monday average lead time sebelum automatic: `18.01h`.
- Monday total adjustment rate sebelum automatic: sekitar `0.60%`.
- Beberapa outlier besar terjadi di hari Senin, misalnya `2025-09-15` dengan lead time `23:48` dan adjustment rate `3.54%`.

Setelah automatic, semua weekday pada periode observasi menjadi `14:00`. Ini penting secara industrial engineering karena variasi berdasarkan hari kerja adalah salah satu sinyal bahwa proses masih bergantung pada kapasitas, antrian manual, atau handoff antar tim. Project ini mengubah proses menjadi lebih controlled dan schedule-driven.

## Correlation: Why Adjustment Matters

![[lead_time_adjustment_correlation.svg]]

Sebelum automatic, data menunjukkan korelasi yang kuat antara lead time dan adjustment:

| Relationship | Pearson | Spearman | Read |
|---|---:|---:|---|
| Lead time vs adjustment rate | `0.65` | `0.52` | Strong positive relationship |
| Lead time vs adjustment count | `0.65` | `0.55` | Strong positive relationship |
| Lead time vs transaction volume | `0.29` | `0.19` | Weak-to-moderate relationship |

Kesimpulan: keterlambatan lebih konsisten dijelaskan oleh data issue dan adjustment/reconciliation, bukan sekadar volume transaksi harian. Ini memperkuat problem diagnosis di deck: bottleneck utama bukan hanya aktivitas transfer, tetapi kualitas data dan proses pengecekan sebelum transfer.

## Statistical Validation

Analisis menggunakan daily observation sebagai unit analisis. Periode dibagi menjadi:

- **Before automatic:** `2025-08-21` sampai `2026-03-11`, `n = 138`.
- **After automatic:** `2026-03-12` sampai `2026-05-29`, `n = 55`.

Validation approach:

- **Permutation test** untuk menguji apakah perbedaan before vs after mungkin terjadi jika label periode diacak.
- **Bootstrap confidence interval** untuk memperkirakan range dampak rata-rata.
- **Correlation test via permutation** untuk menguji hubungan lead time dan adjustment rate sebelum automatic.

Results:

| Test | Result | Interpretation |
|---|---:|---|
| Lead time mean difference | `-1.73h`, p `< 0.001` | Statistically strong reduction |
| Lead time 95% bootstrap CI | `[-2.13h, -1.34h]` | Impact remains materially negative across resamples |
| Daily adjustment-rate difference | `-0.267 pp`, p `< 0.001` | Statistically strong reduction |
| Adjustment-rate 95% bootstrap CI | `[-0.360 pp, -0.183 pp]` | Improvement remains below zero across resamples |
| Lead time vs adjustment correlation before auto | `r = 0.65`, p `< 0.001` | Strong evidence that adjustment-heavy days finish later |

Important caveat:

- This is not a randomized experiment. The statistical result supports that the observed before-after difference is unlikely to be random noise in the daily control data, but causality should still be interpreted with project context.
- Data starts in August 2025, while the original deck baseline references earlier periods. This summary is therefore strongest as **control-period evidence** and **post-improvement validation**, not as the complete original baseline.

## Benefits Of The Project

### Operational Benefits

- **Faster disbursement completion:** average lead time reduced from `15.73h` to `14.00h`.
- **Predictable daily cutoff:** disbursement consistently completes at `14:00` after automation.
- **Reduced late-day work:** days finishing after `17:00` dropped from `24.6%` to `0%`.
- **Lower manual dependency:** fewer cases require adjustment/reconciliation intervention.
- **Cleaner handoff across Finance, Data, Operations, and System teams.**

### Customer And Business Benefits

- **Improved merchant trust:** more predictable settlement timing reduces uncertainty for clients.
- **Lower complaint risk:** fewer late or incorrect disbursement cases.
- **Better SLA credibility:** `14:00` automatic timing is easier to communicate and monitor.
- **Reduced operational firefighting:** teams spend less time handling avoidable exceptions.

### Control And Governance Benefits

- **Better process control:** the process moved from variable timing to a stable schedule.
- **Stronger data quality loop:** adjustment rate becomes a measurable signal for upstream issues.
- **Clearer accountability:** issue categories such as contract mapping, discount/MDR mismatch, refund handling, bank account changes, and PG registration can be assigned to specific owners.
- **Sustainable monitoring:** lead time and adjustment rate can now be used as control metrics.

### Strategic / Industry Perspective

From an operations and industrial engineering perspective, this project reduces classic process waste:

- **Waiting:** disbursement no longer waits until late afternoon or evening.
- **Rework:** adjustment and reconciliation effort declines.
- **Motion / manual handling:** bulk download, formatting, auto-email, and new engine improvements reduce repetitive manual steps.
- **Defects:** data issue categories are converted into controllable system/process improvements.
- **Variation:** automatic `14:00` removes weekday-driven variability.

This makes the project stronger than a simple automation story. It is a process capability improvement: the system becomes faster, more stable, easier to govern, and easier to scale.

## How To Sell This Project

Use this positioning:

> "Auto Disburse converted a semi-manual disbursement workflow into a controlled operating process. The result was not only faster disbursement, but a statistically validated reduction in lead-time variation and adjustment-related rework. The data shows that adjustment-heavy days were the days that finished late; after automation, the process consistently hit 14:00 and adjustment rate fell by more than 80%."

Recommended proof points:

- `1.73h` average lead-time reduction.
- `0%` days after `17:00` in the automatic period.
- `82%` relative reduction in total adjustment rate.
- `r = 0.65` correlation between lead time and adjustment rate before automatic.
- `p < 0.001` for before-after improvements using permutation tests.

## Source And Data

- Project context: [[01 - OKR Automate Disbursement Deck Context]]
- Extraction source: [[deck_extraction]]
- Recap workbook: `/Users/ahmadreza/Documents/1. Projects/Auto Disburse Project/outputs/auto-disburse-recap/Rekap Lead Time Disbursement.xlsx`
- Statistics CSV: [[impact_statistics.csv]]

