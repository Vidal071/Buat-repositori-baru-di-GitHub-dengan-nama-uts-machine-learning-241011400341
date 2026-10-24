# UTS Machine Learning - Linear & Logistic Regression

**Identitas Mahasiswa:**
- **Nama:** Moh Pidal Mudrika
- **NIM:** 241011400341
- **Kelas:** Reg C
- **Random State:** 41 (menggunakan 2 digit terakhir NIM)

---

## 📌 Deskripsi Tugas
Tugas UTS ini mengimplementasikan algoritma **Linear Regression** dan **Logistic Regression** secara mandiri menggunakan **NumPy** (tanpa menggunakan library `scikit-learn` untuk pembuatan model utama dan metrik evaluasi).

---

## 📊 Ringkasan Hasil Model

### A. Bagian A – Linear Regression (`Ads_Data.csv`)
* **Persamaan Garis Regresi (Normal Equation):**
  $$\hat{y} = b + m \cdot X$$
* **Metrik Evaluasi Data Testing:** *(Ganti dengan angka hasil running dari notebook kamu)*
  - **MAE:** ...
  - **MSE:** ...
  - **RMSE:** ...
  - **R² Score:** ...

* **Kesimpulan Eksperimen Learning Rate (Gradient Descent):**
  - **`0.001`**: Konvergensi berjalan terlalu lambat karena langkah iterasi terlalu kecil.
  - **`0.02`**: Sangat pas dan stabil, berhasil konvergen mendekati hasil *Normal Equation*.
  - **`0.1`**: Terjadi *overflow* / divergen karena nilai *step* terlalu besar sehingga melompati titik minimum.

---

### B. Bagian B – Logistic Regression (`Email_Data.csv`)
* **Persamaan Probabilitas Spam:**
  $$P(\text{Spam}) = \sigma(b + m_1 \cdot \text{JumlahLink} + m_2 \cdot \text{KataPromo})$$

* **Metrik Evaluasi Data Testing (Threshold Default = 0.5):** *(Ganti dengan angka hasil running dari notebook kamu)*
  - **Accuracy:** ...
  - **Precision:** ...
  - **Recall:** ...
  - **F1-Score:** ...

* **Rekomendasi Threshold:**
  - **Threshold Terpilih:** **`0.7`**
  - **Alasan:** Pada sistem filter email, kesalahan **False Positive (FP)** (email penting / pekerjaan terbuang ke folder spam) jauh lebih berbahaya dibanding **False Negative (FN)**. Threshold 0.7 menaikkan nilai *Precision* sehingga sistem jauh lebih selektif dan aman bagi pengguna[cite: 1].

---

## 📁 Struktur Repositori
```text
uts-machine-learning-241011400341/
├── README.md            # Dokumentasi & Ringkasan Hasil UTS
├── tugas_UTS.ipynb      # Notebook berisi code & sel penjelasan lengkap (Run All)
├── Ads_Data.csv         # Dataset Biaya Iklan vs Penjualan
└── Email_Data.csv       # Dataset Prediksi Email Spam