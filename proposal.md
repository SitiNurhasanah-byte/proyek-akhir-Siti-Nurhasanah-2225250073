# PROPOSAL PROYEK

# Sistem Pengolahan dan Analisis Nilai Matematika Kelas

**Disusun oleh:**  
Nama: Siti Nurhasanah  
NIM: 2225250073  
Kelas: 3B  

**Mata Kuliah:** Algoritma dan Pemrograman

---

## 1. Latar Belakang

Dalam kegiatan pembelajaran, guru perlu melakukan pengolahan nilai untuk mengetahui hasil belajar siswa. Data nilai yang telah diperoleh tidak hanya dicatat, tetapi juga dianalisis agar dapat memberikan informasi mengenai kondisi akademik siswa dalam suatu kelas.

Pengolahan nilai sering melibatkan berbagai perhitungan, seperti mencari rata-rata kelas, menentukan nilai tertinggi dan terendah, serta menghitung jumlah siswa yang telah mencapai ketuntasan belajar. Apabila jumlah data cukup banyak, proses tersebut memerlukan waktu dan ketelitian yang lebih tinggi sehingga berpotensi menimbulkan kesalahan apabila dikerjakan secara manual.

Perkembangan teknologi memungkinkan proses tersebut dilakukan secara otomatis dengan bantuan program komputer. Melalui pemrograman Python, data nilai dapat dibaca, diperiksa validitasnya, kemudian diolah menjadi informasi yang lebih ringkas dan mudah dipahami.

Berdasarkan kondisi tersebut, proyek ini dirancang untuk membuat program sederhana yang dapat membantu proses rekapitulasi dan analisis nilai matematika kelas. Program diharapkan mampu memberikan informasi statistik dasar sekaligus menjadi sarana penerapan konsep-konsep Algoritma dan Pemrograman yang telah dipelajari selama perkuliahan.

---

## 2. Rumusan Masalah

Rumusan masalah yang menjadi dasar pengembangan proyek ini adalah:

1. Bagaimana membuat program yang dapat membaca data nilai matematika dari sebuah file?
2. Bagaimana memastikan data yang diproses telah sesuai dengan format yang ditentukan?
3. Bagaimana menghitung statistik nilai secara otomatis, seperti rata-rata, nilai maksimum, dan nilai minimum?
4. Bagaimana menentukan jumlah siswa yang memenuhi kriteria ketuntasan belajar?
5. Bagaimana menangani kesalahan input agar program tetap dapat berjalan dengan baik?

---

## 3. Tujuan Proyek

Proyek ini memiliki beberapa tujuan sebagai berikut:

1. Merancang program pengolahan nilai matematika berbasis Python.
2. Mengotomatisasi proses rekapitulasi data nilai siswa.
3. Menyajikan informasi statistik sederhana dari data nilai yang tersedia.
4. Mengelompokkan siswa berdasarkan status ketuntasan belajar.
5. Menerapkan validasi data dan penanganan kesalahan dalam program.
6. Meningkatkan pemahaman penerapan algoritma pada kasus sederhana di bidang pendidikan.

---

## 4. Manfaat Proyek

### 4.1 Bagi Guru

Membantu mempercepat proses pengolahan dan analisis nilai sehingga informasi hasil belajar siswa dapat diperoleh dengan lebih efisien.

### 4.2 Bagi Siswa

Memberikan gambaran mengenai pemanfaatan teknologi dalam pengolahan data pendidikan serta penerapan dasar-dasar pemrograman dalam kehidupan nyata.

### 4.3 Bagi Pengembang

Menjadi sarana latihan dalam menerapkan konsep Python, khususnya pada penggunaan fungsi, pengolahan file, percabangan, perulangan, validasi data, dan debugging.

### 4.4 Bagi Pembelajaran

Menunjukkan bagaimana konsep Algoritma dan Pemrograman dapat digunakan untuk membantu menyelesaikan permasalahan administratif sederhana di lingkungan pendidikan.

---

## 5. Batasan Proyek

Agar proses pengembangan program lebih fokus dan sesuai dengan materi yang telah dipelajari, proyek ini memiliki beberapa batasan sebagai berikut:

1. Program dibuat menggunakan bahasa pemrograman Python dan dijalankan melalui terminal.
2. Data nilai dibaca dari file teks dengan format yang telah ditentukan.
3. Setiap data terdiri atas kode siswa dan nilai yang dipisahkan menggunakan tanda koma (,).
4. Nilai yang dapat diproses berada pada rentang 0 sampai 100.
5. Nilai ketuntasan minimum yang digunakan dalam program adalah 60.
6. Program hanya melakukan analisis statistik dasar berupa rata-rata, nilai tertinggi, nilai terendah, jumlah siswa tuntas, dan jumlah siswa belum tuntas.
7. Data yang tidak sesuai format atau berisi nilai tidak valid tidak akan dimasukkan ke dalam proses perhitungan.
8. Program belum dilengkapi dengan antarmuka grafis maupun penyimpanan database.
9. Hasil analisis ditampilkan melalui terminal dan dapat disimpan ke dalam file laporan.

---

## 6. Metode Pelaksanaan

Pengerjaan proyek dilakukan melalui beberapa tahapan agar pengembangan program berjalan secara sistematis.

### 6.1 Identifikasi Kebutuhan

Tahap pertama adalah mengidentifikasi kebutuhan program berdasarkan permasalahan yang sering muncul saat melakukan pengolahan nilai secara manual. Pada tahap ini ditentukan data masukan, proses yang diperlukan, serta hasil yang ingin diperoleh.

### 6.2 Perancangan Algoritma

Setelah kebutuhan program ditentukan, dilakukan penyusunan algoritma sebagai gambaran alur kerja program. Algoritma mencakup proses membaca file, melakukan validasi data, mengolah nilai, dan menghasilkan laporan.

