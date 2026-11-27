# uts_DAM_werner3
# Analisis Spasial Pariwisata & Korelasi Parameter Cuaca Provinsi NTT

Proyek ini disusun untuk memenuhi tugas Ujian Tengah Semester (UTS) mata kuliah **Data Acquisition & Management (DAM)**. Proyek ini berfokus pada akuisisi data spasial pariwisata dan parameter cuaca di Provinsi Nusa Tenggara Timur (NTT) menggunakan sumber data riil yang terverifikasi serta mematuhi kaidah etika dan legalitas pengumpulan data.

## 👤 Identitas Mahasiswa
* **Nama:** Apolonia Werner
* **NIM:** `2501010151`
* **Mata Kuliah:** Data Acquisition & Management (DAM)
* **Repositori:** [uts_DAM_werner](https://github.com)

---

## 📊 Sumber Data Riil (Anti-Dummy)
Seluruh dataset dalam proyek ini diambil langsung dari sumber terbuka yang resmi dan kredibel tanpa menggunakan data buatan (*dummy*):

1. **OpenStreetMap (OSM):** Data titik koordinat dan atribut destinasi wisata di wilayah Provinsi NTT.
2. **Open-Meteo API:** Data parameter cuaca historis dan aktual (suhu, curah hujan, kelembapan, dan kecepatan angin) berdasarkan koordinat wilayah.
3. **Repositori Data Kode Wilayah Kemendagri:** Data referensi administratif resmi untuk pemetaan kabupaten/kota di Provinsi NTT.

---

## 🛡️ Kepatuhan Etis & Legalitas Akuisisi Data
Sebagai bentuk pertanggungjawaban akademik dan pemenuhan catatan evaluasi, proses akuisisi data telah melewati tahapan validasi berikut:

* **Uji Legalitas `robots.txt`:** Seluruh endpoint dan sumber pengambilan data telah diuji kepatuhannya terhadap protokol `robots.txt` dan dinyatakan lolos secara murni tanpa melanggar batasan akses server.
* **Kepatuhan 9 Butir Etika Data:** Proses pengumpulan, pembersihan, dan penyimpanan data telah mengikuti standar 9 Butir Etika Data (termasuk transparansi sumber, penghormatan *rate limit* API, tidak mengambil data pribadi sensitif, serta atribusi lisensi terbuka).

---

## 📁 Struktur Direktori Proyek

```text
uts_DAM_werner/
├── Data/                   # Dataset hasil akuisisi dan pembersihan (OSM, Open-Meteo, Kemendagri)
├── docs/                   # Dokumentasi proyek, bukti uji robots.txt, dan lampiran 9 Butir Etika Data
├── notebooks/              # Kode sumber Google Colab (.ipynb) untuk akuisisi & analisis spasial
└── README.md               # Dokumentasi utama repositori
```

---

## 🛠️ Teknologi & Pustaka yang Digunakan
* **Lingkungan Pengembangan:** Google Colaboratory (Python 3)
* **Akuisisi & Pemrosesan Data:** `pandas`, `requests`, `geopandas`
* **Analisis Spasial & Visualisasi:** `folium` / `matplotlib` / `seaborn`

---

## 🚀 Cara Menjalankan Proyek
1. *Clone* repositori ini ke komputer lokal Anda:
   ```bash
   git clone https://github.com.git
   ```
2. Buka file notebook (`.ipynb`) menggunakan **Google Colab** atau **Jupyter Notebook**.
3. Pastikan seluruh pustaka yang dibutuhkan telah terinstal, lalu jalankan sel kode secara berurutan.
