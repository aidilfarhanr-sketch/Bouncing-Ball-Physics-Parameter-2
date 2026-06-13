# Simulasi Bola Memantul dengan Parameter 2

Proyek ini merupakan simulasi grafika komputer 2D yang menampilkan dua bola bergerak dan memantul di dalam sebuah area canvas. Simulasi dibuat menggunakan Python, NumPy, Matplotlib, dan Matplotlib Animation. Proyek ini menerapkan konsep dasar fisika gerak, gravitasi, gesekan lantai, deteksi tabrakan antar bola, pantulan pada batas layar, perubahan warna saat tumbukan, serta efek visual glow agar tampilan animasi terlihat lebih menarik.

## Identitas Proyek

- Nama Proyek: Simulasi Bola Memantul dengan Parameter 2
- Pembuat: Aidil Farhan Rares
- NIM: 2515090002
- Jenis Proyek: Simulasi Grafika Komputer 2D
- Bahasa Pemrograman: Python
- Platform: Jupyter Notebook / Google Colab

## Deskripsi Singkat

Simulasi ini menampilkan dua bola yang bergerak di dalam bidang 2D. Setiap bola memiliki posisi, kecepatan, radius, warna, dan koefisien restitusi. Bola akan dipengaruhi oleh gaya gravitasi sehingga bergerak ke bawah, kemudian memantul ketika menyentuh lantai, dinding, atau bola lainnya.

Ketika dua bola saling bertabrakan, sistem akan menghitung arah tumbukan menggunakan jarak Euclidean, normal vector, dan tangential vector. Setelah tabrakan terjadi, warna bola akan berubah secara bergantian untuk memberikan efek visual interaktif.

## Fitur Utama

- Simulasi bola memantul 2D.
- Dua bola dengan posisi dan kecepatan awal berbeda.
- Penerapan gravitasi pada gerak bola.
- Penerapan gesekan lantai menggunakan parameter 2.
- Deteksi tabrakan antar bola.
- Deteksi tabrakan dengan batas window.
- Koefisien restitusi untuk mengatur elastisitas pantulan.
- Perubahan warna bola saat terjadi tumbukan.
- Efek glow neon pada setiap bola.
- Background gradasi gelap agar animasi terlihat modern.
- Animasi berjalan langsung di Jupyter Notebook atau Google Colab.
- Kontrol animasi seperti play, pause, replay, dan frame slider.

## Teknologi yang Digunakan

- Python
- NumPy
- Matplotlib
- Matplotlib Animation
- IPython Display
- Jupyter Notebook / Google Colab

## Konsep yang Diterapkan

### 1. Grafika Komputer 2D

Proyek ini menggunakan canvas 2D dari Matplotlib sebagai ruang visual. Area simulasi dibatasi menggunakan koordinat X dan Y, sehingga objek hanya bergerak di dalam batas yang telah ditentukan.

### 2. Window dan Viewport

Batas tampilan simulasi diatur menggunakan:

- Sumbu X: 0 sampai 10
- Sumbu Y: 0 sampai 6

Pengaturan ini membuat simulasi memiliki area gerak yang jelas dan menjaga objek tetap berada di dalam layar.

### 3. Gravitasi

Gravitasi diterapkan sebagai vektor pada sumbu Y negatif. Hal ini membuat bola seolah-olah tertarik ke bawah pada setiap frame animasi.

```python
GRAVITY = np.array([0, -0.02])
```

### 4. Gesekan Lantai

Gesekan lantai menggunakan parameter 2 yang disesuaikan dengan ketentuan tugas. Gesekan ini membuat kecepatan bola berkurang ketika bola menyentuh lantai, sehingga gerak terlihat lebih realistis.

```python
FLOOR_FRICTION = 2
```

### 5. Koefisien Restitusi

Koefisien restitusi digunakan untuk mengatur tingkat pantulan bola setelah terjadi tabrakan. Semakin besar nilainya, semakin elastis pantulan bola.

```python
cor = 0.82
```

