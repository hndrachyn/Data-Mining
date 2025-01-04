

**Standarisasi** adalah teknik preprocessing data yang digunakan untuk mengubah nilai fitur dalam dataset agar memiliki skala tertentu. Biasanya, standarisasi dilakukan dengan menyesuaikan data sehingga memiliki **mean (rata-rata)** sebesar 0 dan **standar deviasi** sebesar 1. Proses ini penting untuk memastikan bahwa setiap fitur memiliki kontribusi yang sebanding terhadap model, terutama pada algoritma yang sensitif terhadap skala data, seperti algoritma berbasis gradient atau jarak.

### Rumus Standarisasi
Untuk setiap nilai \(x\) dalam fitur, standarisasi dilakukan dengan:
\[
z = \frac{x - \mu}{\sigma}
\]
- \(x\): nilai asli fitur
- \(\mu\): mean (rata-rata) dari fitur
- \(\sigma\): standar deviasi dari fitur

### Kegunaan Standarisasi
1. **Meningkatkan Kinerja Model**: Beberapa algoritma machine learning, seperti Logistic Regression, SVM, dan KNN, bekerja lebih baik dengan data yang distandarisasi karena mereka sensitif terhadap skala fitur.
   
2. **Mempercepat Konvergensi**: Pada algoritma optimasi seperti gradient descent, standarisasi membantu mempercepat proses pelatihan model karena data berada dalam skala yang lebih konsisten.

3. **Meningkatkan Akurasi Prediksi**: Standarisasi mencegah fitur dengan rentang nilai besar mendominasi perhitungan jarak atau parameter model.

4. **Mendukung Model yang Sensitif terhadap Skala**: Beberapa model, seperti Random Forest atau Decision Tree, tidak terlalu sensitif terhadap skala data, tetapi untuk algoritma berbasis jarak (misalnya, K-Means atau PCA), standarisasi menjadi sangat penting.

### Kasus dalam Prediksi Dataset BMKG
Dalam konteks kasus yang dijelaskan:
1. **Standarisasi yang disimpan**: Menggunakan parameter mean dan standar deviasi yang sama dari data saat training untuk standarisasi dataset BMKG. Ini memastikan konsistensi antara data training dan data baru yang akan diprediksi.

2. **Standarisasi baru**: Melakukan standarisasi ulang dengan menghitung ulang mean dan standar deviasi dari dataset BMKG. Meskipun ini menghasilkan hasil prediksi yang berbeda, model dapat menyesuaikan lebih baik dengan dataset baru karena standarisasi tersebut lebih cocok dengan distribusi data baru.

Perbedaan hasil prediksi menunjukkan pentingnya standarisasi yang konsisten dengan proses pelatihan model, meskipun dalam beberapa kasus, standarisasi baru bisa memberikan hasil lebih baik untuk dataset yang berbeda.
