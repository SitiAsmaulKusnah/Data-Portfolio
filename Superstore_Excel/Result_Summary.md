# Analisis Data Superstore Menggunakan Excel

## Deskripsi Proyek

Proyek ini bertujuan untuk melakukan analisis data penjualan dari Superstore menggunakan Excel. Data yang dianalisis mencakup transaksi penjualan, pengembalian barang, serta informasi terkait wilayah dan kategori produk. Analisis ini bertujuan untuk mengungkap pola yang membantu dalam pengambilan keputusan bisnis yang lebih efisien.

## Data Overview

Dataset terdiri dari beberapa sheet utama sebagai berikut:

### 1. **Orders**
Berisi informasi transaksi penjualan:
- `Row ID` : ID unik baris
- `Order ID`: ID unik untuk setiap transaksi.
- `Order Date`: Tanggal pemesanan.
- `Ship Date`: Tanggal pengiriman.
- `Ship Mode`: Metode pengiriman.
- `Customer ID & Name`: ID pelanggan.
- `Customer Name` : Nama pelanggan.
- `Segment`: Segmen produk.
- `Country`: Negara pelanggan.
- `State`: Negara bagian.
- `Postal Code`: Kode pos.
- `Region`: Wilayah Superstore yang diwakili.
- `Produk ID`: ID produk.
- `Category`: Kategori produk.
- `Sub Category`: Subkategori produk.
- `Produk Name`: Nama produk.
- `Sales`: Total penjualan dalam pesanan.
- `Quantity`: Total unit yang terjual.
- `Discount`: Diskon yang diterapkan produk dalam pesanan.
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
- Tidak ada tahun yang terlewat dalam dataset. Data mencakup seluruh periode 2014 hingga 2017.

### Q3: Berapa total penjualan dan keuntungan selama periode tersebut?
- Total Penjualan: $2.297.201
- Total Keuntungan: $286.397

### Q4: Apa tingkat margin keuntungan selama periode tersebut?
Margin keuntungan: 12,46%, menunjukkan bahwa bisnis ini cukup menguntungkan.

### Q5: Apa segmen yang memberikan kontribusi terbesar terhadap keuntungan pada tahun 2017?
- Segmen Consumer: $45.568,2391
- Segmen Corporate: $26.782,3633
- Segmen Home Office: $21.088,6672
- Hal ini menunjukkan bahwa Consumer memberikan kontribusi terbesar pada tahun 2017.

### Q6: Kategori dan subkategori produk mana yang paling signifikan dalam menghasilkan keuntungan pada tahun 2017?
- Kategori Technology menyumbang 54,24% dari total keuntungan dengan subkategori Copiers mencatatkan profit tertinggi sebesar 26,79%. Sebaliknya, subkategori machines mengakali kerugian hingga -3,07%.
- Kategori Supplies menyusul di posisi kedua dengan kontribusi 42,53% terhadap total profit. Subkategori Paper berperan dominan dengan sumbangan profit sebesar 12,89%, sedangkan Supplies mencatatkan kerugian hingga -1,02%.
- Kategori Furniture berada di posisi terakhir dengan kontribusi profit hanya 3,23%. Chairs menjadi subkategori yang paling menguntungkan dalam kelompok ini dengan kontribusi 8,18%, sementara Tables mengalami kerugian terbesar di antara semua subkategori, yakni -8,71%.

### Q7: Kapan terjadi lonjakan penjualan tertinggi?
- Tahun 2016 mengalami lonjakan penjualan sebesar 29,47% dibandingkan dengan tahun sebelumnya.

### Q8: Kategori mana yang berkontribusi terbesar terhadap lonjakan penjualan tahun 2016?
- Kategori Technology berkontribusi 39,06% terhadap lonjakan penjualan 2016.

### Q9: Berapa persen kontribusi kategori Technology di tahun 2016?
- Kategori Technology menyumbang 37,16% dari total penjualan di tahun 2016.

### Q10: Bagaimana distribusi penjualan berdasarkan kuartal?
- Kuartal dengan penjualan tertinggi: Q4 (Oktober–Desember).
- Kuartal dengan penjualan terendah: Q1 (Januari–Maret).

### Q11: Apa yang dapat diprediksi mengenai penjualan di masa depan?
- Model peramalan menunjukkan bahwa penjualan akan meningkat, meskipun dengan ketepatan rendah. Untuk prediksi jangka pendek, metode Moving Average lebih dianjurkan.

### Q12: Bagaimana distribusi nilai transaksi (Average Order Value/AOV)?
- Skewness: 7,01 (mengindikasikan distribusi miring ke kanan).
- Kurtosis: 78,5 (puncak distribusi sangat tajam).
- Hasil ini menunjukkan bahwa daata penjualan 2017 tidak terdistribusi secara normal.

### Q13: Siapa yang memiliki AOV tertinggi pada 2017, Chuck Magee atau Kelly Williams?
- Chuck Magee (East) memiliki AOV tertinggi sebesar 231,3604.
- Namun hasil t-test two sample assuming unequal variances menunjukkan bahwa tidak ada perbedaan yang signifikan antara order sales Chuck Magee (East) dengan Kelly Williams (Central).

## Kesimpulan
Berdasarkan hasil analisis:
- Tahun 2016 mencatatkan pertumbuhan signifikan, terutama didorong oleh kategori Technology.
- Penjualan cenderung musiman, dengan Q4 menjadi kuartal dengan penjualan tertinggi.
- Subkategori Tables dan Supplies perlu diperbaiki karena menunjukkan kerugian.
- Model peramalan yang lebih kompleks diperlukan untuk akurasi jangka panjang.

