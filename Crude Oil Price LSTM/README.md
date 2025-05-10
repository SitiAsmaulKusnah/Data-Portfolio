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
    - Pengecekan missing value dan data duplikat.
    - Konversi kolom date ke format datetime dan dijadikan index DataFrame.
    - Normalisasi menggunakan MinMaxScaler() agar skala data seragam.
    - Pembentukan sequence untuk input LSTM.
    - Pembagian data:
        - Train (1983-2018): Melatih model dari pola historis.
        - Validation (2019-2021): Tuning parameter dan evaluasi saat krisis (COVID-19).
        - Test (2022-2025): Mengukur performa model pada data terbaru.
      
  - Pembuatan Model LSTM
    (Arsitektur model, jumlah neuron, activation function, dll.)
  - Regularisasi
    Menggunakan dropout untuk mengurangi risiko overfitting pada model.
  - Evaluasi Model
    
    Evaluasi model dilakukan menggunakan data testing, yaitu data yang tidak digunakan saat proses pelatihan model. Tujuannya adalah untuk mengukur seberapa baik model mampu memprediksi data baru yang belum pernah dilihat sebelumnya. Dalam proyek ini, saya menggunakan dua metrik evaluasi utama:
    - MAE (Mean Absolute Error): Mengukur rata-rata selisih absolut antara nilai prediksi dan nilai aktual. Semakin kecil MAE, semakin akurat model.
    - RMSE (Root Mean Square Error): Mengukur akar dari rata-rata selisih kuadrat antara prediksi dan aktual. RMSE lebih sensitif terhadap kesalahan besar (outlier), sehingga memberikan gambaran seberapa besar deviasi prediksi dari nilai asli.
      
## 📈 Hasil Analisis
- Grafik
  - Plot Data Historis
    ![1-Data Crude Oil Price](https://github.com/user-attachments/assets/424a86d1-e13a-4470-b0e8-e40c52e88286)

  - Plot Loss Training & Validation
    - Plot tanpa regularisasi
      ![2-Train-Val-Loss](https://github.com/user-attachments/assets/4fa4eddc-f3a0-4e82-8983-aa5c9819fa45) 
    - Plot dengan regularisasi
     ![5-Train-Val-Loss-Regularization](https://github.com/user-attachments/assets/78e1862b-2acc-43a2-a04d-9e389b4e47f1)
    
  - Plot Prediksi vs Aktual
    - Plot tanpa regularisasi
    ![4-Prediction_vs_Actual_All](https://github.com/user-attachments/assets/b56278ef-38ad-4720-8a0d-64cde494f6a8)
    - Plot dengan regularisasi
    ![7-Prediction_vs_Actual_AllRegularization](https://github.com/user-attachments/assets/c7c171e4-64c0-4422-90d0-51112f2a82f3)

    
- Metrik Evaluasi
     
    | Model                      | MAE    | RMSE   |
    |----------------------------|--------|--------|
    | Tanpa Regularisasi (No Dropout) | 4.51  | 5.44  |
    | Dengan Regularisasi (Dropout)   | 5.18  | 6.71  |

- Analisis 
  - Apakah prediksi mendekati harga asli?
  - Apakah penggunaan regularisasi berhasil mengurangi overfitting pada model?
 
## ✅ Kesimpulan
Ringkasan apakah LSTM efektif.

Saran untuk pengembangan selanjutnya 
