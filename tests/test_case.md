# TEST CASE

## Pengujian Program Pengolahan dan Analisis Nilai Matematika

**Nama:** Siti Nurhasanah  
**NIM:** 2225250073  
**Kelas:** 3B  

---

## 1. Tujuan Pengujian

Pengujian ini dilakukan untuk mengetahui apakah Program Pengolahan dan Analisis Nilai Matematika dapat bekerja sesuai rancangan yang telah dibuat. Aspek yang diperiksa meliputi proses pembacaan data dari file, pengecekan validitas nilai, perhitungan statistik nilai, penentuan ketuntasan belajar, serta kemampuan program dalam menangani data yang tidak sesuai format.

---

## 2. Aturan yang Digunakan dalam Program

Dalam proses pengujian, program menggunakan ketentuan sebagai berikut:

- Nilai yang dapat diproses berada pada rentang 0 hingga 100.
- Nilai ketuntasan minimal (KKM) ditetapkan sebesar 60.
- Siswa dengan nilai 60 atau lebih dikategorikan **Tuntas**.
- Siswa yang memperoleh nilai di bawah 60 dikategorikan **Belum Tuntas**.
- Data yang tidak memenuhi format yang ditentukan tidak akan diikutsertakan dalam proses analisis.
- Apabila tidak ditemukan data yang valid, program akan memberikan informasi bahwa data tidak tersedia untuk diproses.

---

## 3. Data yang Digunakan untuk Pengujian

Isi file `data/nilai_contoh.txt`:

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

Pada data di atas, baris **A004** sengaja diberikan nilai berupa teks (`abc`) untuk menguji kemampuan program dalam mengenali dan mengabaikan data yang tidak valid.

---

## 4. Skenario Pengujian

Tabel berikut berisi berbagai kondisi yang digunakan untuk menguji fungsi-fungsi utama program.

| ID | Skenario | Masukan | Hasil yang Diharapkan |
|----|----------|----------|----------------------|
| TC01 | Memeriksa nilai di atas KKM | 85 | Status Tuntas |
| TC02 | Memeriksa nilai tepat pada KKM | 60 | Status Tuntas |
| TC03 | Memeriksa nilai di bawah KKM | 45 | Status Belum Tuntas |
| TC04 | Menguji batas nilai terendah | 0 | Diterima sebagai nilai valid |
| TC05 | Menguji batas nilai tertinggi | 100 | Diterima sebagai nilai valid |
| TC06 | Menguji nilai negatif | -5 | Ditolak karena di luar rentang |
| TC07 | Menguji nilai melebihi batas | 110 | Ditolak karena tidak valid |
| TC08 | Menguji input berupa teks | abc | Data diabaikan |
| TC09 | Membaca data dengan format benar | NIM,nilai | Data berhasil diproses |
| TC10 | Membaca data tanpa tanda koma | A011 80 | Data ditolak |
| TC11 | Membaca baris kosong | Baris kosong | Dilewati |
| TC12 | Membuka file yang tidak tersedia | Nama file salah | Pesan kesalahan muncul |
| TC13 | Seluruh data tidak valid | File kosong/data salah | Program menampilkan informasi tidak ada data |
| TC14 | Perhitungan rata-rata | 80,70,90 | Nilai rata-rata = 80 |
| TC15 | Pencarian nilai maksimum | 80,70,90 | Nilai tertinggi = 90 |
| TC16 | Pencarian nilai minimum | 80,70,90 | Nilai terendah = 70 |
| TC17 | Menghitung siswa tuntas | 60,75,50 | Jumlah tuntas = 2 |
| TC18 | Menghitung siswa belum tuntas | 60,75,50 | Jumlah belum tuntas = 1 |
| TC19 | Menampilkan rekapitulasi nilai | Data valid | Ringkasan statistik muncul |
| TC20 | Menyimpan laporan hasil analisis | Data valid | File laporan berhasil dibuat |

---

## 5. Hasil yang Diharapkan

Dari data pengujian yang digunakan, terdapat sembilan data yang memenuhi syarat untuk diproses dan satu data yang tidak valid.

| Komponen | Hasil |
|-----------|--------:|
| Jumlah data valid | 9 siswa |
| Jumlah keseluruhan nilai | 673 |
| Rata-rata nilai | 74,78 |
| Nilai tertinggi | 100 |
| Nilai terendah | 45 |
| Siswa tuntas | 7 siswa |
| Siswa belum tuntas | 2 siswa |
| Data tidak valid | 1 data |

---

## 6. Pengujian Fungsi Pendukung

Selain pengujian program secara keseluruhan, beberapa fungsi pendukung juga diuji secara terpisah untuk memastikan hasil yang diberikan sudah sesuai.

| ID | Fungsi | Input | Hasil yang Diharapkan |
|----|---------|---------|----------------------|
| UT01 | `validasi_nilai()` | 80 | `True` |
| UT02 | `validasi_nilai()` | 120 | `False` |
| UT03 | `validasi_nilai()` | `"abc"` | `False` |
| UT04 | `status_ketuntasan()` | 85 | `"Tuntas"` |
| UT05 | `status_ketuntasan()` | 60 | `"Tuntas"` |
| UT06 | `status_ketuntasan()` | 45 | `"Belum Tuntas"` |
| UT07 | `format_nilai()` | 85 | `"85.00"` |
| UT08 | `format_nilai()` | `"abc"` | `"Tidak valid"` |

---

## 7. Pengujian Fungsi Analisis Data

Pengujian berikut bertujuan memastikan proses analisis nilai dilakukan dengan benar.

| ID | Fungsi | Input | Hasil yang Diharapkan |
|----|---------|---------|----------------------|
| AN01 | `analisis_nilai()` | 80,70,90 | Rata-rata = 80 |
| AN02 | `analisis_nilai()` | Data kosong | Mengembalikan `None` |
| AN03 | `analisis_nilai()` | 60,50 | 1 tuntas dan 1 belum tuntas |
| AN04 | `analisis_nilai()` | 100,0 | Nilai maksimum 100 dan minimum 0 |

---

## 8. Indikator Keberhasilan

Pengujian dianggap berhasil apabila seluruh fungsi utama program dapat berjalan sesuai tujuan yang telah ditetapkan, yaitu:

1. Data dari file dapat dibaca dengan benar.
2. Data yang tidak valid dapat ditangani tanpa menyebabkan program berhenti.
3. Nilai di luar rentang yang diperbolehkan dapat ditolak.
4. Perhitungan statistik menghasilkan nilai yang tepat.
5. Status ketuntasan ditentukan berdasarkan KKM yang digunakan.
6. Kondisi file tidak ditemukan maupun data kosong dapat ditangani dengan baik.
7. Hasil analisis dapat ditampilkan dan disimpan ke file laporan.

---

## 9. Penutup

Dokumen pengujian ini digunakan sebagai acuan untuk mengevaluasi ketepatan fungsi dan keandalan Program Pengolahan dan Analisis Nilai Matematika. Program dinyatakan memenuhi kebutuhan apabila seluruh skenario pengujian menghasilkan keluaran yang sesuai dengan hasil yang telah direncanakan. Setelah program dijalankan, hasil aktual dari setiap pengujian perlu dicatat sebagai bahan evaluasi dan perbaikan.