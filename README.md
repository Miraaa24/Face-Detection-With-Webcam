# Face Detection — UAS Praktikum Visi Komputer

**Perbandingan Metode Haar Cascade Baseline, Haar Cascade Improved, dan YuNet**

Proyek ini merupakan pengembangan dari proyek UTS Praktikum Visi Komputer yang sebelumnya menggunakan Haar Cascade Classifier untuk mendeteksi wajah secara *real-time* melalui webcam.

Pengembangan dilakukan untuk mengatasi keterbatasan deteksi pada posisi wajah tertentu, pencahayaan rendah, dan hasil kotak pembatas yang kurang sesuai.

## Anggota Kelompok 6

| No. | Nama Anggota | NPM |
|---|---|---|
| 1 | Almira Sadida | 2408107010004 |
| 2 | Hani Huriyah Ahmad | 2408107010020 |

**Mata Kuliah:** Praktikum Visi Komputer  
**Program Studi:** Informatika  
**Universitas:** Universitas Syiah Kuala  
**Tahun:** 2026

## Teknologi yang Digunakan

- **Python** — Bahasa pemrograman utama.
- **OpenCV** — Pengolahan citra dan deteksi wajah.
- **NumPy** — Pengolahan data numerik.
- **Pandas** — Pengolahan hasil evaluasi.
- **Matplotlib** — Visualisasi hasil pengujian.
- **Jupyter Notebook** — Lingkungan pengembangan program.

## Metode Deteksi Wajah

### 1. Haar Cascade Baseline
Metode deteksi wajah standar menggunakan model Haar Cascade frontal tanpa preprocessing tambahan.

### 2. Haar Cascade Improved
Pengembangan Haar Cascade dengan penambahan:
- Gamma Correction untuk menyesuaikan kecerahan citra.
- CLAHE untuk meningkatkan kontras lokal.
- Profile Cascade untuk mendeteksi wajah dari samping.
- Non-Maximum Suppression (NMS) untuk mengurangi kotak pembatas yang tumpang tindih.

### 3. YuNet
Metode deteksi wajah berbasis *deep learning* menggunakan model terlatih `face_detection_yunet_2023mar.onnx` dari OpenCV Zoo.

## Fitur Program

- Deteksi wajah secara *real-time* menggunakan webcam.
- Pemilihan tiga metode deteksi wajah.
- Menampilkan kotak pembatas dan jumlah wajah.
- Menampilkan FPS dan waktu pemrosesan.
- Menyimpan hasil deteksi.
- Evaluasi pada sembilan skenario pengujian.
- Visualisasi perbandingan hasil deteksi.

## Cara Menjalankan Program

1. Pastikan Python dan Jupyter Notebook sudah tersedia.
2. Instal library yang diperlukan:

   ```bash
   pip install opencv-contrib-python numpy pandas matplotlib notebook
   ```

3. Buka file menggunakan Jupyter Notebook atau VS Code.
4. Jalankan kode secara berurutan untuk memuat model dan fungsi deteksi.
5. Jalankan program deteksi wajah menggunakan webcam.

**Kontrol program:**

| Tombol | Fungsi |
|---|---|
| 1 | Haar Baseline |
| 2 | Haar Improved |
| 3 | YuNet |
| S | Menyimpan hasil deteksi |
| Q | Keluar dari program |

## Skenario Pengujian

Pengujian dilakukan pada sembilan kondisi:

1. Wajah frontal dengan pencahayaan baik.
2. Dua wajah menghadap kamera.
3. Wajah miring sekitar 15°.
4. Wajah menoleh sekitar 45°.
5. Wajah profil samping sekitar 90°.
6. Pencahayaan rendah.
7. Backlight.
8. Jarak jauh sekitar 2–3 meter.
9. Tanpa wajah.

**Kelompok 6 — UAS Praktikum Visi Komputer 2026**  
Program Studi Informatika, Universitas Syiah Kuala