### 6.3 Pembuatan Program

Algoritma yang telah dirancang kemudian diimplementasikan ke dalam kode Python. Program disusun menggunakan beberapa fungsi agar lebih mudah dibaca, diuji, dan dikembangkan.

### 6.4 Pengujian Program

Program diuji menggunakan berbagai kondisi data untuk memastikan seluruh fitur berjalan dengan baik. Pengujian dilakukan pada data valid maupun data yang sengaja dibuat tidak valid.

### 6.5 Evaluasi Hasil

Tahap terakhir yaitu membandingkan hasil keluaran program dengan hasil yang dihitung secara manual. Langkah ini dilakukan untuk memastikan bahwa perhitungan yang dihasilkan program sudah benar.

---

## 7. Rancangan Sistem

### 7.1 Data Masukan

Program menerima data berupa file teks yang berisi kode siswa dan nilai matematika.

Contoh isi file:

```text
A001,85
A002,78
A003,92
A004,abc
A005,60
A006,50
```

Data pada baris keempat sengaja dibuat tidak valid untuk menguji proses validasi yang terdapat pada program.

### 7.2 Proses Pengolahan

Data yang diterima akan diproses melalui beberapa tahapan berikut:

1. Membaca seluruh isi file.
2. Memeriksa format setiap baris data.
3. Mengonversi nilai ke tipe numerik.
4. Memvalidasi nilai agar berada pada rentang yang diperbolehkan.
5. Menyimpan data yang valid.
6. Menghitung rata-rata nilai.
7. Menentukan nilai tertinggi dan terendah.
8. Menghitung jumlah siswa tuntas dan belum tuntas.
9. Menampilkan hasil analisis kepada pengguna.

### 7.3 Data Keluaran

Output yang dihasilkan berupa informasi statistik nilai, yaitu:

- Jumlah data yang berhasil diproses
- Nilai rata-rata kelas
- Nilai tertinggi
- Nilai terendah
- Jumlah siswa tuntas
- Jumlah siswa belum tuntas
- Informasi jika terdapat data yang tidak valid

---

## 8. Contoh Hasil Analisis

Dari data contoh yang digunakan, terdapat satu data yang tidak diproses karena nilai berupa teks (`abc`). Oleh karena itu hanya lima data yang digunakan dalam perhitungan.

| Komponen | Hasil |
|-----------|-------:|
| Jumlah data valid | 5 siswa |
| Rata-rata nilai | 73,00 |
| Nilai tertinggi | 92 |
| Nilai terendah | 50 |
| Jumlah siswa tuntas | 4 siswa |
| Jumlah siswa belum tuntas | 1 siswa |

Hasil tersebut menunjukkan bahwa sebagian besar siswa telah memenuhi batas ketuntasan yang digunakan pada program. Informasi seperti ini dapat membantu pengguna memperoleh gambaran umum mengenai kondisi nilai kelas.

---

## 9. Struktur Folder Proyek

Struktur folder yang digunakan dalam proyek dirancang sederhana agar mudah dipahami dan dikelola.

```text
program-analisis-nilai/
│
├── data/
│   ├── nilai.txt
│   └── laporan.txt
│
├── src/
│   ├── main.py
│   ├── data_io.py
│   ├── analisis.py
│   └── utilitas.py
│
├── tests/
│   └── test_case.md
│
├── README.md
├── proposal.md
└── .gitignore
```

Keterangan:

- `data/` digunakan untuk menyimpan data masukan dan keluaran.
- `src/` berisi kode program utama.
- `tests/` berisi dokumen pengujian.
- `README.md` digunakan sebagai panduan penggunaan program.
- `proposal.md` berisi rancangan proyek.

---

## 10. Rencana Pengujian

| No | Kondisi Pengujian | Hasil yang Diharapkan |
|----|-------------------|----------------------|
| 1 | Data valid | Program memproses seluruh data |
| 2 | File tidak ditemukan | Muncul pesan kesalahan |
| 3 | Nilai berupa teks | Data dilewati |
| 4 | Terdapat baris kosong | Baris diabaikan |
| 5 | Nilai kurang dari 0 | Data ditolak |
| 6 | Nilai lebih dari 100 | Data ditolak |
| 7 | Nilai tepat 60 | Status tuntas |
| 8 | Seluruh data valid | Statistik ditampilkan dengan benar |

---

## 11. Jadwal Pelaksanaan

| Tahap | Kegiatan |
|--------|----------|
| 1 | Analisis kebutuhan program |
| 2 | Penyusunan algoritma dan desain program |
| 3 | Implementasi menggunakan Python |
| 4 | Pengujian dan perbaikan program |
| 5 | Penyusunan dokumentasi dan laporan |

Jadwal tersebut disusun sebagai acuan selama proses pengerjaan proyek dan dapat disesuaikan dengan kondisi pelaksanaan.

---

## 12. Penutup

Pembuatan program ini bertujuan untuk membantu proses pengolahan nilai matematika agar lebih praktis dan terstruktur. Dengan memanfaatkan Python, proses yang sebelumnya dilakukan secara manual dapat dikerjakan secara otomatis sehingga dapat mengurangi kemungkinan kesalahan perhitungan.

Selain menghasilkan sebuah program sederhana, proyek ini juga menjadi sarana untuk menerapkan berbagai konsep yang telah dipelajari pada mata kuliah Algoritma dan Pemrograman, seperti penggunaan fungsi, pengolahan file, validasi data, serta penanganan kesalahan. Diharapkan hasil proyek ini dapat memberikan manfaat sekaligus menambah pengalaman dalam mengembangkan solusi berbasis pemrograman untuk kebutuhan pendidikan.