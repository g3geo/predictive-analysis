# 📊 Total Expenditure Predictive Analysis
> **Analisis prediktif menggunakan Machine Learning untuk memprediksi pengeluaran pendidikan berdasarkan variabel finansial dan demografi siswa.**

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)

---

## 📌 Deskripsi Proyek
Proyek ini melakukan pemodelan statistik dan analisis data eksploratif untuk memprediksi `TOTAL_EXPENDITURE` (total pengeluaran) pada sektor pendidikan. Pipeline proyek ini mencakup pembersihan data mendalam, penanganan nilai hilang, seleksi fitur, hingga evaluasi performa model menggunakan algoritma Linear Regression dan Random Forest.

## 🛠️ Metodologi & Preprocessing
* **Pembersihan Data:** Menghapus kolom dengan nilai hilang $>60\%$ dan baris dengan nilai non-null $<50\%$ untuk menjaga kualitas data.
* **Imputasi Data:** Menggunakan `SimpleImputer` dengan strategi *mean* untuk menangani sisa *missing values* pada fitur numerik.
* **Seleksi Fitur:** Variabel yang digunakan meliputi `ENROLL`, `FEDERAL_REVENUE`, `STATE_REVENUE`, `LOCAL_REVENUE`, `SUPPORT_SERVICES_EXPENDITURE`, dan `OTHER_EXPENDITURE`.
* **Data Splitting:** Dataset dibagi menjadi 80% data latih dan 20% data uji dengan *random state* 42 untuk menjamin reproduksibilitas.

## ⚙️ Performa Model
Berdasarkan metrik evaluasi, model **Linear Regression** memberikan hasil yang paling akurat untuk dataset ini.

| Metrik | Linear Regression | Random Forest |
| :--- | :--- | :--- |
| **RMSE** | 513,325.30 | 564,650.65 |
| **MAE** | 223,281.03 | 259,672.82 |
| **$R^2$ Score** | 0.9979 | 0.9974 |
| **MAPE (%)** | 2.67% | 3.11% |

## 💡 Temuan Utama
* **Korelasi Terkuat:** Fitur `SUPPORT_SERVICES_EXPENDITURE` teridentifikasi sebagai prediktor utama dengan koefisien korelasi sebesar **0.9931**.
* **Generalisasi Model:** Selisih antara skor $R^2$ pada data latih dan data uji sangat kecil (0.0019), menunjukkan bahwa model memiliki kemampuan generalisasi yang sangat baik tanpa gejala *overfitting*.

## 🚀 Cara Penggunaan
1. Pastikan lingkungan Python Anda telah terinstal pustaka: `pandas`, `numpy`, `scikit-learn`, `matplotlib`, dan `seaborn` .
2. Gunakan dataset `states_all_extended.csv`.
3. Jalankan pipeline analisis mulai dari fase eksplorasi hingga evaluasi hasil.

---
**Dataset:** Total Expenditure Dataset (Education Finance Data)  
**Analisis Oleh:** Tim Data Science Rosbloks
