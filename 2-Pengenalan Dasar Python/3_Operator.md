# **3. Operator**

**Operator** adalah simbol khusus yang digunakan untuk melakukan operasi pada `variabel` dan `nilai`.

## **a. Operator Aritmatika**

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

### Contoh Kode :

```python
a = 15
b = 4

# Aritmatika
print("Hasil a + b =", a + b)
#output: Hasil a + b = 19

```

#### Penjelasan:

Variabel `a` dan `b` diberi nilai 15 dan 4. Variabel `a` dan `b` digunakan untuk melakukan operasi aritmatika. Hasil dari setiap operasi aritmatika ditampilkan pada output. 


## **b. Operator Penugasan**

Digunakan untuk menetapkan nilai ke variabel. 

| Operator | Nama                 | Contoh        | Hasil |
| :------- | :------------------- | :------------ | :---- |
| `=`      | Penugasan             | `x = 5`       | `5`   |
| `+=`     | Penugasan penjumlahan | `x += 5`      | `10`  |
| `-=`     | Penugasan pengurangan | `x -= 5`      | `0`   |
| `*=`     | Penugasan perkalian   | `x *= 5`      | `25`  |
| `/=`     | Penugasan pembagian   | `x /= 5`      | `2.5` |
| `//=`    | Penugasan pembagian   | `x //= 5`     | `2`   |
| `%=`     | Penugasan modulo      | `x %= 5`      | `1`   |
| `**=`    | Penugasan pangkat     | `x **= 2`     | `25`  |

### Contoh Kode :

```python
a = 15
b = 4

# Perbandingan
print("Apakah a sama dengan b?", a == b)
print("Apakah a lebih besar dari b?", a > b)

````

```python
x = 5
print("x =", x)
x += 5  # Menambahkan 5 ke nilai x (x = x + 5)
print("x += 5 =", x)
x -= 5  # Mengurangi 5 dari nilai x (x = x - 5)
print("x -= 5 =", x)
x *= 5  # Mengalikan nilai x dengan 5 (x = x * 5)
print("x *= 5 =", x)
x /= 5  # Membagi nilai x dengan 5 (x = x / 5)
print("x /= 5 =", x)
x //= 5  # Membagi bulat nilai x dengan 5 (x = x // 5)
print("x //= 5 =", x)
x %= 5  # Menghitung sisa bagi x dengan 5 (x = x % 5)
print("x %= 5 =", x)
x **= 2  # Memangkatkan nilai x dengan 2 (x = x ** 2)
print("x **= 2 =", x)
print("x =", x)
```


# Latihan Praktikum 3.A: Operator Aritmatika & Penugasan

Pada bagian ini, kita akan fokus melatih penggunaan operator untuk melakukan kalkulasi matematis dan cara efisien untuk memperbarui nilai variabel.

## **Bagian 3.1: Operator Aritmatika**

**Tujuan:** Memahami dan menerapkan operator aritmatika dasar dalam konteks pemecahan masalah.

**Latihan 3.1a: Kalkulator Sederhana**

Buatlah sebuah program yang:

1. Meminta pengguna memasukkan **dua angka** (misalnya, `angka1` dan `angka2`).

2. Lakukan semua operasi aritmatika dasar: penjumlahan, pengurangan, perkalian, pembagian (`/`), pembagian bulat (`//`), dan sisa bagi (`%`).

3. Cetak setiap hasil operasi dengan format yang jelas.

**Contoh Output:**

```bash
Masukkan angka pertama: 15
Masukkan angka kedua: 4

--- Hasil Perhitungan ---
15 + 4 = 19
15 - 4 = 11
15 * 4 = 60
15 / 4 = 3.75
15 // 4 = 3
15 % 4 = 3
```

## **Latihan 3.1b: Konversi Suhu**

Suhu dalam Celcius dapat dikonversi ke Fahrenheit dengan rumus:

$F = (C \times \frac{9}{5}) + 32$

Buatlah program yang:

1.  Memiliki variabel `suhu_celcius` dengan nilai `30`.

2.  Hitung dan simpan hasilnya dalam variabel `suhu_fahrenheit`.

3.  Cetak hasilnya.


### **Tantangan:** 

