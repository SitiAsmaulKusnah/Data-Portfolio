# Analisis Data Superstore Menggunakan Excel

## Deskripsi Proyek

Proyek ini bertujuan untuk melakukan analisis data penjualan dari Superstore menggunakan Excel. Data yang dianalisis mencakup transaksi penjualan, pengembalian barang, serta informasi terkait wilayah dan kategori produk. Analisis ini bertujuan untuk mengungkap pola yang membantu dalam pengambilan keputusan bisnis yang lebih efisien.

## Data Overview

Dataset terdiri dari beberapa sheet utama sebagai berikut:

### 1. **Orders**
Berisi informasi transaksi penjualan:
- `Order ID`: ID unik untuk setiap transaksi.
- `Order Date`: Tanggal pemesanan.
- `Ship Date`: Tanggal pengiriman.
- `Ship Mode`: Metode pengiriman.
- `Customer ID & Name`: ID dan nama pelanggan.
- `Sales`: Nilai total penjualan.
- `Profit`: Keuntungan dari transaksi.

### 2. **Returns**
Berisi informasi pengembalian barang:
- `Order ID`: ID pesanan yang dikembalikan.
- `Returned`: Status pengembalian (Ya/Tidak).

### 3. **People**
Berisi informasi wilayah dan supervisor:
- `Region`: Wilayah tempat transaksi.
- `Person`: Nama supervisor wilayah.

## Proses Penggabungan Data
Data dari sheet Orders, Returns, dan People digabungkan menggunakan fungsi VLOOKUP untuk mencocokkan data berdasarkan Order ID. Ini memungkinkan analisis yang lebih komprehensif mengenai transaksi, pengembalian, serta wilayah penjualan.

## Data Cleaning
### Langkah-langkah pembersihan data yang dilakukan:
- Identifikasi Missing Values: Tidak ditemukan nilai yang hilang dalam dataset.
- Pemeriksaan Data Duplikat: Data duplikat dihapus untuk memastikan keakuratan analisis.
- Normalisasi Format Tanggal: Format tanggal pada data dipastikan seragam untuk analisis waktu.

## Data Insights
Berikut adalah beberapa wawasan yang ditemukan dari dataset:

### Q1: Kapan transaksi pemesanan pertama dan terakhir terjadi?
- Transaksi pertama: 3 Januari 2014.
- Transaksi terakhir: 30 Desember 2017.

### Q2: Apakah ada data yang hilang selama beberapa tahun penuh?
Tidak ada tahun yang terlewat dalam dataset. Data mencakup seluruh periode 2014 hingga 2017.

### Q3: Berapa total penjualan dan keuntungan selama periode tersebut?
Total Penjualan: $2.297.201
Total Keuntungan: $286.397

### Q4: Apa tingkat margin keuntungan selama periode tersebut?
Margin keuntungan: 12,46%, menunjukkan bahwa bisnis ini cukup menguntungkan.

### Q5: Apa segmen yang memberikan kontribusi terbesar terhadap keuntungan?
Segmen Consumer: $45.568,2391
Segmen Corporate: $26.782,3633
Segmen Home Office: $21.088,6672

### Q6: Kategori produk mana yang paling signifikan dalam menghasilkan keuntungan?
Kategori Technology menyumbang 54,24% dari total keuntungan.
Kategori Furniture hanya menyumbang 3,23%, dengan subkategori Tables mengalami kerugian.

### Q7: Kapan terjadi lonjakan penjualan tertinggi?
Tahun 2016 mengalami lonjakan penjualan sebesar 29,47% dibandingkan dengan tahun sebelumnya.

### Q8: Kategori mana yang berkontribusi terbesar terhadap lonjakan penjualan tahun 2016?
Kategori Technology berkontribusi 39,06% terhadap penjualan 2016.

### Q9: Berapa persen kontribusi kategori Technology di tahun 2016?
Kategori Technology menyumbang 37,16% dari total penjualan di tahun 2016.

### Q10: Bagaimana distribusi penjualan berdasarkan kuartal?
Kuartal dengan penjualan tertinggi: Q4 (Oktober–Desember).
Kuartal dengan penjualan terendah: Q1 (Januari–Maret).

### Q11: Apa yang dapat diprediksi mengenai penjualan di masa depan?
Model peramalan menunjukkan bahwa penjualan akan meningkat, meskipun dengan ketepatan rendah. Untuk prediksi jangka pendek, metode Moving Average lebih dianjurkan.

### Q12: Bagaimana distribusi nilai transaksi (Average Order Value/AOV)?
Skewness: 7,01 (mengindikasikan distribusi miring ke kanan).
Kurtosis: 78,5 (puncak distribusi sangat tajam).

### Q13: Siapa yang memiliki AOV tertinggi pada 2017?
Chuck Magee (East) memiliki AOV tertinggi sebesar 231,3604.

## Kesimpulan
Berdasarkan hasil analisis:
- Tahun 2016 mencatatkan pertumbuhan signifikan, terutama didorong oleh kategori Technology.
- Penjualan cenderung musiman, dengan Q4 menjadi kuartal dengan penjualan tertinggi.
- Subkategori Tables perlu diperbaiki karena menunjukkan kerugian.
- Model peramalan yang lebih kompleks diperlukan untuk akurasi jangka panjang.

