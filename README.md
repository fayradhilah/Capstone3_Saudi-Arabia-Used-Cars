# Saudi Arabia Used Car Price Prediction Project

## Overview

**Syarah.com** adalah aplikasi jual-beli mobil bekas bergaransi dan mobil baru secara *online* yang beroperasi di seluruh wilayah Kerajaan Arab Saudi. Aplikasi ini menghadirkan pengalaman transaksi yang nyaman dan andal, dengan layanan tambahan berupa pengiriman mobil langsung ke lokasi pelanggan, garansi satu tahun untuk mobil bekas, serta opsi pengembalian tanpa alasan dalam waktu 10 hari. Aplikasi ini melayani dua segmen pelanggan: 

1. **Penjual mobil bekas**: Menyediakan informasi mobil dan jadwal inspeksi untuk penentuan harga.  
2. **Pembeli mobil bekas dan baru**: Membayar uang muka yang dapat dikembalikan, dengan layanan pengiriman gratis dan garansi tambahan.

Sumber: [syarah.com](https://syarah.com/en/about-us)

---

## Problem Statement

Penentuan harga mobil bekas di Syarah.com saat ini mengandalkan metode inspeksi manual, yang memakan waktu dan berisiko menghasilkan estimasi harga yang tidak konsisten. Hal ini dapat:

- Menyebabkan penjual merasa dirugikan jika harga terlalu rendah.
- Mengurangi kepercayaan pembeli jika harga dinilai terlalu tinggi tanpa justifikasi.
- Menghambat efisiensi transaksi karena proses penentuan harga yang lambat.

Untuk mengatasi tantangan ini, diperlukan solusi yang dapat memberikan estimasi harga secara cepat, konsisten, dan transparan.

---

## Goals

Proyek ini bertujuan untuk membangun **model prediktif** berbasis *machine learning* untuk memperkirakan harga mobil bekas dengan akurasi tinggi, menggunakan data terkait seperti tahun produksi, jarak tempuh, kapasitas mesin, dan tipe transmisi. Model ini diharapkan dapat:

1. **Mengurangi Ketidak-konsistenan**  
   Memberikan estimasi harga yang stabil dan dapat diandalkan, menggantikan metode manual yang tidak konsisten.  

2. **Meningkatkan Efisiensi Transaksi**  
   Mempercepat proses jual-beli dengan estimasi harga yang transparan, sehingga memudahkan penjual dan pembeli.  

3. **Memberikan Referensi Andal**  
   Menjadi panduan yang jelas dan terpercaya bagi pengguna untuk pengambilan keputusan transaksi.  

4. **Menjaga Profit dan Kepuasan Pengguna**  
   Menjamin harga sesuai ekspektasi penjual, sekaligus mempertahankan profitabilitas Syarah.com.  

Model ini diharapkan dapat meningkatkan kepercayaan pengguna dan memperbaiki pengalaman transaksi di platform Syarah.com.

---

## Dataset

Dataset yang digunakan dalam proyek ini berisi informasi detail mengenai mobil bekas yang tersedia di platform Syarah.com. Dataset terdiri dari **5624 baris** dan **11 kolom**, dengan rincian sebagai berikut:

| **Kolom**       | **Deskripsi**                                                   |
|------------------|----------------------------------------------------------------|
| **Type**        | Jenis mobil bekas.                                             |
| **Region**      | Wilayah tempat mobil bekas ditawarkan untuk dijual.            |
| **Make**        | Nama perusahaan pembuat mobil.                                 |
| **Gear_Type**   | Jenis transmisi mobil bekas.                                   |
| **Origin**      | Asal mobil bekas.                                              |
| **Options**     | Opsi tambahan yang tersedia pada mobil bekas.                  |
| **Year**        | Tahun pembuatan mobil.                                         |
| **Engine_Size** | Ukuran mesin mobil bekas.                                      |
| **Mileage**     | Jarak tempuh mobil bekas.                                      |
| **Negotiable**  | Bernilai *True* jika harga dapat dinegosiasikan.               |
| **Price**       | Harga mobil bekas.                                             |

---

## Kesimpulan
1. Hasil Model:
Model XGBoost menunjukkan performa yang baik dengan mampu menangkap tren utama data, meskipun masih terpengaruh oleh outlier.

2. Distribusi Residual:
Analisis QQ Plot mengindikasikan distribusi residual yang tidak sepenuhnya normal, menunjukkan adanya bias yang perlu ditangani lebih lanjut.

3. Feature Importance:
Analisis menggunakan Feature Importance dan SHAP menunjukkan bahwa Engine_Size adalah fitur paling berpengaruh terhadap harga mobil bekas, diikuti oleh Year, Mileage, dan Options.

Model ini memberikan dasar yang baik untuk prediksi harga, tetapi langkah tambahan diperlukan, seperti penanganan outlier dan eksplorasi model alternatif, untuk memastikan hasil yang lebih optimal dan keputusan yang lebih valid.
