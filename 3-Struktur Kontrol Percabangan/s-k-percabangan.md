# **Modul Praktikum 3: Struktur Kontrol Percabangan**

Selamat datang di modul ketiga\! Hingga saat ini, program yang kita tulis berjalan lurus dari atas ke bawah, baris demi baris. Namun, program yang cerdas perlu **mengambil keputusan**.

**Struktur Kontrol Percabangan** (atau *Conditional Logic*) memungkinkan program kita berjalan di "simpang jalan". Program akan mengevaluasi sebuah kondisi (misalnya, `apakah nilai > 75?`) dan memutuskan blok kode mana yang akan dieksekusi berdasarkan apakah kondisi itu `True` atau `False`.

**Tujuan Pembelajaran:**

1.  Memahami konsep alur program yang tidak linear (bercabang).
2.  Mampu mengimplementasikan logika `if` untuk satu kondisi.
3.  Mampu mengimplementasikan logika `if-else` untuk dua skenario (benar/salah).
4.  Mampu mengimplementasikan logika `if-elif-else` untuk menangani banyak kondisi yang saling eksklusif.
5.  Menerapkan logika percabangan untuk memecahkan studi kasus (Cek Kelulusan & Kategori Umur).

-----

## **1. Percabangan `if` (Satu Kondisi)**

Bentuk paling sederhana dari percabangan adalah `if`. Ini digunakan ketika Anda ingin **melakukan sesuatu hanya jika** sebuah kondisi terpenuhi. Jika kondisi tidak terpenuhi, program akan melewatinya begitu saja.

**Analogi:** "Jika hari ini hujan, maka saya akan bawa payung." (Tidak ada instruksi jika hari tidak hujan).

**Sintaks:**

```python
if kondisi:
    # Blok kode ini akan dieksekusi
    # HANYA JIKA kondisi bernilai True
    pernyataan_1
    pernyataan_2
```

> **PENTING:** Python sangat bergantung pada **indentasi** (jarak menjorok ke dalam). Semua kode yang ingin Anda masukkan ke dalam blok `if` harus memiliki indentasi yang sama (biasanya 4 spasi atau 1 Tab).

### **Contoh 1:**

```python
# Program untuk memberi diskon jika belanja di atas 200rb
total_belanja = int(input("Total belanja Anda: Rp "))

if total_belanja > 200000:
    print("Selamat! Anda mendapatkan diskon 5%!")
    # Kode lain bisa ditambahkan di sini

print("Terima kasih telah berbelanja.")
# Baris ini akan selalu dieksekusi, karena berada di luar blok if
```

**Diskusi:** Coba jalankan kode di atas dua kali. Pertama dengan `250000` dan kedua dengan `150000`. Apa yang berbeda?

-----

## **2. Percabangan `if-else` (Dua Kondisi)**

Ini adalah bentuk percabangan yang paling umum. `if-else` menangani dua skenario: apa yang harus dilakukan jika kondisi `True`, dan apa yang harus dilakukan **jika tidak** (`False`).

**Analogi:** "Jika nilai \>= 75, maka Lulus. **Jika tidak**, maka Gagal."

**Sintaks:**

```python
if kondisi:
    # Blok kode ini dieksekusi jika kondisi True
    pernyataan_true_1
else:
    # Blok kode ini dieksekusi jika kondisi False
    pernyataan_false_1
```

### **Contoh 2: Program Cek Kelulusan**

Mari kita buat program yang diminta: menentukan kelulusan berdasarkan Nilai Kriteria Ketuntasan Minimal (KKM).

```python
# Tentukan KKM (bisa diubah-ubah)
KKM = 75

# Minta input nilai dari pengguna
nilai_siswa = int(input("Masukkan nilai siswa: "))

# Lakukan pengecekan kondisi
if nilai_siswa >= KKM:
    status = "LULUS"
    print(f"Selamat! Dengan nilai {nilai_siswa}, Anda dinyatakan {status}.")
else:
    status = "GAGAL (REMEDIAL)"
    print(f"Maaf. Dengan nilai {nilai_siswa}, Anda dinyatakan {status}.")

print("Proses evaluasi selesai.")
```

