# Proyek Akuisisi & Manajemen Data (UTS DAM)

Proyek ini bertujuan untuk melakukan akuisisi, pembersihan, dan integrasi data Statistik Pariwisata Bali dengan data historis cuaca harian Bali tahun 2025.

## 👤 Data Diri

| Keterangan | Informasi |
| :--- | :--- |
| **Nama Lengkap** | [Isi Nama Lengkap Anda] |
| **NIM** | [Isi NIM Anda] |
| **Program Studi** | [Isi Program Studi Anda] |
| **Mata Kuliah** | Data Acquisition & Management (DAM) |
| **Dosen Pengampu** | [Isi Nama Dosen Pengampu] |

## 📂 Struktur Direktori Proyek
```
├── data/
│   ├── raw/
│   │   ├── download/      # Berkas mentah hasil unduhan (.xlsx)
│   │   ├── api/           # Berkas JSON mentah hasil dari API
│   │   └── scraping/      # Berkas HTML mentah hasil scraping
│   └── processed/         # Berkas bersih (.csv) dan hasil integrasi data
├── docs/
│   ├── provenance.json    # Dokumen silsilah/asal-usul data
│   └── data_ethics_checklist.csv # Checklist etika akuisisi data
├── notebooks/
│   └── uts_dam_fix.ipynb  # Notebook utama pengerjaan UTS
└── README.md              # Dokumentasi proyek
```

## 🔗 Sumber Data & URL Resmi

Berikut adalah rincian asal-usul dan URL setiap sumber data yang digunakan dalam proyek ini:

1. **Data Statistik Pariwisata Bali (Metode: Download / Scraping)**
   - **Sumber Instansi:** Dinas Pariwisata Provinsi Bali (Disparda Bali)
   - **URL Halaman Resmi:** [https://disparda.baliprov.go.id/buku-statistik-pariwisata-bali-tahun-2025](https://disparda.baliprov.go.id/buku-statistik-pariwisata-bali-tahun-2025)
   - **Tautan Berkas Mentah (.xlsx):** [https://disparda.baliprov.go.id/wp-content/uploads/2023/12/Table-17-Final-7.xlsx](https://disparda.baliprov.go.id/wp-content/uploads/2023/12/Table-17-Final-7.xlsx)

2. **Data Histori Cuaca Bali (Metode: API)**
   - **Sumber Layanan:** Open-Meteo Historical Weather API
   - **URL Platform:** [https://open-meteo.com/](https://open-meteo.com/)
   - **Endpoint API Yang Diakses:** [https://archive-api.open-meteo.com/v1/archive](https://archive-api.open-meteo.com/v1/archive?latitude=-8.65&longitude=115.2167&start_date=2025-01-01&end_date=2025-01-10&hourly=temperature_2m,relative_humidity_2m,rain&timezone=Asia%2FSingapore)

## 🛠️ Cara Menjalankan Proyek
1. Pastikan folder data sesuai dengan struktur di atas.
2. Jalankan notebook pada folder `notebooks/` secara berurutan untuk melakukan akuisisi API cuaca, pembersihan file pariwisata, hingga integrasi data akhir.
3. Hasil akhir penggabungan akan diekspor secara otomatis ke `data/processed/data_integrasi_pariwisata_cuaca.csv`.