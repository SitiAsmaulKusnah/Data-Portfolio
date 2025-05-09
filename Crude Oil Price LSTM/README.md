# Peramalan Harga Minyak Mentah Menggunakan Long Short-Term Memory (LSTM)

Harga minyak mentah merupakan salah satu indikator ekonomi global yang sangat kompleks dan fluktuatif. Pergerakannya dipengaruhi oleh berbagai faktor, seperti geopolitik, penawaran dan permintaan global, kebijakan produksi OPEC, serta ekonomi makro negara-negara besar. Sifatnya yang dinamis dan dampaknya yang luas, maka prediksi harga minyak menjadi sangat penting untuk dilakukan, baik bagi pelagu industri energi, investor, maupun pembuat kebijakan.
Di era data saat ini, pendekatan seperti model ARIMA sering kali belum cukup untuk menangkap pola non-linear yang terkandung dalam data historis harga minyak. Oleh karena itu, metode berbasis deep learning, khususnya Long Short-Term Memory (LSTM) dijadikan alternatif yang menjanjikan dalam peramalan deret waktu (time series forecasting).

## 📊 Dataset

## 🔎 Metodologi
- Model
  Long Short-Term Memory

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
