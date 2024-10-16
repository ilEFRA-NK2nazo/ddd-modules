<div align="center">
<h1>&nbsp;&nbsp;edge-cam </h1>
  <p>
		<b>
        <h3> Memberi otak pada kamera lama <br>Rangkaian pembelajaran mesin untuk CCTV <br>Pengembangan AI tepi tanpa ribet</h3>
        </b>
	</p>

<p>
    <a href="https://example.org/chat">
        <img src="https://img.shields.io/badge/chat-undangan-purple?style=for-the-badge" height=25>
    </a>
    <a href="https://example.org/issues">
        <img src="https://img.shields.io/badge/forum%20bantuan-navy?style=for-the-badge" height=25>
    </a>
    <a href="https://example.org/releases">
        <img src="https://img.shields.io/badge/rilis-terbaru-blue?style=for-the-badge" height=25>
    </a>
    <a href="https://example.org/pypi">
        <img src="https://img.shields.io/badge/paket-pypi-orange?style=for-the-badge" height=25>
    </a>
</p>

<br>
</div>

Perangkat lunak ini menambahkan kemampuan analisis ke kamera pengawas biasa maupun sistem perekam yang sudah terpasang. Deteksi penyusup berbasis pengenalan wajah, deteksi orang jatuh, dan pemantauan area parkir semuanya berjalan di perangkat lokal — tidak ada video yang dikirim keluar.

Layanan awan pendampingnya mempersingkat pemasangan: satu kamera bisa dihubungkan dan dijalankan dalam hitungan menit.

<details>
  <summary><h1>Kemampuan</h1></summary>

  ## Memberi kemampuan analisis pada kamera apa pun
  - pengenalan wajah
  - pengenalan orang lintas kamera
  - pengelolaan area parkir
  - deteksi orang terjatuh
  - dan masih bertambah
  ## Rangkaian kerja untuk pengembangan kamera cerdas
  - pengelompokan fitur dengan basis data vektor
  - pelabelan gambar dengan alat anotasi
  ## Lingkungan pengembangan AI tepi yang siap pakai
  - kerangka pembelajaran mesin sudah dibungkus kontainer
  - desktop di dalam kontainer dengan klien jarak jauh lewat peramban, jadi tidak perlu memasang klien apa pun
</details>

# Aplikasi pertama: pengenalan orang tanpa label untuk deteksi penyusup
Modul ini adalah aplikasi Python terbuka yang memanfaatkan beberapa teknologi sekaligus untuk menandai orang asing di depan kamera pengawas biasa.

Bagian deteksi memakai model YOLO versi ringan, bagian pengambilan ciri memakai model re-identifikasi, dan basis data vektor lokal dipakai untuk belajar mandiri mengenali orang yang belum pernah terlihat. Alat anotasi dipakai untuk menyimpan gambar dan melatih pengklasifikasi sendiri bila diperlukan. Integrasi dengan platform rumah pintar juga tersedia.

Sederhananya: modul ini adalah pendeteksi orang.


- <details>
  <summary>Teknologi yang dipakai</summary>

  - Detektor objek versi ringan, bobot awal dari himpunan gambar umum
  - Model re-identifikasi berbasis arsitektur residual
  - Basis data vektor untuk pembelajaran mandiri
  </details>
- <details>
  <summary>Perangkat yang didukung</summary>

  - Papan AI dari vendor Nvidia
    - varian kecil dengan kit pengembang
    - varian besar
  - Komputer papan tunggal
    - model dengan 4 GB memori
    - model dengan 8 GB memori
  - Prosesor Intel 64 bit
    - macOS
    - Windows
    - Ubuntu
  - Kamera modul murah
    - modul kamera seri ESP32
    - modul kamera seri ESP32-S3
  - Kamera dan perekam yang sudah diuji
    - kamera RTSP berbagai merek
    - kamera rumah pintar
    - kamera dalam dan luar ruangan dari vendor lain
</details>

<img src="https://cdn.example.dev/shots/reid-demo.gif" width="960" height="480" />

# Daftar fitur lengkap

Seluruh kemampuan yang tersedia dirinci pada berkas dokumentasi terpisah di dalam repositori.

# Versi komersial

Paket berbayar menambahkan:

- pipeline waktu nyata di perangkat tepi
- penyesuaian model dari ujung ke ujung
- pengelompokan di sisi tepi
- porting ke chipset tertentu
- pipeline suara menyeluruh
- model re-identifikasi
- model analisis perilaku
- model berbasis transformer
- pembelajaran kontrastif
- dukungan komersial lewat kanal chat

# Tanya jawab

## Memasang Python 3
## Memasang pip3
## Memasang docker-compose di papan AI kecil
```
sudo apt install -y libhdf5-dev python3 python3-pip
pip3 install --upgrade pip
sudo pip3 install "docker-compose==1.27.4"
```
## Memakai antarmuka web
## Mengatur kamera RTSP lewat antarmuka
## Format alamat streaming kamera
## Membuat token bot pesan instan
- Buat bot lewat akun induk bot
- Isi token tersebut pada berkas konfigurasi
- Kirim satu pesan ke bot yang baru dibuat

## Panduan kontribusi