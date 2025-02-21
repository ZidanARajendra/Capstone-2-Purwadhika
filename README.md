# **AWS SaaS Sales Analysis**

## **Deskripsi Proyek**

Proyek ini bertujuan untuk menganalisis data penjualan dari berbagai layanan Software-as-a-Service (SaaS) yang di-host menggunakan Amazon Web Services (AWS). Dataset mencakup informasi terkait berbagai aspek operasional SaaS seperti jumlah pelanggan, pendapatan, dan metrik kinerja lainnya. Tujuan utama dari proyek ini adalah untuk memahami dampak pandemi COVID-19 terhadap profitabilitas perusahaan dengan membandingkan profit selama masa pandemi (2020–2021) dan pasca-pandemi (2022–2023).

---

## **Tujuan Analisis**

1. **Memahami Dampak Pandemi pada Profitabilitas**  
   - Mengetahui apakah ada perbedaan signifikan dalam pola pembelian pelanggan dan profitabilitas antara periode pandemi dan pasca-pandemi.
   - Mengidentifikasi faktor-faktor yang memengaruhi performa perusahaan selama pandemi dan bagaimana perubahan tersebut terjadi setelah pandemi.

2. **Mengembangkan Strategi untuk Masa Depan**  
   - Memberikan rekomendasi strategis berdasarkan pola yang ditemukan untuk membantu perusahaan menyusun strategi menghadapi situasi serupa di masa depan.

3. **Analisis Berdasarkan Berbagai Dimensi**  
   - Melakukan analisis berdasarkan **Industri**, **Segment**, **Produk**, **Region**, dan **Subregion** untuk menemukan tren dan pola spesifik yang memengaruhi profitabilitas.

---

## **Dataset**

Dataset yang digunakan mencakup informasi berikut:

| **Kolom**         | **Deskripsi**                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Row ID             | Pengenal unik untuk setiap transaksi.                                        |
| Order ID           | Pengenal unik untuk setiap pesanan.                                          |
| Order Date         | Tanggal ketika pesanan dilakukan.                                            |
| Contact Name       | Nama orang yang melakukan pesanan.                                           |
| Country            | Negara tempat pesanan dilakukan.                                             |
| City               | Kota tempat pesanan dilakukan.                                               |
| Region             | Wilayah tempat pesanan dilakukan.                                            |
| Subregion          | Subwilayah tempat pesanan dilakukan.                                         |
| Customer           | Nama perusahaan yang melakukan pesanan.                                      |
| Customer ID        | Pengenal unik untuk setiap pelanggan.                                        |
| Industry           | Industri tempat pelanggan berada.                                            |
| Segment            | Segmen pelanggan (SMB, Strategic, Enterprise).                               |
| Product            | Produk yang dipesan.                                                         |
| License            | Kunci lisensi untuk produk.                                                  |
| Sales              | Jumlah total penjualan untuk transaksi.                                      |
| Quantity           | Jumlah total barang dalam transaksi.                                         |
| Discount           | Diskon yang diterapkan pada transaksi.                                       |
| Profit             | Keuntungan dari transaksi.                                                   |

---

## **Fitur Utama Analisis**

1. **Pengelompokan Data Berdasarkan Periode**  
   - Data dibagi menjadi dua periode: **Pandemi (2020–2021)** dan **Pasca-Pandemi (2022–2023)**.

2. **Visualisasi Data**  
   - Menggunakan grafik seperti **Histogram**, **Pie Chart**, dan **Bar Chart** untuk memvisualisasikan distribusi profit, persentase profit, dan tren pertumbuhan.

3. **Uji Hipotesis Statistik**  
   - Melakukan uji statistik seperti **Z-Test** dan **Chi-Square Test** untuk menentukan apakah perbedaan profit antar periode atau kategori signifikan secara statistik.

4. **Analisis Berdasarkan Dimensi**  
   - **Industri**: Membandingkan profitabilitas berdasarkan industri seperti Finance, Consumer Products, dan Tech.  
   - **Segment**: Menganalisis profitabilitas berdasarkan segmen pelanggan seperti SMB, Strategic, dan Enterprise.  
   - **Produk**: Mengidentifikasi produk dengan pertumbuhan profit tertinggi dan terendah.  
   - **Region/Subregion**: Membandingkan performa region seperti AMER, EMEA, dan APJ serta subregion di dalamnya.

5. **Rekomendasi Strategis**  
   - Memberikan rekomendasi berdasarkan temuan analisis untuk meningkatkan profitabilitas di masa depan.

---

## **Cara Menggunakan Program**

### **Prasyarat**
- Pastikan Anda memiliki Python versi 3.x terinstal di sistem Anda.
- Instal modul yang diperlukan dengan menjalankan perintah berikut:
  ```bash
  pip install pandas numpy matplotlib seaborn plotly statsmodels scipy
  ```

### **Langkah-langkah Penggunaan**

1. **Muat Dataset**  
   Muat dataset `SaaS-Sales.csv` ke dalam program menggunakan `pandas`:
   ```python
   df = pd.read_csv("SaaS-Sales.csv")
   ```

2. **Jalankan Analisis**  
   Jalankan skrip analisis untuk menghasilkan visualisasi dan hasil statistik:
   ```python
   python nama_file.py
   ```

3. **Simpan Hasil**  
   Hasil analisis dapat disimpan ke file CSV untuk referensi lebih lanjut:
   ```python
   df.to_csv('Saas-Sales-Final.csv', index=False)
   ```

---

## **Insight Utama**

1. **Pola Industri**  
   - Sektor **Consumer Products**, **Finance**, **Tech**, dan **Retail** menunjukkan peningkatan profit signifikan pasca-pandemi.  
   - Sektor **Communications** adalah satu-satunya industri yang mengalami penurunan profit.

2. **Pola Segment**  
   - Segmen **Strategic** mencatat peningkatan profit tertinggi secara persentase.  
   - Semua segmen menunjukkan peningkatan profit sehat antara 45% hingga 70%.

3. **Pola Produk**  
   - Produk **Alchemy** dan **One View** menunjukkan pertumbuhan profit luar biasa (>160%).  
   - Produk **Big Ol Database** mengalami penurunan profit drastis (98.86%).

4. **Pola Region**  
   - Region **AMER** menjadi pemegang profit tertinggi dengan total profit $85,645.88.  
   - Region **APJ** menunjukkan pemulihan terkuat dengan peningkatan profit 1370%.

---

## **Keunggulan Program**

- **Visualisasi Interaktif**: Menggunakan library seperti `matplotlib`, `seaborn`, dan `plotly` untuk menghasilkan grafik yang informatif dan mudah dipahami.  
- **Analisis Mendalam**: Melibatkan uji hipotesis statistik untuk mendukung temuan analisis.  
- **Rekomendasi Strategis**: Memberikan saran praktis berdasarkan hasil analisis untuk membantu pengambilan keputusan bisnis.

---

Terima kasih telah menggunakan **AWS SaaS Sales Analysis**! Kami harap proyek ini dapat membantu Anda memahami dampak pandemi pada profitabilitas dan merencanakan strategi bisnis yang lebih baik. 😊
