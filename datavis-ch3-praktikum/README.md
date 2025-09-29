# Praktikum Datavis – Static First (Chapter 3 Baseline)

## Setup Lingkungan
1. Buat virtual environment: `python -m venv venv`
2. Aktifkan venv  
   - Windows PowerShell: `.\venv\Scripts\Activate.ps1`  
   - macOS/Linux: `source venv/bin/activate`
3. Install dependensi dasar: `pip install -r requirements.txt`
4. Jalankan antarmuka: `jupyter lab` (alternatif: `jupyter notebook`)

> Tip: setelah instalasi berhasil, bekukan versi dengan `pip freeze > requirements-lock.txt` bila ingin reproduksibilitas penuh.

## Alur Kerja Cepat
- Aktifkan venv sebelum membuka notebook.  
- Masuk ke direktori `notebooks/` lalu buka file yang relevan melalui Jupyter.  
- Jalankan seluruh sel guna memastikan semua visualisasi dapat dirender tanpa error.  
- Gunakan dataset bawaan seaborn (diamonds, iris, tips, flights); tidak perlu unduhan eksternal.

## Notebook yang Tersedia
### `01_praktikum_statis.ipynb`
Notebook utama berisi rangkaian contoh visualisasi statis:
- **Setup & data check** – memuat paket, menampilkan versi, dan mempersiapkan dataset.
- **Distribusi** – histogram vs log scale, KDE, ECDF untuk membaca bentuk dan sebaran data.
- **Sebaran kategori** – boxplot, violin plot, dan strip plot guna membandingkan antar kategori.
- **Kategori & agregasi** – countplot, barplot mean/median serta `catplot` dengan hue.
- **Relasi antar variabel** – scatterplot multi-hue, regresi linear (`lmplot`), dan pairplot.
- **Tren waktu** – line chart musiman serta area plot rata-rata tahunan dari dataset flights.
- **Korelasi & heatmap** – korelasi numerik diamonds dan heatmap penumpang per bulan/tahun.

Gunakan notebook ini sebagai materi utama praktikum sebelum mengerjakan tugas mandiri.

### `05_homework_template.ipynb`
Template tugas yang meminta mahasiswa:
1. Memilih salah satu dataset bawaan seaborn (`tips`, `flights`, `iris`, dsb.).
2. Membuat minimal satu histogram, satu barplot agregasi, dan satu scatter/line plot.
3. Menambahkan interpretasi singkat pada sel markdown setelah setiap visualisasi.

## Struktur Direktori
```
datavis-ch3-praktikum/
├─ README.md
├─ requirements.txt
├─ notebooks/
│  ├─ 01_praktikum_statis.ipynb
│  └─ 05_homework_template.ipynb
└─ venv/  # dibuat lokal, jangan dikomit
```

## Pemeriksaan Cepat
- `python --version` memastikan interpreter benar.
- `jupyter lab --no-browser` untuk uji buka server tanpa membuka tab otomatis.
- Jalankan seluruh sel di `01_praktikum_statis.ipynb` setelah instalasi; semua chart harus tampil normal.
