---
type: project-context
created: 2026-06-19
project: Auto Rekon Online Food - MSI
source:
  - /Users/ahmadreza/Auto Rekon Online Food - MSI
tags:
  - project
  - msi
  - reconciliation
  - online-food
  - python
  - flask
  - excel-automation
  - operations
  - finance-ops
  - workflow-automation
  - portfolio-case
---

# Auto Rekon Online Food - MSI Project Context

## Summary

Project ini adalah aplikasi rekonsiliasi offline untuk membandingkan transaksi ERP dengan laporan settlement platform online food seperti GoFood, GrabFood, dan ShopeeFood.

Tujuan utamanya adalah membantu proses finance atau operations mengecek apakah nilai transaksi online food di ERP sudah sesuai dengan laporan dari masing-masing platform, per toko, per tanggal, dan per platform.

Project source berada di:

`/Users/ahmadreza/Auto Rekon Online Food - MSI`

## Problem

Proses rekonsiliasi transaksi online food biasanya memakan waktu karena data berasal dari beberapa sumber berbeda:

- File ERP penerimaan penjualan per tipe pembayaran.
- File ERP laporan transaksi penjualan.
- Laporan GoFood per outlet dan tanggal.
- Laporan GrabFood per outlet dan tanggal.
- Folder ShopeeFood yang disiapkan sebagai placeholder untuk pengembangan berikutnya.

Masalah operasional yang diselesaikan:

- Nama toko di ERP dan platform tidak selalu sama.
- File laporan tersebar berdasarkan platform dan tanggal.
- Tim perlu membandingkan nilai ERP vs platform secara konsisten.
- Transaksi yang hanya muncul di ERP atau hanya muncul di platform perlu terlihat jelas.
- Hasil rekonsiliasi perlu bisa diexport ke Excel agar mudah direview dan dibagikan.
- User non-teknis membutuhkan UI yang lebih mudah daripada menjalankan script terminal.

## Solution

Ahmad membangun tool rekonsiliasi berbasis Python yang bisa dijalankan dalam dua mode:

- CLI/offline engine melalui `rekon.py`.
- Web interface lokal berbasis Flask melalui `webapp/app.py`.

Tool ini membaca file Excel ERP dan platform, menstandarkan field transaksi, memetakan nama toko lintas sumber, melakukan matching transaksi, lalu menghasilkan summary dan detail rekonsiliasi.

Output utama:

- Rekap per toko per hari.
- Rekap per platform per toko.
- Detail transaksi.
- Daftar transaksi yang hanya ada di ERP.
- Daftar transaksi yang hanya ada di platform.
- File Excel hasil rekonsiliasi di folder `Hasil Rekon/`.

## User Workflow

High-level workflow:

1. User menaruh file ERP di folder `Download ERP/`.
2. User menaruh laporan platform di folder platform masing-masing:
   - `GoFood/<tanggal>/`
   - `Grabfood/<tanggal>/`
   - `ShopeeFood/<tanggal>/`
3. User menjalankan aplikasi web atau script CLI.
4. User memilih project folder dan range tanggal.
5. Aplikasi melakukan scan folder untuk membaca file yang tersedia.
6. Aplikasi memuat data ERP dan laporan platform.
7. Aplikasi melakukan rekonsiliasi berdasarkan toko, tanggal, platform, dan amount.
8. User melihat hasil di UI dalam bentuk stats, tab summary, tab platform, dan detail.
9. User export hasil rekonsiliasi ke Excel.

## Folder Structure

Struktur project utama:

- `rekon.py`: core reconciliation engine, loader data, matching logic, report generator, CLI runner.
- `webapp/app.py`: Flask web app, API endpoint, folder browser, mapping activation, export endpoint.
- `webapp/templates/index.html`: UI utama untuk scan folder, pilih tanggal, proses rekonsiliasi, tab hasil, dan export.
- `webapp/templates/config.html`: UI konfigurasi mapping toko.
- `store_mapping.json`: mapping nama toko antara ERP, GrabFood, dan GoFood Merchant ID.
- `Download ERP/`: tempat file ERP.
- `GoFood/`: laporan GoFood per tanggal.
- `Grabfood/`: laporan GrabFood per tanggal.
- `ShopeeFood/`: placeholder platform berikutnya.
- `Hasil Rekon/`: output Excel rekonsiliasi.
- `build.py`: build script cross-platform dengan PyInstaller.
- `build_windows.py`: build script khusus Windows.
- `installer/RekonOnlineFood.iss`: script Inno Setup untuk installer Windows.
- `Rekon Online Food.command`: launcher macOS.
- `Rekon Online Food.bat`: launcher Windows.
- `requirements.txt`: dependency Python.

## Data Sources

ERP files:

- `penerimaan_penjualan_per_tipe_pembayaran_*.xlsx`
- `Laporan Transaksi Penjualan *.xlsx`

Platform files:

- GoFood report Excel, dibaca dari folder `GoFood/<tanggal>/`.
- GrabFood report Excel, dibaca dari folder `Grabfood/<tanggal>/`.
- ShopeeFood belum ada loader aktif, tetapi struktur folder dan kolom summary sudah disiapkan.