Minta pengguna untuk memasukkan nilai Celcius melalui fungsi `input()`\!

## **Latihan 3.1c: Total Detik**

Buatlah sebuah program untuk mengkonversi total detik menjadi format jam, menit, dan detik.

1.  Buat variabel `total_detik` dengan nilai, misalnya `3661`. (Artinya 1 jam, 1 menit, 1 detik).

2.  Gunakan operator pembagian bulat (`//`) dan sisa bagi (`%`) untuk menghitung:
      * Jumlah jam
      * Jumlah menit
      * Sisa detik

3.  Cetak hasilnya dalam format: `Jam: [jam], Menit: [menit], Detik: [detik]`.

**Petunjuk:**

  * Ada 3600 detik dalam satu jam.
  * Ada 60 detik dalam satu menit.

-----

## **Bagian 3.2: Operator Penugasan (Assignment)**

**Tujuan:** Memahami cara kerja operator penugasan untuk menyederhanakan kode saat memodifikasi nilai variabel.

| Operator | Contoh      | Ekuivalen dengan |
|:---------|:------------|:-----------------|
| `+=`     | `x += 5`    | `x = x + 5`      |
| `-=`     | `x -= 5`    | `x = x - 5`      |
| `*=`     | `x *= 5`    | `x = x * 5`      |
| `/=`     | `x /= 5`    | `x = x / 5`      |

**Latihan 3.2: Simulasi Poin Game**

Bayangkan Anda sedang membuat sistem skor sederhana untuk sebuah game.

1.  Buat variabel `skor` dan inisialisasi dengan nilai `0`.

2.  Simulasikan kejadian berikut menggunakan **operator penugasan**:
      * Pemain mendapatkan 100 poin karena menyelesaikan level.
      * Pemain kehilangan 25 poin karena terkena jebakan.
      * Pemain mendapatkan bonus poin dua kali lipat dari skor saat ini.

3.  Cetak nilai `skor` setelah setiap kejadian untuk melihat perubahannya.

#### **Contoh Kode Awal:**

```python
skor = 0
print(f"Skor awal: {skor}")

# Pemain menyelesaikan level
skor += 100
print(f"Setelah menyelesaikan level, skor menjadi: {skor}")

# Lanjutkan untuk simulasi berikutnya...
```

-----

### **Latihan 3.2: Menghitung Bunga Sederhana**

Buatlah program untuk mensimulasikan pertumbuhan saldo tabungan.

1.  Buat variabel `saldo_awal` dengan nilai `1000000`.
2.  Buat variabel `bunga_tahunan` dengan nilai `0.05` (artinya 5%).
3.  Gunakan operator penugasan `*=` untuk menghitung dan **memperbarui** saldo setelah satu tahun. Rumusnya: `saldo = saldo * (1 + bunga_tahunan)`.
4.  Cetak saldo awal dan saldo setelah satu tahun.


-----

## **Latihan Praktikum 1.B: Operator Pembanding & Logika**

Pada bagian ini, kita akan belajar bagaimana program Anda dapat membuat perbandingan dan mengambil keputusan berdasarkan logika. Ini adalah fondasi dari program yang "pintar".

### **Bagian 1: Operator Pembanding / Relasi (Comparison)**

**Tujuan:** Memahami cara membandingkan dua nilai untuk mendapatkan hasil Boolean (`True` atau `False`).

Operator ini digunakan untuk mengecek hubungan antara dua nilai:

| Operator | Deskripsi | Contoh | Hasil |
| :--- | :--- | :--- | :--- |
| `==` | Sama dengan | `10 == 10` | `True` |
| `!=` | Tidak sama dengan | `10 != 5` | `True` |
| `>` | Lebih besar dari | `10 > 5` | `True` |
| `<` | Lebih kecil dari | `10 < 5` | `False`|
| `>=` | Lebih besar dari atau sama dengan | `10 >= 10` | `True` |
| `<=` | Lebih kecil dari atau sama dengan | `10 <= 5` | `False`|

**Latihan 1.1: Cek Batas Umur (SIM)**
Buatlah program yang:

