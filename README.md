# 🥚 Klasifikasi Jenis dan Kesegaran Telur Berdasarkan Citra Digital

Proyek ini bertujuan untuk mengembangkan model yang mampu mengklasifikasikan **jenis dan tingkat kesegaran telur** (ayam, bebek, dan puyuh) berdasarkan **analisis citra digital**.  
Proses meliputi pengumpulan dataset citra, pra-pemrosesan, ekstraksi fitur, hingga pelatihan beberapa model **Convolutional Neural Network (CNN)**.

---

## 📂 Akses Dataset dan File Proyek

Seluruh dataset citra, file notebook, dan model asli yang digunakan dalam proyek ini dapat diakses melalui tautan berikut:

👉 [**Buka Folder Proyek di Google Drive**](https://drive.google.com/drive/folders/1idpvSD83f5X6ykcNeXoYZFFhFIUtD-JC)

---

## 🏗️ Struktur Proyek

Berikut adalah struktur direktori dan penjelasan file utama dalam proyek ini.

### 📁 Direktori / Folder

- **`Ekstraksi/`**  
  Berisi data hasil ekstraksi fitur dari citra telur dalam format `.csv`.  
  Fitur yang diekstraksi meliputi:
  - **GLCM (Gray Level Co-occurrence Matrix)**
  - **RGB Mean**
  - **Histogram RGB**

- **`Model/`**  
  Berisi file model `.h5` hasil dari proses pelatihan.  
  Terdapat 4 varian model yang dilatih:

  | Nama Model | Deskripsi |
  |-------------|------------|
  | **ModelCNN_3** | Klasifikasi jenis telur (3 label: ayam, bebek, puyuh) |
  | **ModelCNN_6** | Klasifikasi jenis dan kesegaran dasar (6 label: ayam segar/tidak segar, dst.) |
  | **ModelCNN_9** | Klasifikasi jenis dan tingkat kesegaran detail (9 label: ayam segar/kurang segar/tidak segar, dst.) |
  | **ModelCNN_Multi** | Klasifikasi multi-label untuk memprediksi jenis telur dan lama waktu penyimpanan secara terpisah |

---

### 📘 File Penting (Notebook & Dataset Index)

| File | Deskripsi |
|------|------------|
| **`01_Computer Vision.ipynb`** | Notebook utama yang mencakup seluruh alur kerja proyek: pra-pemrosesan, ekstraksi fitur, dan pelatihan `ModelCNN_3`. |
| **`02_ModelCNN_6.ipynb`** | Notebook khusus untuk melatih `ModelCNN_6`. |
| **`03_ModelCNN_9.ipynb`** | Notebook khusus untuk melatih `ModelCNN_9`. |
| **`04_ModelCNN_MultiLabel.ipynb`** | Notebook khusus untuk melatih `ModelCNN_Multi`. |
| **`05_EvaluasiModel.ipynb`** | Notebook untuk melakukan pengujian dan evaluasi performa model menggunakan data input baru. |
| **`dataset_index.csv`** | File indeks dataset berisi informasi path folder, nama file, jam pengambilan, dan label jenis telur. |

---

## 🧠 Ringkasan Teknologi yang Digunakan

- **Python 3.x**
- **TensorFlow / Keras** untuk pelatihan CNN  
- **OpenCV** dan **scikit-image** untuk pra-pemrosesan citra  
- **Pandas** dan **NumPy** untuk pengolahan data tabular  
- **Matplotlib / Seaborn** untuk visualisasi hasil

---

## 🚀 Cara Menggunakan

1. Clone repositori ini atau unduh folder proyek dari Google Drive.  
2. Buka salah satu notebook (misalnya `01_Computer Vision.ipynb`) di **Jupyter Notebook** atau **Google Colab**.  
3. Jalankan setiap sel sesuai urutan untuk mereplikasi hasil model.  
4. Simpan model hasil pelatihan di folder `Model/`.

---

## 📊 Hasil Sementara

- Model terbaik diperoleh pada varian **ModelCNN_9** dengan akurasi tertinggi untuk klasifikasi multi-level.  
- Hasil prediksi visual dapat divisualisasikan dengan confusion matrix dan grafik akurasi-loss.

---

## ✍️ Pengembang

Proyek ini dikembangkan sebagai bagian dari penelitian terkait **pengenalan objek berbasis citra digital** dengan fokus pada **klasifikasi telur** berdasarkan tingkat kesegaran dan jenisnya.

---

## 📚 Referensi

Koolagudi, S. G., Kumar, S. A., Ramana, K., Kumar, S. V. N. S., Soujanya, K. L. S., Madhuri, C. B., Suma, V., & Prasad, C. R. K. V. S. S. L. V. (2022). *Identification of plant-leaf diseases using a convolutional neural network.* **Wireless Personal Communications, 125**(3), 2451–2472.  

Manav. (2021, Mei). *Convolutional Neural Networks (CNNs) in Deep Learning.* **Analytics Vidhya.** Diakses pada 11 September 2025, dari [www.analyticsvidhya.com](https://www.analyticsvidhya.com/blog/2021/05/convolutional-neural-networks-cnn/)  

Jones, T. (2023, Februari 13). *How Long Do Eggs Last Before They Go Bad?* **Healthline.** Diakses pada 11 September 2025, dari [www.reallygreatsite.com](https://www.reallygreatsite.com)

---
💡 *Jika Anda ingin mengembangkan proyek ini lebih lanjut, silakan gunakan dataset dan model yang disediakan dengan mencantumkan referensi ke repositori ini.*

