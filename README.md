# praktikum4


```mermaid
graph TD
    Start((Start))
    InitList[Initialize empty list: data_mahasiswa ]
    InputData[/Input Data Mahasiswa: Nama, NIM, Nilai Tugas, Nilai UTS, Nilai UAS/]
    CalculateNilai[/Calculate Nilai Akhir: tugas times 0.3 plus uts times 0.35 plus uas times 0.35/]
    AddToList[Tambahkan Data ke List]
    Decision{Tambah data lagi?}
    PrintData[/Print output data/]
    End((End))

    Start --> InitList
    InitList --> InputData
    InputData --> CalculateNilai
    CalculateNilai --> AddToList
    AddToList --> Decision
    Decision -- Ya --> InputData
    Decision -- Tidak --> PrintData
    PrintData --> End
```

# Program Input dan Output Data Mahasiswa
Program ini merupakan aplikasi sederhana berbasis konsol untuk mencatat data mahasiswa dan menampilkan hasilnya dalam bentuk tabel. Setiap mahasiswa memiliki informasi berupa nama, NIM, nilai tugas, nilai UTS, nilai UAS, dan nilai akhir yang dihitung berdasarkan bobot tertentu.

### Fitur Utama:
1. Input Data Mahasiswa:
   - Pengguna dapat memasukkan nama, NIM, nilai tugas, UTS, dan UAS.
   - Nilai akhir dihitung otomatis dengan rumus:
                 Nilai Akhir=(Tugas×0.3)+(UTS×0.35)+(UAS×0.35)
2. Penyimpanan Data:
   - Data yang dimasukkan akan disimpan dalam daftar (list) dengan struktur berupa dictionary untuk setiap mahasiswa.
3. Tampilan Data:
   - Setelah input selesai, semua data ditampilkan dalam bentuk tabel dengan kolom berisi nomor, nama, NIM, nilai tugas, UTS, UAS, dan nilai akhir.
4. Pilihan Berhenti:
   - Pengguna dapat memilih untuk menambah data baru atau menghentikan program dengan mengetik y (ya) atau t (tidak).

### Struktur Kode:
1. Inisialisasi List Data Mahasiswa:
   - data_mahasiswa = [] digunakan untuk menyimpan seluruh data mahasiswa yang dimasukkan.
2. Pengumpulan Data:
   - Program berjalan dalam loop while True untuk memungkinkan input data secara berulang.
   - Input data mencakup nama, NIM, nilai tugas, UTS, dan UAS.
3. Perhitungan Nilai Akhir:
   - Nilai akhir dihitung menggunakan formula yang memberikan bobot:
   - 30% untuk nilai tugas.
   - 35% untuk nilai UTS.
   - 35% untuk nilai UAS.
4. Menambah Data ke List:
   - Setiap data mahasiswa ditambahkan ke dalam list data_mahasiswa sebagai dictionary menggunakan metode append.
5. Tampilan Akhir:
   - Setelah loop selesai, data ditampilkan dalam format tabel menggunakan print dengan lebar kolom yang disesuaikan agar lebih rapi.

## Contoh Output

![Output](/code&output/.png)

## Catatan:
- Format tabel disesuaikan agar data lebih mudah dibaca.
- Nilai akhir ditampilkan dengan dua angka desimal menggunakan format(nilai_akhir, '.2f').
