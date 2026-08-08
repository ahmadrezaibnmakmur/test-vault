# Konsep Waste Retail untuk Brand Procil

## Tujuan Catatan

Catatan ini membantu memahami konsep **waste** pada bisnis retail makanan, terutama untuk konteks **Brand Procil**, di mana proses masak dilakukan di outlet dan **1 kemasan bahan baku bisa menghasilkan beberapa produk jadi**.

Contoh sederhana:

- 1 kemasan bahan baku ayam marinasi = 1 kg
- Setelah dimasak di outlet, 1 kg tersebut bisa menjadi 5 porsi produk jadi
- Produk jadi dijual ke customer sebagai item retail
- Selisih antara stok bahan baku, hasil masak, produk terjual, dan sisa produk menjadi dasar perhitungan waste

---

## 1. Apa Itu Waste?

Dalam konteks retail makanan, **waste** adalah nilai atau kuantitas barang yang sudah menjadi beban bisnis tetapi tidak berhasil menjadi penjualan.

Waste bisa terjadi pada beberapa tahap:

1. **Waste bahan baku**
   - Bahan rusak, expired, tumpah, hilang, salah simpan, atau tidak bisa dipakai sebelum dimasak.

2. **Waste proses masak**
   - Shrinkage karena proses masak, gosong, salah masak, gagal produksi, atau hasil masak tidak sesuai standar.

3. **Waste produk jadi**
   - Produk sudah dimasak tetapi tidak terjual sampai batas waktu jual.

4. **Waste administrasi**
   - Stok fisik dan stok sistem berbeda karena salah input, salah konversi resep, salah satuan, atau transaksi tidak dicatat.

---

## 2. Kenapa Waste Brand Procil Lebih Kompleks?

Pada retail biasa, 1 barang masuk sering langsung sama dengan 1 barang jual.

Contoh retail sederhana:

- Beli 1 botol minuman
- Jual 1 botol minuman
- Kalau hilang 1 botol, waste = 1 botol

Namun di Brand Procil, ada proses produksi di outlet:

- Outlet menerima bahan baku
- Bahan baku dimasak
- Hasil masak menjadi beberapa produk jadi
- Produk jadi dijual satuan

Artinya, sistem harus memahami hubungan antara:

- **Bahan baku**
- **Resep atau konversi**
- **Produk jadi**
- **Yield hasil masak**
- **Waste**

---

## 3. Contoh Konversi Bahan Baku ke Produk Jadi

Misalnya Brand Procil punya produk:

**Produk Jadi:** Procil Chicken Rice Bowl

**Bahan baku utama:**

- 1 pack ayam marinasi = 1.000 gram

**Standar resep:**

- 1 porsi rice bowl menggunakan 200 gram ayam matang/setara porsi standar
- Maka 1 pack ayam marinasi secara standar menghasilkan 5 porsi

Rumus:

```text
Jumlah produk jadi standar = Qty bahan baku / kebutuhan bahan per porsi
```

Contoh:

```text
1.000 gram / 200 gram = 5 porsi
```

Jadi, dalam standar sistem:

```text
1 pack ayam marinasi = 5 porsi Procil Chicken Rice Bowl
```

---

## 4. Jenis Waste Berdasarkan Tahap Operasional

### A. Waste Sebelum Masak

Terjadi ketika bahan baku belum diproses.

Contoh:

- Ayam expired sebelum dimasak
- Plastik kemasan bocor
- Bahan jatuh ke lantai
- Bahan salah thawing
- Stok hilang saat opname

Pencatatan:

```text
Waste bahan baku = qty bahan baku yang tidak bisa dipakai
```

Contoh:

```text
1 pack ayam marinasi rusak
Waste = 1 pack
```

Dampak ERP:

- Stok bahan baku berkurang
- Biaya waste dicatat sebagai kerugian operasional
- Tidak ada produk jadi yang terbentuk

---

### B. Waste Saat Proses Masak

Terjadi saat bahan baku sudah dipakai untuk produksi tetapi hasilnya tidak sesuai standar.

Contoh:

