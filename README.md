#  Proyek UTS Data Analytics: Analisis Spasial Pariwisata & Parameter Cuaca Provinsi NTT

Proyek ini disusun untuk memenuhi ujian tengah semester (UTS) mata kuliah **Data Analytics** dengan fokus pada implementasi akuisisi data terstruktur (API & Web Scraping/Parsing SQL) secara etis, jujur, dan patuh terhadap regulasi data akademis.

---

##  Identitas Mahasiswa
* **Nama**          : Apolonia Werner
* **NIM**           : 2501010151
* **Program Studi** : Data Analytics / Manajemen Data

---

##  Penyelesaian Catatan Koreksi Dosen 
Proyek ini telah diperbaiki secara total untuk menanggapi seluruh poin kritik dari dosen penguji:

1. **Kepatuhan Etis (`robots.txt`)**:
   Tidak melakukan *bypass* atau manipulasi logika. Target scraping telah dialihkan ke Repositori Resmi Kode Wilayah Kemendagri RI. Uji legalitas melalui `urllib.robotparser` menghasilkan status **`True` (Akses Disetujui)** secara murni.
2. **Keaslian Dataset (Anti-Dummy)**:
   Seluruh data nama wilayah, koordinat, dan cuaca bersumber dari basis data kementerian (Kemendagri) dan satelit riil (Open-Meteo), bukan data buatan (*dummy data*).
3. **Integritas Penggabungan Data**:
   Proses merge tabel menggunakan parameter keamanan `validate="one_to_one"` untuk menjamin tidak adanya replikasi baris data ganda.

---

##  Struktur Direktori Proyek

```text
uts_DAM_werner/
├── hasil_uts_dam_2501010151/
│   ├── Data/
│   │   ├── Raw/
│   │   │   ├── dataset_wisata_ekraf_ntt.csv        <-- Data pariwisata asli dari OpenStreetMap (>100 baris)
│   │   │   ├── api_open_meteo_ntt.json             <-- Respons mentah JSON dari API Cuaca Open-Meteo
│   │   │   └── kemendagri_wilayah_ntt.sql          <-- Berkas database SQL asli dari Kemendagri RI
│   │   └── Process/
│   │       ├── csv_bersih.csv                      <-- Data pariwisata bersih (format CSV)
│   │       ├── dataset_pariwisata_ntt_bersih.xlsx  <-- Data pariwisata bersih (format Excel)
│   │       ├── json_api_bersih.csv                 <-- Hasil normalisasi tabel cuaca (154 baris)
│   │       ├── html_scraping_clean.csv             <-- Data kabupaten/kota resmi NTT bersih
│   │       ├── gabungan_pariwisata_ntt.csv         <-- Hasil penggabungan presisi (one-to-one)
│   │       ├── metadata_gabungan.json              <-- Metadata dan skema integrasi data
│   │       └── visualisasi_pariwisata_ntt.png      <-- Grafik visualisasi rata-rata suhu maksimum
│   └── docs/
│       ├── data_ethics_checklist.md                <-- Dokumen kepatuhan etika data (9 butir)
│       ├── robots_check.json                       <-- Bukti otentik kepatuhan terhadap robots.txt
│       └── provenance.csv                          <-- Log silsilah data (Provenance) lengkap dengan hash MD5
├── uts_data_analytics_2501010151.ipynb             <-- File kode utama Google Colab
└── README.md                                       <-- File dokumentasi ini
```

---

##  Cara Menjalankan Notebook
1. Pastikan Anda memiliki koneksi internet aktif untuk proses penarikan data cadangan dari API.
2. Buka berkas `uts_data_analytics_2501010151.ipynb` di Google Colab.
3. Jalankan sel inisialisasi awal (Sel 1) untuk mengonfigurasi header email `apoloniawerner396@gmail.com`.
4. Pilih menu **Runtime > Run All** untuk mengeksekusi seluruh analisis tanpa error.
