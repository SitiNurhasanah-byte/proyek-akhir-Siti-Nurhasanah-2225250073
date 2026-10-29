# Sistem Pengolahan Nilai Matematika Siswa

**Nama:** Siti Nurhasanah  
**NIM:** 2225250073  
**Kelas:** 3B  

---

# 1. Gambaran Program

Proyek ini dibuat untuk membantu proses pengolahan nilai matematika siswa secara otomatis menggunakan bahasa pemrograman Python. Program membaca data nilai dari file teks, memeriksa validitas data yang tersedia, kemudian menghasilkan informasi statistik sederhana yang dapat digunakan untuk melihat gambaran hasil belajar siswa.

Melalui program ini, proses perhitungan yang biasanya dilakukan secara manual dapat dilakukan dengan lebih cepat dan konsisten. Selain itu, program juga mampu mengabaikan data yang tidak sesuai format sehingga hasil analisis tetap valid.

---

# 2. Fitur Utama

Program memiliki beberapa fitur sebagai berikut:

- Membaca data nilai dari file teks.
- Melakukan pengecekan format data.
- Memvalidasi nilai agar berada pada rentang yang diperbolehkan.
- Menghitung rata-rata nilai kelas.
- Menentukan nilai tertinggi dan nilai terendah.
- Menghitung jumlah siswa yang tuntas dan belum tuntas.
- Menampilkan hasil analisis di terminal.
- Menyimpan ringkasan hasil pengolahan ke file laporan.

---

# 3. Aturan Pengolahan Data

Program menggunakan ketentuan berikut dalam proses analisis:

- Nilai yang diproses berada pada rentang 0 sampai 100.
- Nilai minimum ketuntasan ditetapkan sebesar 60.
- Nilai 60 atau lebih akan dikategorikan sebagai **Tuntas**.
- Nilai di bawah 60 akan dikategorikan sebagai **Belum Tuntas**.
- Data yang tidak memenuhi format tidak akan dimasukkan ke proses perhitungan.
- Program akan memberikan informasi apabila file tidak dapat ditemukan atau tidak terdapat data yang dapat diproses.

---

# 4. Struktur Folder Proyek

```text
sistem-pengolahan-nilai/
├── data/
│   ├── nilai_contoh.txt
│   └── laporan_hasil.txt
│
├── output/
│   └── .gitkeep
│
├── src/
│   ├── main.py
│   ├── analisis.py
│   ├── data_io.py
│   └── utilitas.py
│
├── tests/
│   └── test_case.md
│
├── README.md
├── proposal.md
└── .gitignore
```

## Keterangan Folder

| File / Folder | Fungsi |
|--------------|---------|
| `main.py` | Mengatur alur utama program |
| `analisis.py` | Berisi proses perhitungan dan analisis data |
| `data_io.py` | Menangani pembacaan dan penyimpanan file |
| `utilitas.py` | Menyediakan fungsi validasi dan fungsi pendukung |
| `nilai_contoh.txt` | Menyimpan data mentah yang akan dianalisis |
| `laporan_hasil.txt` | Menyimpan hasil rekapitulasi nilai |
| `proposal.md` | Dokumen proposal proyek |
| `test_case.md` | Dokumentasi pengujian program |
| `.gitignore` | Daftar file yang tidak dilacak Git |

---

# 5. Bentuk Data Masukan

Program menggunakan file teks sebagai sumber data.

Contoh isi file:

```text
A001,85
A002,78
A003,92
A004,abc
A005,60
A006,50
A007,75
A008,88
A009,45
A010,100
```

Format data terdiri dari kode siswa dan nilai yang dipisahkan menggunakan tanda koma.

Pada contoh di atas, data `A004,abc` digunakan untuk menguji apakah program dapat mendeteksi nilai yang tidak berbentuk angka.

---

# 6. Cara Menjalankan Program

## Persiapan

Pastikan:

- Python 3 sudah terpasang pada komputer.
- Struktur folder proyek sesuai dengan rancangan.
- File data tersedia pada folder yang telah ditentukan.

## Menjalankan Program

Buka terminal pada folder proyek kemudian jalankan:

```bash
python main.py
```

Setelah program dijalankan, hasil analisis akan ditampilkan pada terminal dan dapat disimpan ke file laporan.

---

# 7. Contoh Hasil Analisis

Berdasarkan data contoh, terdapat sembilan data yang valid dan satu data yang tidak dapat diproses.

| Komponen | Hasil |
|-----------|-------:|
| Data valid | 9 |
| Jumlah nilai | 673 |
| Rata-rata | 74,78 |
| Nilai tertinggi | 100 |
| Nilai terendah | 45 |
| Jumlah siswa tuntas | 7 |
| Jumlah siswa belum tuntas | 2 |
| Data tidak valid | 1 |

Data tersebut memberikan gambaran umum mengenai kondisi hasil belajar siswa dalam satu kelas berdasarkan data yang tersedia.

---

# 8. Pengujian Program

Pengujian dilakukan pada berbagai kondisi untuk memastikan program bekerja sesuai tujuan.

Beberapa aspek yang diperiksa meliputi:

- Validasi rentang nilai.
- Pengelompokan status ketuntasan.
- Pembacaan file data.
- Penanganan data kosong.
- Penanganan nilai yang tidak valid.
- Perhitungan statistik nilai.
- Penanganan file yang tidak ditemukan.
- Penyimpanan laporan hasil analisis.

Rincian seluruh skenario pengujian tersedia pada dokumen `test_case.md`.

---

# 9. Efisiensi Program

Jika jumlah data siswa dinyatakan dengan **n**, maka:

- Kompleksitas waktu: **O(n)**
- Kompleksitas ruang: **O(n)**

Hal ini terjadi karena setiap data hanya dibaca dan diproses satu kali selama program berjalan.

Dengan pendekatan tersebut, program masih cukup efisien untuk digunakan pada data kelas dengan jumlah siswa yang wajar.

---

# 10. Pengembangan Selanjutnya

Program ini masih dapat disempurnakan dengan menambahkan beberapa fitur, seperti:

- Pencarian data siswa berdasarkan NIM.
- Pengurutan nilai dari tertinggi ke terendah.
- Penyimpanan laporan dalam format CSV atau Excel.
- Visualisasi statistik dalam bentuk grafik.
- Menu interaktif berbasis terminal.
- Antarmuka grafis yang lebih mudah digunakan.

---

# 11. Kesimpulan

Proyek ini dibuat sebagai penerapan konsep dasar Algoritma dan Pemrograman dalam kasus sederhana yang berkaitan dengan dunia pendidikan. Program mampu membaca data nilai dari file, melakukan validasi, menghitung statistik dasar, serta menyajikan informasi yang membantu pengguna memahami kondisi nilai siswa secara lebih cepat.

Selain menghasilkan solusi sederhana untuk pengolahan data nilai, proyek ini juga menjadi sarana latihan dalam menerapkan fungsi, pengolahan file, validasi data, exception handling, serta modularisasi program menggunakan Python.