1.  Meminta pengguna memasukkan usia mereka.
2.  Periksa apakah usia pengguna **lebih besar dari atau sama dengan** 17 (syarat minimal membuat SIM).
3.  Cetak hasil perbandingan tersebut (`True` jika memenuhi syarat, `False` jika tidak).

-----

**Latihan 1.2: Perbandingan Password**
Program sering memvalidasi input. Mari kita buat simulasi sederhananya.

1.  Buat sebuah variabel `password_sistem` dengan nilai `"SuperAman123"`.
2.  Minta pengguna untuk memasukkan password mereka.
3.  Bandingkan apakah password yang dimasukkan pengguna **sama persis** dengan `password_sistem`.
4.  Cetak hasil perbandingannya.

**Tantangan:** Coba masukkan password dengan huruf besar/kecil yang berbeda (misal, "superaman123"). Apa hasilnya? Mengapa?

-----

### **Bagian 2: Operator Logika (Logical)**

**Tujuan:** Memahami cara menggabungkan beberapa kondisi Boolean menjadi satu hasil akhir.

Ada tiga operator logika utama:

  * **`and`**: Menghasilkan `True` hanya jika **kedua** kondisi bernilai `True`.
  * **`or`**: Menghasilkan `True` jika **salah satu** (atau kedua) kondisi bernilai `True`.
  * **`not`**: Membalik nilai Boolean (dari `True` menjadi `False`, dan sebaliknya).

**Latihan 2.1: Validasi Login Lengkap**
Mari kita gabungkan Latihan 1.2 dengan pengecekan username.

1.  Buat variabel `username_benar = "admin"` dan `password_benar = "SuperAman123"`.
2.  Minta input `username_input` dari pengguna.
3.  Minta input `password_input` dari pengguna.
4.  Buat satu kondisi yang mengecek apakah `username_input` **SAMA DENGAN** `username_benar` **DAN** `password_input` **SAMA DENGAN** `password_benar`.
5.  Cetak hasil akhir (status login berhasil atau tidak).

-----

**Latihan 2.2: Syarat Kelulusan**
Seorang siswa dinyatakan lulus jika:

1.  Nilai ujian teori di atas 75 (`teori > 75`).
2.  **DAN** nilai ujian praktik di atas 75 (`praktik > 75`).

Buatlah program yang:

1.  Meminta input `nilai_teori` dan `nilai_praktik`.
2.  Cetak status kelulusan (`True` atau `False`) berdasarkan kedua syarat tersebut.

-----

**Latihan 2.3: Pengecekan Hari Libur**
Seseorang akan pergi piknik jika:

1.  Hari itu adalah akhir pekan (`is_weekend = True`).
2.  **ATAU** hari itu adalah tanggal merah (`is_tanggal_merah = True`).

Buatlah program yang:

1.  Memiliki variabel `is_weekend = False` dan `is_tanggal_merah = True`.
2.  Tentukan apakah orang tersebut akan pergi piknik atau tidak.
3.  Cetak hasilnya.

-----

**Latihan 2.4: Menggunakan `not`**
Buatlah sebuah program sederhana yang:

1.  Memiliki variabel `sedang_sibuk = True`.
2.  Cetak kebalikan dari variabel tersebut menggunakan `not` (yang akan merepresentasikan "apakah saya bebas?").
3.  Cetak hasilnya.

-----

**Tantangan (Gabungan): Pengecekan Tiket Wahana**
Sebuah wahana *roller coaster* memiliki aturan ketat:

1.  Pengunjung harus memiliki tinggi badan **minimal 160 cm**.
2.  **DAN** usianya **minimal 14 tahun**.
3.  **DAN** pengunjung tersebut **TIDAK** memiliki riwayat penyakit jantung.

Buatlah program yang:

1.  Meminta input `tinggi_badan` (int), `usia` (int), dan `punya_penyakit_jantung` (string "ya" atau "tidak").
2.  Konversi input `punya_penyakit_jantung` menjadi Boolean (jika "ya" maka `True`, jika "tidak" maka `False`).
3.  Gunakan operator pembanding dan logika (`and`, `not`) untuk menentukan apakah pengunjung boleh naik.
4.  Cetak `True` (boleh naik) atau `False` (tidak boleh naik).
