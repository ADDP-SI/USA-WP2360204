# **Modul Praktikum 1: Pengenalan Dasar Python**

Selamat datang di praktikum pertama pemrograman Python\! Modul ini akan memandu Anda memahami elemen-elemen paling fundamental dalam Python, yaitu cara menyimpan informasi, jenis-jenis data yang ada, bagaimana mengolah data tersebut, serta cara berinteraksi dengan program yang Anda buat.

**Tujuan Pembelajaran:**

1.  Memahami konsep **variabel** dan cara mendeklarasikannya.
2.  Mengenali **tipe data** dasar seperti string, integer, float, dan boolean.
3.  Menggunakan berbagai jenis **operator** (aritmatika, perbandingan, logika).
4.  Mengimplementasikan fungsi dasar **input** dan **output**.

-----

## **1. Variabel**

Dalam pemrograman, **variabel** adalah sebuah "wadah" atau nama yang digunakan untuk menyimpan suatu nilai atau data di dalam memori komputer. Anggap saja seperti sebuah kotak yang Anda beri label untuk menyimpan sesuatu di dalamnya.

**Aturan Penamaan Variabel:**

  * Harus diawali dengan huruf atau garis bawah (`_`), tidak boleh angka.
  * Dapat berisi huruf, angka, dan garis bawah (`a-z`, `A-Z`, `0-9`, `_`).
  * Bersifat *case-sensitive*, artinya `nama` dan `Nama` dianggap dua variabel yang berbeda.
  * Gunakan nama yang deskriptif (misalnya, `nama_lengkap` lebih baik daripada `nl`).

**Contoh Kode:**

```python
# Mendeklarasikan dan memberikan nilai (assignment) ke variabel
nama_mahasiswa = "Budi Hartono"
umur = 20
nilai_uts = 85.5
sudah_lulus = False

# Mencetak isi variabel
print(nama_mahasiswa)
print(umur)
```

**Latihan 1:**

Buatlah tiga variabel: `nama_produk` (isi dengan nama barang favoritmu), `harga` (isi dengan harganya), dan `stok_tersedia` (isi dengan jumlah stoknya). Cetak ketiga variabel tersebut ke layar.

-----

## **2. Tipe Data**

Setiap nilai yang disimpan dalam variabel memiliki **tipe data**. Tipe data menentukan jenis nilai tersebut dan operasi apa saja yang bisa dilakukan padanya. Python secara otomatis mengenali tipe data saat Anda memberikan nilai ke variabel (*dynamic typing*).

Berikut adalah tipe data dasar yang paling umum:

  * **String (`str`)**: Teks atau kumpulan karakter. Ditulis dengan tanda kutip tunggal (`'...'`) atau ganda (`"..."`).
      * Contoh: `"Halo Dunia"`, `'Python 101'`
  * **Integer (`int`)**: Bilangan bulat, tanpa desimal.
      * Contoh: `10`, `-5`, `2023`
  * **Float (`float`)**: Bilangan desimal atau pecahan.
      * Contoh: `3.14`, `99.9`, `-0.5`
  * **Boolean (`bool`)**: Hanya memiliki dua nilai, `True` atau `False`. Biasanya digunakan untuk menyatakan kondisi.

**Contoh Kode & Pengecekan Tipe Data:**
Anda bisa menggunakan fungsi `type()` untuk memeriksa tipe data sebuah variabel.

```python
# Contoh tipe data
judul_buku = "Belajar Python Dasar"
jumlah_halaman = 150
versi_cetak = 1.2
sedang_dibaca = True

# Mengecek tipe datanya
print(type(judul_buku))      # Output: <class 'str'>
print(type(jumlah_halaman))  # Output: <class 'int'>
print(type(versi_cetak))     # Output: <class 'float'>
print(type(sedang_dibaca))   # Output: <class 'bool'>
```

**Latihan 2:**

Buat sebuah variabel bernama `suhu_celcius` dengan nilai `27.5`. Periksa dan cetak tipe datanya. Kemudian, coba ubah nilai variabel tersebut menjadi sebuah teks (misalnya, `"dua puluh tujuh"`) dan periksa kembali tipe datanya. Amati perubahannya.

-----

## **3. Operator**

**Operator** adalah simbol khusus yang digunakan untuk melakukan operasi pada variabel dan nilai.

### **a. Operator Aritmatika**

Digunakan untuk melakukan operasi matematika umum.

