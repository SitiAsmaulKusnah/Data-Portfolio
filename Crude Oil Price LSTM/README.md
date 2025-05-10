# Peramalan Harga Minyak Mentah Menggunakan Long Short-Term Memory (LSTM)

Harga minyak mentah merupakan salah satu indikator ekonomi global yang sangat kompleks dan fluktuatif. Pergerakannya dipengaruhi oleh berbagai faktor, seperti geopolitik, penawaran dan permintaan global, kebijakan produksi OPEC, serta ekonomi makro negara-negara besar. Sifatnya yang dinamis dan dampaknya yang luas, maka prediksi harga minyak menjadi sangat penting untuk dilakukan, baik bagi pelagu industri energi, investor, maupun pembuat kebijakan.
Di era data saat ini, pendekatan seperti model ARIMA sering kali belum cukup untuk menangkap pola non-linear yang terkandung dalam data historis harga minyak. Oleh karena itu, metode berbasis deep learning, khususnya Long Short-Term Memory (LSTM) dijadikan alternatif yang menjanjikan dalam peramalan deret waktu (time series forecasting).

## 📊 Dataset
- Sumber: Kaggle
- Periode Data: 1 Januari 1983 hingga 1 April 2025
- Fitur yang Digunakan: Harga minyak mentah per bulan
  
## 🔎 Metodologi
- Model
  
  Long Short-Term Memory (LSTM) merupakan salah satu modifikasi dari Recurrent Neural network (RNN) yang mampu menangani ketergantungan jangka panjang dalam data berurutan. LSTM mampu mengatasi masalah vanishing gradient yang sering terjadi pada RNN tradisional dengan memperkenalkan sel memori yang dapat menyimpan informasi dalam waktu yang lama.
  Arsitektur LSTM melibatkan sel memori yang dikontrol oleh tiga gate, input gate, forget gate, dan output gate.
  - Input gate: mengontrol informasi apa yang ditambahkan ke dalam sel memori
  - Forget gate: menentukan informasi apa yang dihapus dari sel memori
  - Output gate: mengontrol informasi apa yang dikeluarkan dari sel memori
Hal ini memungkinkan jaringan LSTM untuk secara selektif mempertahankan atau membuang informasi saat mengalir melalui jaringan yang memungkinkan mereka untuk mempelajari ketergantungan jangka panjang. Jaringan ini memiliki keadaan tersembunyi yang seperti memori jangka pendek. Memori ini diperbarui menggunakan input saat ini, keadaan tersembunyi sebelumnya, dan keadaan sel memori saat ini.
  Arsitektur LSTM memiliki struktur rantai yang berisi empat jaringan saraf dan blok memori yang berbeda yang disebut sel. Berikut adalah arsitektur model LSTM.
![image](https://github.com/user-attachments/assets/644db34b-3cf4-4b2c-917a-8f32397bf535)

    

- Langkah-langkah:
    - Preprocessing Data
    (Normalisasi data, pembentukan sequence, dan pembagian data latih dan uji)
  - Pembuatan Model LSTM
    (Arsitektur model, jumlah neuron, activation function, dll.)
  - Regularisasi
    (Penggunaan dropout untuk mengurangi overfitting)
  - Evaluasi Model
    (Menggunakan metrik RMSE, MAE, serta visualisasi prediksi vs aktual)Preprocessing Data
  
## 📈 Hasil Analisis
- Grafik
  - Plot Data Historis
  - Plot Loss Training & Validation
  - Plot Prediksi vs Aktual
    
- Tabel Metrik Evaluasi

- Analisis 
  - Apakah prediksi mendekati harga asli?
  - Apakah penggunaan regularisasi berhasil mengurangi overfitting pada model?
 
## ✅ Kesimpulan
Ringkasan apakah LSTM efektif.

Saran untuk pengembangan selanjutnya 
