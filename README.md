# Analisis Pengaruh Kegiatan Internal dan Eksternal terhadap Performa Akademik Mahasiswa

Proyek UTS Data Science 2026/2027, Program Studi Informatika, UPN "Veteran" Yogyakarta.
Dosen pengampu: Dhimas Arief Dharmawan, S.T., Ph.D.

Proyek ini menguji kegiatan mahasiswa mana yang berhubungan dengan CGPA. Kegiatan **internal**
(kehadiran, ko-kurikuler, konsultasi dosen) dan **eksternal** (jam belajar, media sosial, pengembangan
keterampilan) dibandingkan dengan CGPA pada 1.155 mahasiswa. Kerangka kerja yang dipakai adalah CRISP-DM.

## Isi repository

| Berkas | Keterangan |
|---|---|
| `Project_DataScience.ipynb` | Notebook utama: Business Understanding, Data Gathering, EDA, Cleaning, EDA lanjutan, dan Preprocessing |
| `data/Students_Performance_data_set.xlsx` | Dataset asli (CC BY 4.0) |
| `data/data_bersih.csv` | Data setelah cleaning|
| `fig/` | Gambar hasil EDA yang dipakai di laporan
|
| `requirements.txt` | Daftar pustaka Python |

## Cara menjalankan

1. Pasang Python 3.10 atau lebih baru.
2. `pip install -r requirements.txt`
3. Buka `Project_DataScience.ipynb` lalu jalankan semua sel dari atas ke bawah (*Run All*).

Notebook membaca data dari folder `data/` dan menyimpan gambar ke `fig/`. Validasi silang dan pembagian data
memakai `random_state=42`, jadi hasilnya sama setiap kali dijalankan.

## Temuan singkat

- Setelah 39 mahasiswa baru (CGPA = 0) dikeluarkan, rata-rata CGPA adalah 3,27.
- Kehadiran berhubungan positif dengan CGPA (Spearman 0,25). Jam media sosial berhubungan negatif sangat lemah (−0,09).
- Ko-kurikuler, konsultasi dosen, jam belajar, dan jam keterampilan tidak berhubungan nyata dengan CGPA.
- SGPA sebelumnya paling kuat (Spearman 0,63). Regresi linear R² 0,45 dengan SGPA, 0,03 tanpa SGPA.
- Hasil hanya menunjukkan hubungan, bukan sebab-akibat, dan berasal dari satu program studi di satu kampus.

## Sumber data

Rahman, A. T., Lamia, S., Shishir, A. H., & Barsa, M. M. (2024). *Students_Academic_Performance_Evaluation_Dataset*
(Versi 1) [Dataset]. Mendeley Data. https://doi.org/10.17632/dc3797vf3t.1. Lisensi CC BY 4.0.
