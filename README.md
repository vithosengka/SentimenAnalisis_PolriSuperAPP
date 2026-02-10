# 📊 Analisis Sentimen Ulasan Pengguna Polri Super App  
**Menggunakan Support Vector Machine (SVM) dan IndoBERT**

## 📌 Deskripsi Proyek
Proyek ini bertujuan untuk menganalisis sentimen ulasan pengguna aplikasi **Polri Super App** yang tersedia di Google Play Store. Analisis dilakukan untuk memahami persepsi publik terhadap aplikasi serta mengidentifikasi permasalahan utama yang memengaruhi pengalaman pengguna.

Dua pendekatan Machine Learning digunakan dan dibandingkan:
- **Support Vector Machine (SVM)** berbasis TF-IDF
- **IndoBERT** (Pretrained Transformer untuk Bahasa Indonesia)

Hasil analisis tidak hanya berfokus pada performa model, tetapi juga menghasilkan **insight bisnis dan rekomendasi strategis** yang dapat digunakan sebagai dasar pengambilan keputusan.

---

## 🎯 Tujuan Proyek
- Mengklasifikasikan sentimen ulasan pengguna (Positif, Netral, Negatif)
- Membandingkan performa model Machine Learning klasik dan Deep Learning
- Mengidentifikasi akar masalah utama dalam pengalaman pengguna aplikasi
- Memberikan rekomendasi berbasis data untuk peningkatan kualitas layanan

---

## 📂 Dataset
- Sumber: **Google Play Store Reviews – Polri Super App**
- Bahasa: Indonesia
- Label Sentimen: Positif, Netral, Negatif
- Pra-pemrosesan:
  - Case folding
  - Tokenization
  - Stopword removal
  - Stemming (Bahasa Indonesia)



## ⚙️ Metodologi
### 1. Machine Learning (SVM)
- Representasi teks: **TF-IDF**
- Kernel: Linear
- Kelebihan:
  - Training sangat cepat (< 1 menit)
  - Ringan secara komputasi
  - Cocok untuk sistem real-time

### 2. Deep Learning (IndoBERT)
- Model: Pretrained IndoBERT
- Fine-tuning pada dataset ulasan
- Kelebihan:
  - Precision & Recall lebih stabil
  - Lebih baik dalam memahami konteks bahasa

---

## 📈 Evaluasi Model
Metrik evaluasi yang digunakan:
- Accuracy
- Precision
- Recall
- F1-Score

| Model     | Accuracy |
|-----------|----------|
| SVM       | 94.92%   |
| IndoBERT  | 94.72%   |

---

## 🧠 Kesimpulan & Insight

### 1️⃣ Evaluasi Performa Model (Teknis)
- **Efektivitas Tinggi**  
  Kedua model mencapai akurasi di atas 94%, menunjukkan bahwa sentimen ulasan Polri Super App sangat terpolarisasi (sangat positif atau sangat negatif).

- **Efisiensi vs Kompleksitas**
  - **SVM**: Cepat, ringan, dan sangat efisien → ideal untuk deployment real-time.
  - **IndoBERT**: Unggul dalam Precision dan Recall → lebih minim kesalahan fatal (False Positive).

- **Keputusan Akhir**
  Untuk kebutuhan saat ini, **SVM dengan Kernel Linear** dipilih sebagai model terbaik karena memberikan keseimbangan optimal antara **akurasi tinggi (~95%)** dan **biaya komputasi rendah**.

---

### 2️⃣ Diagnosis Masalah Aplikasi (Business Insight)
- **Kepuasan Pengguna Terpolarisasi**  
  Pengguna sangat puas saat aplikasi berjalan lancar, namun sangat kecewa ketika terjadi gangguan teknis dasar.

- **Akar Masalah Utama (Root Cause)**  
  Mayoritas sentimen negatif **bukan disebabkan oleh fitur layanan kepolisian**, melainkan oleh **masalah akses sistem**, dengan kata kunci dominan:
  - `OTP / Kode`
  - `Login / Daftar`
  - `Verifikasi Wajah`

- **Fitur Paling Rentan**  
  Modul **Registrasi & Login** memiliki rasio komplain tertinggi dan menjadi *bottleneck* utama karena menghalangi akses ke fitur lainnya.

---

### 3️⃣ Rekomendasi Strategis (Action Plan)

#### 🔴 Jangka Pendek (Prioritas Utama)
- **Perbaikan Gateway OTP**
  - Audit vendor SMS OTP
  - Tambahkan metode verifikasi alternatif (WhatsApp Official / Email)

#### 🤖 Implementasi AI Monitoring
Gunakan model sentimen sebagai sistem monitoring otomatis:
- **Ulasan Negatif** → Tiket prioritas ke Tim IT Support
- **Ulasan Positif** → Evaluasi kepuasan publik oleh Tim Humas

#### 🛠 Fokus Stabilitas Sistem
- Hentikan sementara pengembangan fitur baru
- Alokasikan resource untuk:
  - Stabilitas server
  - Perbaikan bug Login & Verifikasi Wajah  
  > ±80% keluhan berasal dari modul ini

---

## 🛠 Tools & Teknologi
- Python
- Scikit-learn
- PyTorch
- HuggingFace Transformers
- IndoBERT
- Pandas, NumPy, Matplotlib, Seaborn

---

## 🚀 Pengembangan Selanjutnya
- Aspect-Based Sentiment Analysis (ABSA)
- Deteksi sarkasme & bahasa gaul
- Deployment model sebagai REST API
- Dashboard monitoring sentimen real-time

---

## 👤 Author
**Vito Sengka**  
_Data Science Enthusiast | Machine Learning | NLP_

📌 Proyek ini dibuat untuk keperluan pembelajaran, penelitian, dan portofolio.
