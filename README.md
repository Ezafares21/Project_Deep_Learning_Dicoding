# Proyek Klasifikasi Gambar: Intel Image Classification - Dicoding

Proyek akhir untuk kelas Belajar Fundamental Deep Learning.
- Arsitektur: Transfer Learning menggunakan MobileNetV2
- Jumlah Kelas: 6 (Buildings, Forest, Glacier, Mountain, Sea, Street)

Repositori ini berisi proyek akhir untuk kelas **Belajar Fundamental Deep Learning** di Dicoding. Proyek ini berfokus pada pembangunan model klasifikasi gambar multi-kelas (*multiclass image classification*) menggunakan pendekatan *Transfer Learning* dengan arsitektur **MobileNetV2**, serta melakukan ekspor model ke berbagai format deployment.

---

## 📌 Ringkasan Proyek

* **Dataset**: Intel Image Classification (6 Kelas: `buildings`, `forest`, `glacier`, `mountain`, `sea`, `street`)
* **Arsitektur Model**: MobileNetV2 (Transfer Learning)
* **Format Output Model**: `SavedModel` (TensorFlow), `TensorFlow.js` (`.json`), dan `TensorFlow Lite` (`.tflite`)

---

## 📁 Struktur Repositori

```text
.
├── DL_Klasifikasi_Gambar_Reza.ipynb   # Notebook eksperimen & pelatihan model
├── requirements.txt                  # Dependensi library Python
├── saved_model/                      # Model format Keras / SavedModel
│   ├── fingerprint.pb
│   ├── saved_model.pb
│   └── variables/
├── tfjs_model/                       # Model format TensorFlow.js untuk deployment Web
│   ├── group1-shard1of3.bin
│   ├── group1-shard2of3.bin
│   ├── group1-shard3of3.bin
│   └── model.json
├── tflite/                           # Model format TF Lite untuk Mobile/Edge Devices
│   ├── label.txt
│   └── model.tflite
└── README.md                         # Dokumentasi proyek


🛠️ Langkah Eksperimen & Pemodelan
Pre-processing Data:

Melakukan pemisahan dataset (train dan validation set).

Menerapkan augmentasi gambar (rescaling, rotation, flip, dll.) untuk mencegah overfitting.

Arsitektur Model:

Memakai pretrained model MobileNetV2 sebagai feature extractor.

Menambahkan lapisan Dense, Dropout untuk regularisasi, dan lapisan Softmax untuk output 6 kelas.

Ekspor & Deployment Model:

SavedModel: Format standar TensorFlow untuk kebutuhan deployment server.

TFJS: Konversi model menggunakan tensorflowjs_converter agar siap diintegrasikan ke aplikasi berbasis Web.

TF Lite: Konversi model menggunakan TFLiteConverter untuk penggunaan di perangkat mobile / Android.

🚀 Cara Menjalankan Secara Lokal
1. Kloning Repositori
Bash
git clone [https://github.com/Ezafares21/Project_Deep_Learning_Dicoding.git](https://github.com/Ezafares21/Project_Deep_Learning_Dicoding.git)
cd Project_Deep_Learning_Dicoding
2. Instalasi Dependensi
Buat virtual environment (opsional) lalu instal library yang dibutuhkan:

Bash
pip install -r requirements.txt
3. Menjalankan Notebook
Buka dan jalankan file DL_Klasifikasi_Gambar_Reza.ipynb menggunakan Jupyter Lab / VS Code / Google Colab:

Bash
jupyter lab DL_Klasifikasi_Gambar_Reza.ipynb


👤 Penulis
Nama: Reza Al Pares

GitHub: @Ezafares21