Contoh periode data yang ada di project:

- 19 Mei 2026.
- 11 Juni 2026.

## Store Mapping

Project memakai `store_mapping.json` untuk menyatukan nama toko lintas sumber.

Setiap toko bisa punya beberapa identifier:

- `erp1`: nama toko di file ERP penerimaan.
- `erp2`: nama toko di file ERP transaksi.
- `display`: nama tampilan yang mudah dibaca.
- `grabfood_store`: nama toko di file GrabFood.
- `gof_merchant_id`: Merchant ID GoFood.

Contoh toko yang sudah dimapping:

- Bintara.
- Harapan Jaya.
- Mutiara Gading Timur (MGT).
- Muchtar Tabrani.
- Pekayon.
- Perumnas 1.
- Seroja.
- Wisma Asri.
- Wisma Jaya.
- Jati Makmur.
- Rawa Kalong.
- Tanah Merdeka.
- Rawa Lumbu.
- Pasar Kecapi.
- Cilincing.
- Kayuringin.

Mapping ini penting karena nama outlet di ERP dan platform tidak selalu identik.

## Reconciliation Logic

Core matching ada di function `reconcile()` dalam `rekon.py`.

Matching dilakukan per platform dengan kriteria:

- Store folder sama.
- Tanggal transaksi sama.
- Amount sama.

Jika exact match tidak ditemukan, engine mencoba fuzzy amount match:

- Store sama.
- Tanggal sama.
- Selisih amount masih dalam tolerance.
- Tolerance adalah nilai terbesar antara 5% dari amount ERP atau Rp 5.000.

Hasil matching dibagi menjadi tiga kelompok:

- `matched`: transaksi ERP dan platform yang cocok.
- `unmatched_erp`: transaksi yang hanya muncul di ERP.
- `unmatched_platform`: transaksi yang hanya muncul di platform.

## Report Output

Excel output dibuat melalui `export_to_excel()`.

Sheet yang dihasilkan:

- `Rekap per Toko`: ringkasan per toko dan tanggal.
- `Rekap per Platform`: ringkasan per platform dan toko.
- `Detail Transaksi`: transaksi matched dan unmatched dalam satu tabel detail.
- `Hanya di ERP`: transaksi yang tidak punya pasangan di platform.
- `Hanya di Platform`: transaksi platform yang tidak punya pasangan di ERP.

Format file output:

`Hasil Rekon/Rekon_OnlineFood_<YYYYMMDD>.xlsx`

Jika range tanggal lebih dari satu hari:

`Hasil Rekon/Rekon_OnlineFood_<YYYYMMDD>-<YYYYMMDD>.xlsx`

## Web App

Web app berjalan lokal di:

`http://localhost:8080`

Endpoint utama:

- `GET /`: halaman rekonsiliasi.
- `GET /config`: halaman konfigurasi mapping toko.
- `GET /api/health`: health check aplikasi.
- `POST /api/browse`: folder browser.
- `POST /api/scan`: scan file ERP dan platform.
- `POST /api/rekon`: menjalankan rekonsiliasi dan mengembalikan JSON result.
- `POST /api/export`: export hasil ke Excel.
- `GET /api/config/mapping`: load mapping toko.
- `POST /api/config/mapping`: simpan mapping toko.

UI utama menyediakan:

- Input project folder.
- Browse folder.
- Tanggal awal dan tanggal akhir.
- Scan folder.
- Proses rekonsiliasi.
- Stats hasil rekonsiliasi.
- Tab rekap per toko.
- Tab GoFood.
- Tab GrabFood.
- Tab ShopeeFood.
- Tab detail.
- Tab hanya ERP.
- Tab hanya platform.

UI config menyediakan:

- Load mapping berdasarkan project folder.
- Search toko.
- Tambah toko.
- Edit mapping.
- Hapus mapping.
- Simpan semua mapping.

## Packaging And Distribution

Project sudah disiapkan agar bisa dipakai user tanpa menjalankan command teknis setiap kali.

Launcher:

- macOS: `Rekon Online Food.command`.
- Windows: `Rekon Online Food.bat`.

Build:

- `build.py` untuk build executable dengan PyInstaller.
- `build_windows.py` untuk build Windows `.exe`.
- `installer/RekonOnlineFood.iss` untuk membuat installer Windows dengan Inno Setup.

Dokumentasi build Windows ada di:

`installer/README_WINDOWS_BUILD.md`

Output Windows yang ditargetkan:

- `dist/RekonOnlineFood/RekonOnlineFood.exe`
- `dist/installer/RekonOnlineFoodSetup.exe`

## Commands

Menjalankan CLI untuk satu hari:

```bash
python3 rekon.py --start-date 2026-06-11 --end-date 2026-06-11
```

Menjalankan CLI dengan project path tertentu:

```bash
python3 rekon.py --project-path "/path/to/project" --start-date 2026-06-11 --end-date 2026-06-11
```

Menjalankan web app:

```bash
python3 webapp/app.py
```

Melihat status mapping Merchant ID GoFood:

```bash
python3 rekon.py --map-merchant
```

