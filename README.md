# 📊 Analisis Sentimen Ulasan Polri Super App
**Metode: SVM & IndoBERT**

## 📌 Deskripsi
Proyek ini menganalisis sentimen ulasan pengguna aplikasi **Polri Super App** di Google Play Store untuk memahami persepsi publik dan mengidentifikasi permasalahan utama aplikasi. Analisis dilakukan menggunakan pendekatan **Machine Learning (SVM)** dan **Deep Learning (IndoBERT)**.

---

## 🎯 Tujuan
- Mengklasifikasikan sentimen ulasan (Positif, Netral, Negatif)
- Membandingkan performa SVM dan IndoBERT
- Menghasilkan insight teknis dan rekomendasi strategis

---

## 📂 Dataset
- Sumber: Google Play Store (web scraping)
- Bahasa: Indonesia  
- Rentang data: **1 tahun terakhir dari waktu pengambilan data**
- Pra-pemrosesan: cleaning, tokenization, stopword removal, stemming

---

## ⚙️ Metodologi
- **SVM (TF-IDF + Linear Kernel)**  
  Cepat, ringan, cocok untuk sistem real-time
- **IndoBERT (Fine-tuning)**  
  Unggul dalam Precision & Recall, memahami konteks bahasa

---

## 📈 Hasil Evaluasi
| Model | Accuracy |
|------|----------|
| SVM | 94.92% |
| IndoBERT | 94.72% |



## 🧠 Insight Utama
- Sentimen pengguna sangat terpolarisasi (sangat positif / negatif)
- Keluhan utama berasal dari masalah **Login, OTP, dan Verifikasi Wajah**
- Modul Registrasi/Login menjadi bottleneck utama akses layanan

---

## 🛠 Rekomendasi
- Perbaikan sistem OTP & alternatif verifikasi
- Implementasi AI untuk monitoring otomatis ulasan
- Fokus stabilitas sistem sebelum penambahan fitur baru

---

## 🛠 Tools
Python, Scikit-learn, PyTorch, IndoBERT, Pandas, Matplotlib

---

## 👤 Author
**Vito Sengka**  
_Data Science | NLP_