- Ayam gosong
- Produk kurang matang dan tidak layak jual
- Salah bumbu
- Salah timing masak
- Output hanya 4 porsi, padahal standar 5 porsi

Contoh perhitungan:

```text
Standar: 1 pack = 5 porsi
Aktual hasil masak: 4 porsi layak jual
Selisih: 1 porsi
Waste proses = 1 porsi
```

Jika 1 pack ayam bernilai Rp50.000:

```text
Harga pokok per porsi standar = Rp50.000 / 5 = Rp10.000
Waste proses = 1 porsi x Rp10.000 = Rp10.000
```

Dampak ERP:

- Stok bahan baku berkurang 1 pack
- Produk jadi bertambah 4 porsi
- Waste proses dicatat 1 porsi atau senilai Rp10.000

---

### C. Waste Setelah Masak

Terjadi saat produk sudah jadi tetapi tidak terjual.

Contoh:

- Outlet memasak 5 porsi
- Terjual 3 porsi
- Sisa 2 porsi tidak boleh dijual lagi karena melewati batas holding time

Perhitungan:

```text
Produk jadi hasil masak = 5 porsi
Produk terjual = 3 porsi
Sisa tidak layak jual = 2 porsi
Waste produk jadi = 2 porsi
```

Jika HPP per porsi Rp10.000:

```text
Waste produk jadi = 2 x Rp10.000 = Rp20.000
```

Dampak ERP:

- Stok produk jadi berkurang karena dibuang
- Biaya waste produk jadi dicatat
- Gross margin outlet turun

---

## 5. Rumus Dasar Waste

### Waste Kuantitas

```text
Waste qty = Qty standar yang seharusnya tersedia - Qty aktual yang bisa dijual/terjual
```

Contoh:

```text
Standar hasil masak = 5 porsi
Aktual layak jual = 4 porsi
Waste qty = 1 porsi
```

### Waste Nilai Rupiah

```text
Waste value = Waste qty x HPP per unit
```

Contoh:

```text
Waste qty = 1 porsi
HPP per porsi = Rp10.000
Waste value = Rp10.000
```

### Waste Rate

```text
Waste rate = Waste value / Total HPP produksi
```

Contoh:

```text
Total HPP produksi = Rp50.000
Waste value = Rp10.000
Waste rate = 20%
```

---

## 6. Ilustrasi End-to-End

Asumsi:

- Outlet menerima 10 pack ayam marinasi
- 1 pack standar menghasilkan 5 porsi
- HPP 1 pack = Rp50.000
- HPP standar per porsi = Rp10.000

Maka potensi produk jadi:

```text
10 pack x 5 porsi = 50 porsi
```

Skenario aktual:

- 1 pack rusak sebelum dimasak
- 8 pack dimasak
- 1 pack masih tersisa sebagai stok bahan baku
- Dari 8 pack yang dimasak, standar output = 40 porsi
- Aktual hasil layak jual = 38 porsi
- Produk terjual = 35 porsi
- Sisa produk jadi expired = 3 porsi

Perhitungan waste:

| Jenis Waste | Perhitungan | Waste Qty | Waste Value |
|---|---:|---:|---:|
| Waste bahan baku | 1 pack rusak | 1 pack | Rp50.000 |
| Waste proses masak | Standar 40 porsi - aktual 38 porsi | 2 porsi | Rp20.000 |
| Waste produk jadi | 38 porsi - 35 porsi terjual | 3 porsi | Rp30.000 |
| **Total waste** |  |  | **Rp100.000** |

Total HPP bahan yang terkena waste:

```text
Rp50.000 + Rp20.000 + Rp30.000 = Rp100.000
```

---

## 7. Bagaimana Waste Dicatat di ERP?

ERP perlu mencatat waste sebagai transaksi stok dan transaksi biaya. Idealnya, ERP tidak hanya mengurangi stok, tetapi juga menyimpan alasan waste.

### A. Master Data yang Dibutuhkan

1. **Item bahan baku**
   - Contoh: Ayam Marinasi 1 kg
   - Satuan: pack atau gram
   - HPP: Rp50.000 per pack