| Operator | Nama                 | Contoh        | Hasil |
| :------- | :------------------- | :------------ | :---- |
| `+`      | Penjumlahan          | `10 + 5`      | `15`  |
| `-`      | Pengurangan          | `10 - 5`      | `5`   |
| `*`      | Perkalian            | `10 * 5`      | `50`  |
| `/`      | Pembagian (float)    | `10 / 4`      | `2.5` |
| `//`     | Pembagian (bulat)    | `10 // 4`     | `2`   |
| `%`      | Modulo (sisa bagi)   | `10 % 3`      | `1`   |
| `**`     | Pangkat              | `10 ** 2`     | `100` |

### **b. Operator Perbandingan**

Digunakan untuk membandingkan dua nilai. Hasilnya selalu `True` atau `False`.

| Operator | Deskripsi             | Contoh       | Hasil |
| :------- | :-------------------- | :----------- | :---- |
| `==`     | Sama dengan           | `5 == 5`     | `True`|
| `!=`     | Tidak sama dengan     | `5 != 3`     | `True`|
| `>`      | Lebih besar dari      | `5 > 3`      | `True`|
| `<`      | Lebih kecil dari      | `5 < 3`      | `False`|
| `>=`     | Lebih besar atau sama | `5 >= 5`     | `True`|
| `<=`     | Lebih kecil atau sama | `5 <= 3`     | `False`|

**Contoh Kode:**

```python
a = 15
b = 4

# Aritmatika
print("Hasil a + b =", a + b)

# Perbandingan
print("Apakah a sama dengan b?", a == b)
print("Apakah a lebih besar dari b?", a > b)
```

**Latihan 3:**

Buat program sederhana untuk menghitung luas persegi panjang. Buat dua variabel, `panjang` dan `lebar`, lalu hitung luasnya (`panjang * lebar`). Cetak hasilnya dengan format: "Luas persegi panjang adalah: [hasil]".

-----

## **4. Input & Output**

### **a. Output**

Kita sudah sering menggunakannya. Fungsi `print()` digunakan untuk menampilkan informasi (output) ke layar atau konsol.

**Contoh Kode:**

```python
nama = "Andi"
umur = 22

# Menggabungkan teks dan variabel
print("Nama saya", nama, "dan umur saya", umur, "tahun.")

# Menggunakan f-string (cara yang lebih modern dan direkomendasikan)
print(f"Nama saya {nama} dan umur saya {umur} tahun.")
```

### **b. Input**

Untuk membuat program yang interaktif, kita perlu menerima masukan (input) dari pengguna. Fungsi `input()` digunakan untuk tujuan ini.

**Penting:** Secara *default*, semua masukan dari fungsi `input()` akan dianggap sebagai tipe data **string (`str`)**. Jika Anda membutuhkan angka, Anda harus mengubahnya (melakukan *casting*).

**Contoh Kode:**

```python
# Meminta input nama dari pengguna
nama_pengguna = input("Silakan masukkan nama Anda: ")

# Meminta input umur, lalu mengubahnya menjadi integer
umur_pengguna = int(input("Masukkan umur Anda: "))

# Menampilkan hasil input
print(f"Halo, {nama_pengguna}! Tahun depan umur Anda adalah {umur_pengguna + 1}.")
```

**Latihan 4:**

Buat program yang meminta pengguna memasukkan alas dan tinggi sebuah segitiga. Program kemudian harus menghitung dan menampilkan luas segitiga tersebut. Ingat, rumus luas segitiga adalah $0.5 \\times alas \\times tinggi$. Pastikan input dari pengguna diubah menjadi tipe data yang sesuai (float atau integer).

-----

## **Referensi & Dokumentasi**

Untuk pemahaman yang lebih mendalam, sangat disarankan untuk merujuk ke sumber-sumber berikut:

1.  **Dokumentasi Resmi Python:**
      * [The Python Tutorial - An Informal Introduction to Python](https://docs.python.org/3/tutorial/introduction.html): Sumber terbaik untuk mempelajari sintaks dasar langsung dari pembuatnya.
2.  **Buku & Sumber Pembelajaran Populer:**
      * **"Automate the Boring Stuff with Python" by Al Sweigart:** Buku gratis yang sangat praktis dan cocok untuk pemula.
      * **W3Schools - Python Tutorial:** Referensi cepat dan interaktif untuk sintaks Python.
      * **Real Python:** Artikel dan tutorial mendalam tentang berbagai topik Python.

Selamat mencoba dan jangan takut untuk bereksperimen dengan kode\!