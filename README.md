# Product Review Sentiment Analysis

## 📌 Deskripsi Proyek

Proyek ini bertujuan untuk membangun model **Natural Language Processing (NLP)** dan **Machine Learning** yang mampu mengklasifikasikan ulasan pelanggan ke dalam tiga kategori sentimen:

* Positive
* Neutral
* Negative

Analisis sentimen dilakukan dengan memanfaatkan teknik pemrosesan teks, ekstraksi fitur menggunakan TF-IDF, serta beberapa algoritma Machine Learning untuk memahami opini pelanggan dan menghasilkan insight bisnis yang bermanfaat.

---

## 🎯 Tujuan Proyek

* Melakukan preprocessing terhadap data ulasan pelanggan.
* Mengubah data teks menjadi fitur numerik menggunakan TF-IDF.
* Membandingkan performa beberapa algoritma Machine Learning.
* Mengevaluasi performa model menggunakan berbagai metrik evaluasi.
* Menghasilkan insight bisnis berdasarkan sentimen pelanggan.

---

## 📂 Dataset

Dataset yang digunakan berisi ulasan pelanggan beserta rating produk.

### Fitur Utama

| Kolom        | Deskripsi                           |
| ------------ | ----------------------------------- |
| Rating       | Penilaian pelanggan terhadap produk |
| Review Title | Judul ulasan                        |
| Review Text  | Isi ulasan                          |

### Pembuatan Label Sentimen

Label sentimen dibuat berdasarkan rating pelanggan:

| Rating | Sentimen |
| ------ | -------- |
| 1 – 2  | Negative |
| 3      | Neutral  |
| 4 – 5  | Positive |

---

## ⚙️ Tahapan Proyek

### 1. Data Cleaning

* Menghapus missing values
* Menghapus data duplikat
* Menggabungkan Review Title dan Review Text

### 2. Text Preprocessing

* Lowercase Conversion
* URL Removal
* Number Removal
* Punctuation Removal
* Tokenization
* Stopword Removal
* Lemmatization

### 3. Feature Engineering

Menggunakan metode:

**TF-IDF Vectorization**

Parameter:

* Maximum Features = 10.000
* N-Gram Range = (1,2)

### 4. Machine Learning Modeling

Model yang digunakan:

* Naive Bayes
* Logistic Regression
* Linear Support Vector Machine (SVM)

### 5. Model Evaluation

Metrik evaluasi yang digunakan:

* Accuracy Score
* Balanced Accuracy
* Macro F1 Score
* Classification Report
* Confusion Matrix

---

## 📊 Distribusi Sentimen

Dataset memiliki distribusi kelas yang tidak seimbang (Class Imbalance):

| Sentimen | Persentase |
| -------- | ---------: |
| Negative |        68% |
| Positive |        27% |
| Neutral  |         4% |

Karena distribusi data tidak seimbang, evaluasi model tidak hanya menggunakan Accuracy, tetapi juga Balanced Accuracy dan Macro F1 Score agar hasil evaluasi lebih representatif.

---

## 🤖 Hasil Model

| Model               | Accuracy |
| ------------------- | -------: |
| Naive Bayes         |   90.09% |
| Logistic Regression |   91.37% |
| Linear SVM          |   91.13% |

### Model Terbaik

**Logistic Regression**

### Performa Model Terbaik

| Metric            |  Score |
| ----------------- | -----: |
| Accuracy          | 91.37% |
| Balanced Accuracy | 62.55% |
| Macro F1 Score    | 62.43% |

---

## 📈 Visualisasi

Proyek ini menghasilkan beberapa visualisasi:

* Sentiment Distribution
* Review Length Distribution
* Word Cloud
* Model Performance Ranking
* Confusion Matrix

Seluruh visualisasi otomatis disimpan dalam format PNG.

---

## 💡 Business Insights

Berdasarkan hasil analisis sentimen:

* Sebagian besar pelanggan memberikan ulasan negatif terhadap produk atau layanan.
* Tingginya jumlah ulasan negatif dapat menjadi indikator adanya masalah pada kualitas produk, layanan pelanggan, atau pengalaman pengguna.
* Ulasan positif menunjukkan bahwa sebagian pelanggan tetap merasa puas terhadap produk yang digunakan.
* Ulasan netral memiliki jumlah yang sangat sedikit sehingga model lebih sulit mengenali kategori tersebut.
* Analisis sentimen dapat membantu perusahaan memonitor persepsi pelanggan secara otomatis dan mendukung pengambilan keputusan berbasis data.

---

## 🛠️ Teknologi yang Digunakan

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* NLTK
* Scikit-Learn
* WordCloud
* Joblib

---

---

## 📋 Kesimpulan

Proyek ini berhasil membangun sistem klasifikasi sentimen berbasis NLP dan Machine Learning untuk mengelompokkan ulasan pelanggan ke dalam kategori Positive, Neutral, dan Negative.

Model Logistic Regression memberikan performa terbaik dengan Accuracy sebesar 91.37%. Namun, karena dataset memiliki distribusi kelas yang tidak seimbang, evaluasi juga dilakukan menggunakan Balanced Accuracy dan Macro F1 Score untuk memberikan gambaran performa model yang lebih adil dan representatif.

Hasil penelitian menunjukkan bahwa kombinasi TF-IDF dan Logistic Regression mampu memberikan performa yang baik dalam tugas klasifikasi sentimen serta dapat digunakan untuk membantu perusahaan memahami opini pelanggan secara lebih efisien.

Author

Briliant Vilendro Kastilong

Teknik Informatika

Universitas Mercu Buana
