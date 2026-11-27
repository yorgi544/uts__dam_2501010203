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

| Path / Direktori | Jenis | Keterangan |
| :--- | :--- | :--- |
| `data/raw/download/` | Folder | Berkas mentah hasil unduhan (`.xlsx`) |
| `data/raw/api/` | Folder | Berkas JSON mentah hasil dari API |
| `data/raw/scraping/` | Folder | Berkas HTML mentah hasil scraping |
| `data/processed/` | Folder | Berkas bersih (`.csv`) dan hasil integrasi data |
| `docs/provenance.json` | File | Dokumen silsilah/asal-usul data |
| `docs/data_ethics_checklist.csv` | File | Checklist etika akuisisi data |
| `notebooks/uts_dam_fix.ipynb` | File | Notebook utama pengerjaan UTS |
| `README.md` | File | Dokumentasi proyek |

## 🔗 Sumber Data & URL Resmi

| No | Dataset & Metode | Sumber Instansi / Layanan | URL Resmi & Tautan |
| :--- | :--- | :--- | :--- |
| **1** | **Data Statistik Pariwisata Bali**<br>*(Metode: Download / Scraping)* | Dinas Pariwisata Provinsi Bali (Disparda Bali) | • **Halaman Resmi:** [Buku Statistik Pariwisata Bali 2025](https://disparda.baliprov.go.id/buku-statistik-pariwisata-bali-tahun-2025)<br>• **Berkas Mentah (.xlsx):** [Table-17-Final-7.xlsx](https://disparda.baliprov.go.id/wp-content/uploads/2023/12/Table-17-Final-7.xlsx) |
| **2** | **Data Histori Cuaca Bali**<br>*(Metode: API)* | Open-Meteo Historical Weather API | • **Platform:** [open-meteo.com](https://open-meteo.com/)<br>• **Endpoint API:** [Archive API Open-Meteo](https://archive-api.open-meteo.com/v1/archive?latitude=-8.65&longitude=115.2167&start_date=2025-01-01&end_date=2025-01-10&hourly=temperature_2m,relative_humidity_2m,rain&timezone=Asia%2FSingapore) |

## 🛠️ Cara Menjalankan Proyek

| Tahap | Langkah Pengerjaan | Deskripsi / Output |
| :--- | :--- | :--- |
| **1** | **Persiapan Direktori** | Pastikan seluruh struktur folder data sudah sesuai dengan tabel struktur direktori di atas. |
| **2** | **Eksekusi Notebook** | Jalankan notebook pada folder `notebooks/uts_dam_fix.ipynb` secara berurutan (akuisisi API cuaca, pembersihan data pariwisata, hingga integrasi). |
| **3** | **Hasil Akhir** | Berkas hasil penggabungan akan diekspor secara otomatis ke `data/processed/data_integrasi_pariwisata_cuaca.csv`. |