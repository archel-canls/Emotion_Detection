# Real-Time Emotion Recognition using Deep ANN 🧠🤖

Proyek ini adalah sistem deteksi emosi wajah secara *real-time* yang dibangun di atas arsitektur **Artificial Neural Network (ANN)**. Sistem ini mampu mengklasifikasikan 7 ekspresi manusia: Marah, Jijik, Takut, Senang, Sedih, Terkejut, dan Netral.

---

## 🚀 Fitur Utama

* **Deep Learning Architecture**: Menggunakan arsitektur ANN *Ultra-Capacity* dengan jutaan parameter untuk akurasi optimal.
* **Adaptive Preprocessing**: Implementasi **CLAHE** (Contrast Limited Adaptive Histogram Equalization) untuk memperjelas fitur wajah di berbagai kondisi cahaya.
* **Real-Time Stability**: Fitur **Smoothing** menggunakan *moving average* agar label emosi pada kamera stabil dan tidak berubah-ubah drastis.
* **Weighted Learning**: Menggunakan *Class Weights* untuk memprioritaskan akurasi pada emosi krusial seperti **Senang** dan **Terkejut**.

---

## 🛠️ Alur Kerja Sistem

1.  **Tahap 1: Pembangunan Database**
    Membaca dataset gambar, melakukan *Grayscale*, menerapkan *CLAHE*, dan mengubahnya menjadi format `pixels.csv`.
2.  **Tahap 2: Training Model (Deep Learning)**
    Melatih jaringan syaraf tiruan (ANN) menggunakan library **TensorFlow/Keras**. Arsitektur mencakup lapisan `Flatten`, `Dense` (2048, 1024, 512 unit), `BatchNormalization`, dan `Dropout`.
3.  **Tahap 3: Deteksi Kamera**
    Menggunakan **OpenCV** dan **Haar Cascade** untuk mendeteksi wajah, lalu melakukan prediksi emosi secara instan.

---

## 📦 Teknologi yang Digunakan

* **Bahasa**: Python
* **AI Framework**: TensorFlow & Keras
* **Computer Vision**: OpenCV
* **Data Analysis**: Pandas, Numpy, Scikit-learn

---

## 📋 Cara Menjalankan

Karena file model (`.keras`) dan database (`.csv`) memiliki ukuran besar (>200MB), silakan ikuti langkah berikut untuk mereproduksi sistem:

1.  **Clone Repository**:
    ```bash
    git clone [https://github.com/archel-canls/Emotion_Detection.git](https://github.com/archel-canls/Emotion_Detection.git)
    ```
2.  **Siapkan Dataset**: Pastikan folder `dataset/train` tersedia.
3.  **Jalankan Notebook**:
    * Eksekusi **Cell 1** untuk membangun database.
    * Eksekusi **Cell 2** untuk melatih model (menghasilkan `model_cerdas.keras`).
    * Eksekusi **Cell 3** untuk menyalakan kamera pendeteksi.

---

## 📊 Statistik Model
* **Input Layer**: 48x48 pixel (Grayscale)
* **Hidden Layers**: 4 Dense Layers dengan Batch Normalization
* **Output**: 7 Emotion Categories

---
**Author**: [Archel](https://github.com/archel-canls)  
**Project**: Sistem Cerdas - Artificial Intelligence Project
