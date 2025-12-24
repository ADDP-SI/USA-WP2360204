# **UJIAN AKHIR SEMESTER (UAS)**

**Mata Kuliah:** Algoritma & Dasar Pemrograman

**Petunjuk Pengerjaan:**

1. Buatlah file `Python` (`.py`) untuk setiap nomor soal.
2. Gunakan komentar untuk menjelaskan logika kode Anda jika diperlukan.
3. Pastikan program dapat berjalan (`running`) tanpa error sintaks.
4. Penilaian didasarkan pada `logika algoritma`, `ketepatan output`, dan penggunaan fitur bahasa yang sesuai.

5. Submit tugas Anda ke **[Google Drive](https://drive.google.com/drive/folders/1_NVUE1ql9Yixs6S2dKtfExVzG6frSIys?usp=sharing)**. Sesuaikan dengan kelas Anda. dan untuk penamaan folder harus `NIM-NAMA` contoh : `25602040012-NAMA ANDA` simpan file `.py` dengan nama file `soal1.py`, `soal2.py`, dst. didalam folder `NIM-NAMA` Anda.

### **SOAL 1: Logika Dasar & Percabangan (10 Poin)**

Buatlah program **Indeks Massa Tubuh (IMT)**.

1. Minta input `berat_badan` (kg) dan `tinggi_badan` (cm).
2. Konversi tinggi badan ke meter.
3. Hitung IMT dengan rumus: $IMT = \frac{berat\_badan}{tinggi \times tinggi}$.
4. Tampilkan kategori berdasarkan aturan:
* IMT < 18.5: "Kurus"
* 18.5 <= IMT < 25: "Normal"
* 25 <= IMT < 30: "Gemuk"
* IMT >= 30: "Obesitas"


### **SOAL 2: Perulangan & Aritmatika (10 Poin)**

Buatlah program **Pengecekan Bilangan Prima**.
Program meminta input sebuah angka bulat positif, lalu menentukan apakah angka tersebut adalah bilangan Prima atau bukan.

* *Clue:* Bilangan prima hanya habis dibagi 1 dan dirinya sendiri. Gunakan perulangan `for` dan operator modulo `%`.

### **SOAL 3: Struktur Data List (10 Poin)**

Buatlah program **Keranjang Belanja Sederhana**.

1. Buat list kosong `keranjang = []`.
2. Gunakan perulangan `while` untuk meminta user memasukkan nama barang.
3. Jika user mengetik "selesai", perulangan berhenti.
4. Setiap barang yang diketik dimasukkan ke dalam list.
5. Di akhir program, cetak: "Isi keranjang Anda: `[item1, item2, ...]`" dan "Total barang: `X`".

### **SOAL 4: Manipulasi String (10 Poin)**

Buatlah program **Deteksi Palindrom**.

Program meminta input sebuah kata/kalimat. Program harus mengecek apakah kata tersebut adalah *Palindrome* (dibaca dari depan dan belakang sama).

* Syarat: Abaikan perbedaan huruf besar/kecil (case-insensitive).
* Contoh True: "Katak", "Malam", "Radar".
* Contoh False: "Makan", "Siang".

### **SOAL 5: Fungsi & Modularisasi (10 Poin)**

Buatlah program **Konversi Suhu Modular**.

1. Buat fungsi `celcius_ke_fahrenheit(c)` yang mengembalikan nilai Fahrenheit.
2. Buat fungsi `celcius_ke_kelvin(c)` yang mengembalikan nilai Kelvin.
3. Di program utama, minta input suhu Celcius.
4. Panggil kedua fungsi tersebut dan tampilkan hasilnya.

### **SOAL 6: Operator Bitwise (5 Poin)**

Buatlah fungsi sederhana `cek_ganjil_genap_bitwise(angka)`.
Fungsi ini harus menentukan apakah angka Ganjil atau Genap **tanpa menggunakan operator modulo (`%`)**, melainkan menggunakan operator **Bitwise AND (`&`)**.

* *Clue:* Angka ganjil pasti bit terakhirnya bernilai 1.

### **SOAL 7: Algoritma Pencarian / Searching (10 Poin)**

Diberikan list data stok barang berikut:
`stok = ["Buku", "Pensil", "Penggaris", "Penghapus", "Spidol"]`
Buatlah program yang:

1. Meminta input nama barang yang dicari user.
2. Gunakan algoritma **Linear Search** untuk mencari barang tersebut.
3. Jika ketemu, cetak "Barang ditemukan pada indeks ke-X".
4. Jika tidak, cetak "Barang tidak tersedia".
5. Pastikan pencarian tidak terpengaruh huruf besar/kecil.

### **SOAL 8: Algoritma Pengurutan / Sorting (15 Poin)**

Diberikan data nilai ujian mahasiswa yang acak:
`nilai = [55, 80, 90, 65, 70, 40, 95]`

1. Implementasikan algoritma **Bubble Sort** atau **Selection Sort** (Pilih satu) secara manual. **DILARANG** menggunakan fungsi bawaan `.sort()` atau `sorted()`.
2. Urutkan nilai dari yang **Terbesar ke Terkecil (Descending)**.
3. Tampilkan list setelah diurutkan.

### **SOAL 9: Rekursi (10 Poin)**

Buatlah fungsi rekursif bernama `pangkat_rekursif(bilangan, eksponen)`.
Program menghitung hasil perpangkatan tanpa menggunakan operator `**`.

* Contoh input: `bilangan = 2`, `eksponen = 3`
* Logika rekursi: $2^3 = 2 \times 2^2 \rightarrow 2 \times (2 \times 2^1) \dots$
* Output: `8`

### **SOAL 10: Studi Kasus Terintegrasi (10 Poin)**

**Program Manajemen Kontak Sederhana.**
Gabungkan konsep List, Fungsi, dan Menu (`while` loop).
Fitur yang harus ada:

1. `tambah_kontak(nama, no_hp)`: Menambahkan data ke list (bisa list of strings atau list of tuples).
2. `lihat_kontak()`: Menampilkan semua daftar kontak dengan perulangan `for`.
3. Menu utama yang terus berjalan sampai user memilih "Keluar".

---

#### **Rubrik Penilaian**

| Kriteria | Deskripsi | Poin Maksimal |
| --- | --- | --- |
| **Logika Algoritma** | Alur program benar dan memecahkan masalah sesuai soal. | 50% |
| **Sintaks** | Kode berjalan tanpa error (Syntax Error/Runtime Error). | 30% |
| **Implementasi Konsep** | Menggunakan konsep yang diminta (misal: Soal 8 wajib manual sort, bukan `.sort()`). | 20% |

Selamat Mengerjakan dan Semoga Sukses!