2. **Item produk jadi**
   - Contoh: Procil Chicken Rice Bowl
   - Satuan: porsi
   - HPP standar: Rp10.000 per porsi

3. **Bill of Material atau Recipe**
   - 1 pack ayam marinasi menghasilkan 5 porsi
   - Atau 200 gram ayam per porsi

4. **Waste reason**
   - Expired
   - Rusak
   - Gosong
   - Salah masak
   - Tidak terjual
   - Selisih stock opname
   - Trial/training

5. **Outlet/location**
   - Waste harus tercatat per outlet agar bisa dianalisis.

---

### B. Transaksi Saat Bahan Baku Diterima

Saat outlet menerima bahan baku:

```text
Debit stok bahan baku
Credit goods in transit / pembelian / inventory clearing
```

Contoh stok:

```text
Ayam Marinasi +10 pack
```

---

### C. Transaksi Saat Produksi/Masak

Saat outlet memasak 1 pack ayam:

```text
Stok bahan baku berkurang: -1 pack
Stok produk jadi bertambah: +5 porsi, jika hasil sesuai standar
```

Jika hasil aktual hanya 4 porsi:

```text
Stok bahan baku: -1 pack
Stok produk jadi: +4 porsi
Waste proses: +1 porsi atau Rp10.000
```

ERP perlu mencatat:

- Nomor transaksi produksi
- Outlet
- Shift
- Staff/PIC
- Bahan yang dikonsumsi
- Output produk jadi
- Selisih yield
- Alasan selisih

---

### D. Transaksi Saat Produk Dijual

Saat 1 porsi terjual:

```text
Stok produk jadi berkurang: -1 porsi
Revenue bertambah
COGS/HPP diakui
```

Contoh:

```text
Produk jadi -1 porsi
Penjualan +RpXX.XXX
HPP +Rp10.000
```

---

### E. Transaksi Saat Produk Jadi Dibuang

Jika produk jadi tidak terjual dan harus dibuang:

```text
Stok produk jadi berkurang
Biaya waste bertambah
```

Contoh:

```text
Produk jadi -3 porsi
Waste produk jadi +Rp30.000
Reason: tidak terjual / expired holding time
```

ERP sebaiknya membuat dokumen:

```text
Waste Adjustment / Inventory Write-Off
```

Isi dokumen:

- Tanggal
- Outlet
- SKU
- Qty waste
- UOM
- HPP/unit
- Total nilai waste
- Reason code
- Catatan
- Approval, jika melewati threshold

---

## 8. Model Pencatatan ERP yang Disarankan

### Pilihan 1: Waste Dicatat di Level Bahan Baku

Cocok jika ERP belum kuat mengelola produk jadi hasil masak.

Contoh:

```text
1 pack ayam dipakai
Terjual hanya 3 dari potensi 5 porsi
Waste dianggap setara 2/5 pack ayam
```

Perhitungan:

```text
2 porsi waste / 5 porsi standar = 0,4 pack
Waste bahan baku = 0,4 x Rp50.000 = Rp20.000
```

Kelebihan:

- Lebih sederhana
- Cocok untuk tahap awal

Kekurangan:

- Sulit tahu apakah waste terjadi saat masak atau setelah produk jadi
- Analisis operasional kurang detail

---

### Pilihan 2: Waste Dicatat di Level Produk Jadi

Cocok jika ERP memiliki proses produksi atau kitchen module.

Contoh:

```text
1 pack ayam dimasak menjadi 5 porsi
Produk jadi masuk stok: 5 porsi
Terjual: 3 porsi
Waste produk jadi: 2 porsi
```

Kelebihan:

- Lebih akurat untuk outlet
- Bisa membedakan waste proses dan waste tidak terjual
- Cocok untuk analisis per menu

Kekurangan:

- Butuh disiplin input produksi harian
- Butuh recipe/BOM yang rapi

---

### Pilihan 3: Hybrid

Ini biasanya paling realistis untuk Brand Procil.

Gunakan:

- Waste bahan baku untuk bahan rusak sebelum masak
- Waste proses untuk hasil masak kurang dari standar
- Waste produk jadi untuk produk yang sudah jadi tetapi tidak terjual

Dengan model ini, manajemen bisa tahu akar masalah:

- Apakah pemborosan karena overstock bahan?
- Apakah karena proses masak tidak konsisten?
- Apakah karena forecasting demand salah?
- Apakah karena produk sudah dimasak terlalu banyak?

---

## 9. Contoh Format Pencatatan Waste Harian

| Tanggal | Outlet | SKU | Tipe Waste | Qty | UOM | HPP/Unit | Total | Reason | Catatan |
|---|---|---|---|---:|---|---:|---:|---|---|
| 2026-07-13 | Outlet A | Ayam Marinasi | Bahan baku | 1 | pack | Rp50.000 | Rp50.000 | Expired | Tidak dipakai sebelum close |
| 2026-07-13 | Outlet A | Chicken Rice Bowl | Proses | 2 | porsi | Rp10.000 | Rp20.000 | Gosong | Batch pertama gagal |
| 2026-07-13 | Outlet A | Chicken Rice Bowl | Produk jadi | 3 | porsi | Rp10.000 | Rp30.000 | Tidak terjual | Lewat holding time |

---

## 10. KPI Waste yang Perlu Dipantau

### Waste Value

Total nilai waste dalam rupiah.

```text
Waste value = total qty waste x HPP per unit
```

### Waste Rate terhadap HPP

Mengukur waste dibanding total biaya produk.

```text
Waste rate = waste value / total COGS atau total HPP produksi
```

### Waste Rate terhadap Sales

Mengukur waste dibanding penjualan.

```text
Waste to sales = waste value / net sales
```

### Waste per Outlet

Membandingkan outlet mana yang paling tinggi waste-nya.

### Waste per Menu

Mendeteksi produk yang sering tidak habis atau sering gagal diproduksi.

### Waste Reason Mix

Melihat penyebab utama waste:

- Expired
- Tidak terjual
- Salah masak
- Selisih opname
- Rusak saat penyimpanan

---

## 11. Prinsip Penting untuk Brand Procil

1. **Pisahkan waste bahan baku dan waste produk jadi**
   - Karena akar masalahnya berbeda.

2. **Recipe/BOM harus jelas**
   - Tanpa standar konversi, ERP tidak bisa menghitung apakah output aktual normal atau tidak.

3. **Gunakan satuan yang konsisten**
   - Misalnya pack, gram, dan porsi harus punya relasi yang jelas.

4. **Catat reason code**
   - Waste tanpa alasan hanya menjadi angka, bukan insight.

5. **Bedakan shrinkage normal dan waste abnormal**
   - Penurunan berat karena masak bisa normal, tetapi gosong atau tidak terjual adalah waste operasional.

6. **Waste harus dicatat di hari yang sama**
   - Jika dicatat belakangan, data outlet bisa bias.

7. **ERP harus bisa menelusuri dari produk jadi ke bahan baku**
   - Agar margin per menu dan waste per bahan bisa dianalisis.

---

## 12. Ringkasan Praktis

Untuk Brand Procil, waste tidak cukup hanya dihitung dari barang yang dibuang. Waste perlu dilihat sebagai selisih antara:

```text
Bahan baku yang dikonsumsi
vs
Produk jadi standar yang seharusnya terbentuk
vs
Produk jadi aktual yang layak jual
vs
Produk yang benar-benar terjual
```

Model paling baik adalah:

```text
Bahan baku rusak sebelum masak -> waste bahan baku
Output masak kurang dari standar -> waste proses
Produk matang tidak terjual -> waste produk jadi
```

Di ERP, setiap waste harus mengurangi stok dan membentuk biaya, lengkap dengan:

- Outlet
- SKU
- Qty
- UOM
- HPP
- Total value
- Tipe waste
- Reason code
- Approval jika perlu

Dengan pencatatan seperti ini, Brand Procil bisa membedakan apakah masalah utama berasal dari pembelian bahan, penyimpanan outlet, proses masak, forecasting demand, atau disiplin pencatatan operasional.