### 6. Deteksi Tabrakan Antar Bola

Tabrakan antar bola dihitung berdasarkan jarak antar pusat bola. Jika jarak antar pusat lebih kecil dari jumlah radius kedua bola, maka sistem menganggap terjadi tabrakan.

### 7. Perubahan Warna Saat Tabrakan

Setiap bola memiliki dua pilihan warna. Ketika terjadi tumbukan, warna bola akan berganti secara otomatis untuk menampilkan efek interaksi visual.

### 8. Efek Glow

Efek glow dibuat dengan menambahkan lingkaran transparan berukuran lebih besar di belakang bola utama. Efek ini membuat tampilan bola terlihat lebih hidup dan modern.

## Struktur File

```text
Simulasi-Bola-Memantul-Parameter-2/
│
├── Bola_memantul_parameter_2.ipynb
└── README.md
```

## Cara Menjalankan Proyek

### 1. Clone Repository

```bash
git clone https://github.com/username/Simulasi-Bola-Memantul-Parameter-2.git
```

### 2. Masuk ke Folder Proyek

```bash
cd Simulasi-Bola-Memantul-Parameter-2
```

### 3. Install Library yang Dibutuhkan

```bash
pip install numpy matplotlib ipython
```

### 4. Jalankan Notebook

Buka file notebook menggunakan salah satu platform berikut:

- Jupyter Notebook
- JupyterLab
- Google Colab
- Visual Studio Code dengan extension Jupyter

Kemudian jalankan semua cell dari awal sampai akhir.

## Cara Menjalankan di Google Colab

1. Buka Google Colab.
2. Upload file `Bola_memantul_parameter_2.ipynb`.
3. Pilih menu `Runtime`.
4. Klik `Run all`.
5. Animasi akan tampil langsung di output notebook.

## Output Program

Output dari proyek ini adalah animasi dua bola yang bergerak dan memantul di dalam canvas 2D. Bola akan:

- Bergerak mengikuti kecepatan awal.
- Dipengaruhi oleh gravitasi.
- Memantul ketika mengenai dinding.
- Memantul ketika menyentuh lantai.
- Berinteraksi ketika bertabrakan dengan bola lain.
- Mengalami perubahan warna setelah tumbukan.
- Menampilkan efek cahaya atau glow.

## Tampilan Visual

Proyek ini menggunakan tampilan visual dengan nuansa gelap dan efek neon. Background dibuat menggunakan gradasi warna agar animasi terlihat lebih modern. Setiap bola memiliki warna utama dan glow sehingga lebih mudah diamati saat bergerak.

## Tujuan Proyek

Tujuan dari proyek ini adalah untuk memahami penerapan konsep grafika komputer dan simulasi fisika sederhana menggunakan Python. Proyek ini juga memperlihatkan bagaimana objek 2D dapat dianimasikan, diberi efek visual, dan dikendalikan melalui perhitungan matematika sederhana.

## Manfaat Proyek

- Memahami dasar animasi frame-by-frame.
- Memahami konsep koordinat 2D.
- Memahami penerapan gravitasi dalam simulasi.
- Memahami deteksi tabrakan antar objek.
- Memahami perubahan posisi objek berdasarkan kecepatan.
- Memahami penggunaan Matplotlib untuk animasi.
- Meningkatkan pemahaman terhadap konsep grafika komputer.

## Library Import

```python
import numpy as np
import matplotlib.pyplot as plt
from matplotlib.animation import FuncAnimation
from IPython.display import HTML, display
```

## Catatan

Jika animasi belum muncul, lakukan beberapa langkah berikut:

1. Pastikan semua cell sudah dijalankan dari awal.
2. Restart kernel notebook.
3. Jalankan ulang menggunakan `Run All`.
4. Jika menggunakan Google Colab, pastikan output HTML animasi berhasil dimuat.

## Author

Aidil Farhan Rares  
NIM: 2515090002

## License

Proyek ini dibuat untuk kebutuhan pembelajaran dan tugas grafika komputer.