**Diskusi:** Apa yang terjadi jika kita memasukkan nilai `75`? Apakah `75 >= 75` bernilai `True` atau `False`? Mengapa operator `>=` penting di sini?

-----

## **3. Percabangan `if-elif-else` (Banyak Kondisi)**

Bagaimana jika kita punya lebih dari dua kemungkinan? Misalnya, untuk menentukan nilai huruf (A, B, C, D, E). Kita tidak bisa menggunakan `if-else` saja.

Di sinilah `elif` (singkatan dari *else if*) digunakan. Ini memungkinkan kita membuat "rantai" kondisi. Python akan mengecek satu per satu dari atas ke bawah dan akan **berhenti di kondisi pertama yang `True`**.

**Analogi:** "Jika lampu merah, berhenti. **Jika tidak, tapi jika** lampu kuning, hati-hati. **Jika tidak** (berarti hijau), jalan."

**Sintaks:**

```python
if kondisi_1:
    # Blok jika kondisi_1 True
    pernyataan_1
elif kondisi_2:
    # Blok jika kondisi_1 False, TAPI kondisi_2 True
    pernyataan_2
elif kondisi_3:
    # Blok jika kondisi_1 & 2 False, TAPI kondisi_3 True
    pernyataan_3
else:
    # Blok jika SEMUA kondisi di atas False
    pernyataan_default
```

### **Contoh 3: Program Kategori Umur**

Mari kita buat program kedua yang diminta: mengelompokkan usia.

```python
# Minta input usia
umur = int(input("Masukkan usia Anda: "))

kategori = ""

if umur < 0:
    kategori = "Input tidak valid"
elif umur <= 5:
    kategori = "Balita"
elif umur <= 12:
    kategori = "Anak-anak"
elif umur <= 18:
    kategori = "Remaja"
elif umur <= 60:
    kategori = "Dewasa"
else:
    # Jika semua kondisi di atas False (berarti umur > 60)
    kategori = "Lansia"

print(f"Usia {umur} tahun termasuk dalam kategori: {kategori}")
```

**Diskusi:** Mengapa urutan `if-elif` ini sangat penting? Apa yang terjadi jika kita meletakkan `elif umur <= 60:` di baris pertama setelah `if`?

-----

## **Latihan Praktikum**

Sekarang, coba terapkan konsep yang sudah dibahas untuk menyelesaikan masalah berikut.

### **Latihan 1: Konversi Nilai Huruf (Grading)**

Buatlah program yang meminta input nilai angka (0-100) dan mengonversinya menjadi nilai huruf berdasarkan aturan berikut:

  * `85 - 100` : `A`
  * `70 - 84`  : `B`
  * `60 - 69`  : `C`
  * `50 - 59`  : `D`
  * `< 50`      : `E`
  * Jika nilai di luar 0-100, cetak "Nilai tidak valid".

### **Latihan 2: Kalkulator Diskon Belanja (Nested If)**

Buat program kalkulator diskon dengan aturan *nested* (bersarang):

1.  Minta input `total_belanja` (int).
2.  Minta input `status_member` (string "ya" atau "tidak").
3.  Terapkan aturan:
      * Jika `total_belanja > 1000000`:
          * Jika `status_member == "ya"`, diskon adalah 10%.
          * Jika `status_member == "tidak"`, diskon adalah 5%.
      * Jika `total_belanja` antara `500000` dan `1000000`:
          * Jika `status_member == "ya"`, diskon adalah 5%.
          * Jika `status_member == "tidak"`, tidak ada diskon (0%).
      * Jika `total_belanja < 500000`:
          * Tidak ada diskon (0%) untuk member ataupun non-member.

Cetak total yang harus dibayar setelah dipotong diskon.


## **Referensi**

  * Dokumentasi Resmi Python - `if` Statements: [https://docs.python.org/3/tutorial/controlflow.html\#if-statements](https://www.google.com/search?q=https://docs.python.org/3/tutorial/controlflow.html%23if-statements)
  * W3Schools - Python If...Else: [https://www.w3schools.com/python/python\_if\_else.asp](https://www.w3schools.com/python/python_if_else.asp)
  * Real Python - Conditional Statements in Python: [https://realpython.com/python-conditional-statements/](https://realpython.com/python-conditional-statements/)
