# Catatan Singkat Preprocessing Machine Learning

## 1. **Binarisation (Binerisasi)**
Mengubah data numerik menjadi binary (0 atau 1) berdasarkan threshold tertentu.
- **Contoh**: Nilai < 0.5 → 0, Nilai ≥ 0.5 → 1
- **Gunakan kapan?**: Ketika hanya perlu klasifikasi sederhana (ya/tidak, ada/tidak ada)

## 2. **Normalization (Normalisasi)**
Mengubah skala data ke rentang tertentu (biasanya 0-1).
- **Rumus**: (x - min) / (max - min)
- **Gunakan kapan?**: Ketika fitur punya rentang yang sangat berbeda

## 3. **Standardization (Standarisasi)**
Mengubah data agar rata-rata = 0 dan standar deviasi = 1.
- **Rumus**: (x - mean) / std
- **Gunakan kapan?**: Algoritma yang sensitif terhadap skala (SVM, KNN, Neural Network)

## 4. **Label Encoding**
Mengubah kategori menjadi angka.
- **Contoh**: ['red', 'blue', 'green'] → [0, 1, 2]
- **Gunakan kapan?**: Untuk categorical data ordinal (ada urutan)

## 5. **One-Hot Encoding**
Mengubah kategori menjadi kolom binary.
- **Contoh**: 'red' → [1, 0, 0], 'blue' → [0, 1, 0], 'green' → [0, 0, 1]
- **Gunakan kapan?**: Untuk categorical data nominal (tidak ada urutan)

## 6. **Missing Value Handling**
Mengatasi data yang hilang/kosong.
- **Mean/Median Imputation**: Isi dengan rata-rata/median
- **Mode Imputation**: Isi dengan nilai yang paling sering muncul
- **Drop**: Hapus baris/kolom dengan missing value
- **Gunakan kapan?**: Selalu cek missing value sebelum training!

## 7. **Feature Scaling**
Menyamakan skala antar fitur agar model lebih optimal.
- Termasuk: Normalization & Standardization
- **Gunakan kapan?**: Hampir semua algoritma ML (kecuali Decision Tree/Random Forest)

## 8. **Feature Selection**
Memilih fitur yang paling penting untuk model.
- **Gunakan kapan?**: Ketika punya terlalu banyak fitur atau ingin mengurangi overfitting

## 9. **Outlier Handling**
Mengatasi data yang nilainya ekstrem/tidak wajar.
- **Metode**: IQR method, Z-score, atau remove outliers
- **Gunakan kapan?**: Ketika ada data yang sangat jauh dari data lainnya

## 10. **Data Splitting**
Membagi data menjadi train set dan test set.
- **Rasio umum**: 80:20 atau 70:30
- **Gunakan kapan?**: Selalu! Untuk evaluasi model yang objektif

---

## Quick Tips:
✅ **Urutan preprocessing**:
1. Handle missing values
2. Remove outliers (jika perlu)
3. Encoding categorical data
4. Feature scaling (normalization/standardization)
5. Split data (train/test)

✅ **Jangan lupa**: Preprocessing yang dilakukan di training set juga harus diterapkan ke test set!

✅ **Simpan scaler/encoder**: Agar bisa digunakan untuk data baru saat deployment