Auto-map Merchant ID GoFood:

```bash
python3 rekon.py --auto-map-merchant
```

Build Windows di mesin Windows:

```bat
py -m pip install -r requirements.txt pyinstaller
py build_windows.py
```

## Technical Notes

Dependency utama:

- Flask.
- pandas.
- openpyxl.
- PyInstaller untuk packaging.
- Inno Setup untuk installer Windows.

Beberapa detail implementasi penting:

- `activate_project_mapping()` di web app refresh global mapping di `rekon.py` agar mapping mengikuti project folder yang dipilih user.
- App membedakan bundled mode dan source mode dengan `sys.frozen` dan `sys._MEIPASS`.
- Saat app packaged, default project path diarahkan ke `~/Documents/Rekon Online Food`.
- Health check dipakai agar jika aplikasi sudah berjalan dan shortcut diklik lagi, browser cukup membuka instance yang sudah aktif.
- Upload file tidak dipakai; app membaca langsung folder lokal agar cocok dengan workflow operasional berbasis file Excel.

## Current Status

Sudah ada:

- Loader ERP penerimaan.
- Loader ERP transaksi.
- Loader GrabFood.
- Loader GoFood.
- Store mapping JSON.
- Merchant ID mapping untuk GoFood.
- Matching exact dan fuzzy amount.
- Summary per toko per hari.
- Summary per platform.
- Detail transaksi.
- Export Excel.
- Web UI lokal.
- Config UI untuk mapping toko.
- Launcher macOS dan Windows.
- Build Windows executable dan installer.

Masih bisa dikembangkan:

- Loader ShopeeFood aktif.
- Test otomatis untuk loader dan matching.
- Validasi schema file Excel sebelum proses.
- Better error messaging untuk kolom file yang berubah.
- Audit trail perubahan mapping toko.
- Export report dengan styling Excel yang lebih rapi.
- Rule matching yang lebih spesifik per platform jika fee, discount, atau settlement basis berbeda.
- Mode review manual untuk approve atau reject fuzzy match.

## Ahmad's Role

Ahmad membuat project ini sebagai workflow automation untuk operasi rekonsiliasi online food MSI.

Peran yang tercermin dari project:

- Memahami proses finance/operations berbasis file Excel.
- Menerjemahkan kebutuhan rekonsiliasi manual menjadi logic aplikasi.
- Mendesain struktur folder input dan output.
- Membuat data loader untuk beberapa format Excel.
- Mendesain mapping toko lintas sistem.
- Membuat matching engine transaksi.
- Membuat output summary dan detail yang bisa langsung direview.
- Membuat web UI lokal untuk user non-teknis.
- Menyiapkan packaging agar aplikasi bisa dipakai di Windows.

## Impact

Project ini membantu mengubah proses rekonsiliasi dari pekerjaan manual berbasis banyak file menjadi workflow yang lebih terstruktur:

- Data ERP dan platform dibaca otomatis.
- Perbedaan nama toko dinormalisasi.
- Transaksi matched dan unmatched langsung terlihat.
- Summary bisa dilihat per toko, tanggal, dan platform.
- Hasil bisa diexport ke Excel untuk review lanjutan.
- User bisa memakai UI lokal tanpa perlu memahami Python.

## Portfolio Positioning

Short version:

> Built a local Python and Flask reconciliation tool for MSI to compare ERP transactions against GoFood and GrabFood reports, normalize store mapping, identify matched and unmatched transactions, and export review-ready Excel reports.

Indonesian version:

> Saya membuat aplikasi rekonsiliasi online food untuk MSI menggunakan Python dan Flask. Aplikasi ini membaca file ERP, GoFood, dan GrabFood, menyamakan mapping toko, mencocokkan transaksi berdasarkan toko, tanggal, dan nominal, lalu menghasilkan rekap serta detail selisih dalam Excel.

## Skill Signals

- Python automation.
- Excel data processing with pandas and openpyxl.
- Finance operations reconciliation.
- Local web app development with Flask.
- File-based workflow automation.
- Data normalization and mapping.
- Transaction matching logic.
- Exception and edge-case handling.
- User-facing tool design for non-technical operators.
- Windows packaging with PyInstaller and Inno Setup.

## Potential LinkedIn Angles

- Rekonsiliasi bukan cuma compare angka, tetapi juga masalah mapping data lintas sistem.
- Banyak workflow finance bisa diautomasi tanpa harus membuat cloud app besar.
- Excel tetap bisa menjadi interface kerja, sementara Python menangani proses beratnya.
- Tool internal yang bagus harus mengikuti struktur folder dan kebiasaan kerja user.
- Matching fuzzy perlu dibuat hati-hati karena membantu proses review, tetapi tetap harus transparan.

## Related Notes

- [[00 - PARA Home|PARA Home]]
- [[02 Areas/Personal Branding Agent/11 - Ahmad Reza Career Profile|Ahmad Reza Career Profile]]
- [[02 Areas/Personal Branding Agent/13 - Ahmad Reza Skills and Achievement Inventory|Ahmad Reza Skills and Achievement Inventory]]
