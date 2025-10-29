# **3. Operator**

**Operator** adalah simbol khusus yang digunakan untuk melakukan operasi pada `variabel` dan `nilai`.

Operator merupakan simbol-simbol yang digunakan untuk melakukan operasi tertentu. Ada 6 jenis operator dalam pemrogramanan yang wajib diketahui:

1. Operator `Aritmatika`
2. Operator `Penugasan`
3. Operator `Pembanding/Relasi`
4. Operator `Logika`
5. Operator `Bitwise`
6. Operator `Ternary`

## 1. Operator Aritmatika

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

### Latihan Praktikum : Operator Aritmatika

Pada bagian ini, kita akan fokus melatih penggunaan operator untuk melakukan kalkulasi matematis dan cara efisien untuk memperbarui nilai variabel.

### Operator Aritmatika

**Tujuan:** Memahami dan menerapkan operator aritmatika dasar dalam konteks pemecahan masalah.

> **Kalkulator Sederhana**\!

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

## 2. Operator Penugasan (Assignment)

**Tujuan:** Memahami cara kerja operator penugasan untuk menyederhanakan kode saat memodifikasi nilai variabel.

| Operator | Contoh      | Ekuivalen dengan |
|:---------|:------------|:-----------------|
| `+=`     | `x += 5`    | `x = x + 5`      |
| `-=`     | `x -= 5`    | `x = x - 5`      |
| `*=`     | `x *= 5`    | `x = x * 5`      |
| `/=`     | `x /= 5`    | `x = x / 5`      |


### Latihan Praktikum : Operator Penugasan

> **Simulasi Poin Game**

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

> **Konversi Suhu**\!

$F = (C \times \frac{9}{5}) + 32$

Buatlah program yang:

1.  Memiliki variabel `suhu_celcius` dengan nilai `30`.

2.  Hitung dan simpan hasilnya dalam variabel `suhu_fahrenheit`.

3.  Cetak hasilnya.


### **Tantangan:** 

Minta pengguna untuk memasukkan nilai Celcius melalui fungsi `input()`\!

> **Total Detik**\!

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

> **Menghitung Bunga Sederhana**

Buatlah program untuk mensimulasikan pertumbuhan saldo tabungan.

1.  Buat variabel `saldo_awal` dengan nilai `1000000`.
2.  Buat variabel `bunga_tahunan` dengan nilai `0.05` (artinya 5%).
3.  Gunakan operator penugasan `*=` untuk menghitung dan **memperbarui** saldo setelah satu tahun. Rumusnya: `saldo = saldo * (1 + bunga_tahunan)`.
4.  Cetak saldo awal dan saldo setelah satu tahun.


-----

## 3. Operator Pembanding & Logika

Pada bagian ini, kita akan belajar bagaimana program Anda dapat membuat perbandingan dan mengambil keputusan berdasarkan logika. Ini adalah fondasi dari program yang "pintar".

### Operator Pembanding / Relasi (Comparison)

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

### Latihan Praktikum : Operator Pembanding

> **Cek Batas Umur (SIM)**

Buatlah program yang:

1.  Meminta pengguna memasukkan usia mereka.
2.  Periksa apakah usia pengguna **lebih besar dari atau sama dengan** 17 (syarat minimal membuat SIM).
3.  Cetak hasil perbandingan tersebut (`True` jika memenuhi syarat, `False` jika tidak).


> **Perbandingan Password**\!

Program yang sering digunakan untuk memvalidasi input. Mari kita buat simulasi sederhananya.

1.  Buat sebuah variabel `password_sistem` dengan nilai `"SuperAman123"`.
2.  Minta pengguna untuk memasukkan password mereka.
3.  Bandingkan apakah password yang dimasukkan pengguna **sama persis** dengan `password_sistem`.
4.  Cetak hasil perbandingannya.

**Tantangan:** Coba masukkan password dengan huruf besar/kecil yang berbeda (misal, "superaman123"). Apa hasilnya? Mengapa?

-----

### Operator Logika (Logical)

**Tujuan:** Memahami cara menggabungkan beberapa kondisi Boolean menjadi satu hasil akhir.

Ada tiga operator logika utama:

  * **`and`**: Menghasilkan `True` hanya jika **kedua** kondisi bernilai `True`.
  * **`or`**: Menghasilkan `True` jika **salah satu** (atau kedua) kondisi bernilai `True`.
  * **`not`**: Membalik nilai Boolean (dari `True` menjadi `False`, dan sebaliknya).

### Latihan Praktikum : Operator Logika

> Validasi Login Lengkap\!

Mari kita gabungkan dengan pengecekan username dan password dari latihan sebelumnya.

1.  Buat variabel `username_benar = "admin"` dan `password_benar = "SuperAman123"`.
2.  Minta input `username_input` dari pengguna.
3.  Minta input `password_input` dari pengguna.
4.  Buat satu kondisi yang mengecek apakah `username_input` **SAMA DENGAN** `username_benar` **DAN** `password_input` **SAMA DENGAN** `password_benar`.
5.  Cetak hasil akhir (status login berhasil atau tidak).

> **Syarat Kelulusan**\!

Seorang siswa dinyatakan lulus jika:

1.  Nilai ujian teori di atas 75 (`teori > 75`).
2.  **DAN** nilai ujian praktik di atas 75 (`praktik > 75`).

Buatlah program yang:

1.  Meminta input `nilai_teori` dan `nilai_praktik`.
2.  Cetak status kelulusan (`True` atau `False`) berdasarkan kedua syarat tersebut.

> Pengecekan Hari Libur\!

Seseorang akan pergi piknik jika:

1.  Hari itu adalah akhir pekan (`is_weekend = True`).
2.  **ATAU** hari itu adalah tanggal merah (`is_tanggal_merah = True`).

Buatlah program yang:

1.  Memiliki variabel `is_weekend = False` dan `is_tanggal_merah = True`.
2.  Tentukan apakah orang tersebut akan pergi piknik atau tidak.
3.  Cetak hasilnya.

> Menggunakan `not`\!

Buatlah sebuah program sederhana yang:

1.  Memiliki variabel `sedang_sibuk = True`.
2.  Cetak kebalikan dari variabel tersebut menggunakan `not` (yang akan merepresentasikan "apakah saya bebas?").
3.  Cetak hasilnya.

> Tantangan (Gabungan): Pengecekan Tiket Wahana

Sebuah wahana *roller coaster* memiliki aturan ketat:

1.  Pengunjung harus memiliki tinggi badan **minimal 160 cm**.
2.  **DAN** usianya **minimal 14 tahun**.
3.  **DAN** pengunjung tersebut **TIDAK** memiliki riwayat penyakit jantung.

Buatlah program yang:

1.  Meminta input `tinggi_badan` (int), `usia` (int), dan `punya_penyakit_jantung` (string "ya" atau "tidak").
2.  Konversi input `punya_penyakit_jantung` menjadi Boolean (jika "ya" maka `True`, jika "tidak" maka `False`).
3.  Gunakan operator pembanding dan logika (`and`, `not`) untuk menentukan apakah pengunjung boleh naik.
4.  Cetak `True` (boleh naik) atau `False` (tidak boleh naik).

-----

## 4. Operator Bitwise dan Ternary

- **Operator Ternary:** Cara yang sangat efisien untuk menulis pernyataan `if-else` sederhana dalam satu baris.
- **Operator Bitwise:** Operator tingkat lanjut (low-level) yang bekerja langsung pada representasi biner (angka 0 dan 1) dari sebuah data.

**Tujuan:**

1.  Memahami dan menggunakan sintaks **Operator Ternary** untuk menyingkat kode.
2.  Memahami konsep dasar **operasi biner** (bitwise).
3.  Mengidentifikasi dan menggunakan operator bitwise (`&`, `|`, `^`, `~`, `<<`, `>>`).
4.  Mengenali kasus penggunaan umum untuk operator bitwise.

## Operator Ternary (Conditional Expressions)

**Konsep:**

Operator Ternary adalah cara pintas untuk menulis pernyataan `if-else`. Ini memungkinkan Anda untuk mengevaluasi sebuah kondisi dan mengembalikan satu dari dua nilai berdasarkan apakah kondisi itu `True` atau `False`.

Ini sangat berguna untuk membuat kode lebih ringkas, terutama saat Anda ingin memberikan nilai ke variabel berdasarkan suatu kondisi.

**Sintaks Dasar:**

```python
nilai_jika_true if kondisi else nilai_jika_false
```

**Contoh: `if-else` vs Ternary**

Mari kita lihat perbandingan kode untuk menentukan kelulusan siswa.

**Versi `if-else` standar:**

```python
nilai = 80
status = "" # Variabel harus dideklarasikan dulu

if nilai >= 75:
    status = "Lulus"
else:
    status = "Gagal"

print(f"Nilai Anda {nilai}, status: {status}")
```

**Versi Operator Ternary:**

```python
nilai = 80

# Semua logika 'if-else' terjadi dalam satu baris saat assignment
status = "Lulus" if nilai >= 75 else "Gagal"

print(f"Nilai Anda {nilai}, status: {status}")
```

**Contoh : Ganjil/Genap**

```python
angka = 7
jenis_angka = "Ganjil" if angka % 2 != 0 else "Genap"

print(f"Angka {angka} adalah bilangan {jenis_angka}")
```

**Latihan**

> Konversi ke Ternary

Ubahlah blok kode `if-else` di bawah ini menjadi satu baris menggunakan operator ternary.

```python
# Kode Asli
umur = 20
kategori = ""

if umur < 18:
    kategori = "Anak-anak"
else:
    kategori = "Dewasa"

print(kategori)

# --- Tulis kode ternary Anda di bawah ---
# kategori = ...
# print(kategori)
```

## Operator Bitwise (Operasi Biner)

> **Catatan:** Ini adalah topik lanjutan. Operator bitwise tidak umum digunakan dalam skrip Python sehari-hari (seperti web development atau analisis data), tetapi sangat penting dalam pemrograman tingkat rendah, optimasi, kriptografi, dan sistem perizinan.

### **Konsep Kunci: Semuanya adalah 0 dan 1**

Komputer tidak melihat angka `10` seperti kita. Komputer melihatnya sebagai `1010` (representasi biner). Operator bitwise bekerja langsung pada **setiap bit** (setiap 0 atau 1) dari angka-angka ini.

Anda dapat melihat representasi biner sebuah angka di Python menggunakan fungsi `bin()`:

```python
print(bin(10))  # Output: '0b1010'
print(bin(12))  # Output: '0b1100'
```

('`0b`' hanya awalan yang menandakan "biner").

### **Tabel Operator Bitwise**

| Operator | Nama | Deskripsi |
| :--- | :--- | :--- |
| `&` | AND | `1` jika kedua bit adalah `1`, selain itu `0`. |
| `|` | OR | `1` jika **salah satu** bit adalah `1`. |
| `^` | XOR | `1` jika kedua bit **berbeda**. |
| `~` | NOT | Membalik semua bit (mengubah `0` jadi `1` dan `1` jadi `0`). |
| `<<` | Left Shift | Menggeser bit ke kiri (mengisi `0` di kanan). |
| `>>` | Right Shift| Menggeser bit ke kanan (membuang bit paling kanan). |

-----

### **Contoh Mendalam (`&`, `|`, `^`)**

Mari kita gunakan `a = 10` dan `b = 12`.

  * `a = 10` (Biner: `1010`)
  * `b = 12` (Biner: `1100`)

**1. `&` (AND)**: `a & b`

```
  1010  (10)
& 1100  (12)
------
  1000  (Hasil: 8)
```

  * Bit 1 (kanan): `0 & 0 = 0`
  * Bit 2: `1 & 0 = 0`
  * Bit 3: `0 & 1 = 0`
  * Bit 4 (kiri): `1 & 1 = 1`

**2. `|` (OR)**: `a | b`

```
  1010  (10)
| 1100  (12)
------
  1110  (Hasil: 14)
```

  * Bit 1 (kanan): `0 | 0 = 0`
  * Bit 2: `1 | 0 = 1`
  * Bit 3: `0 | 1 = 1`
  * Bit 4 (kiri): `1 | 1 = 1`

**3. `^` (XOR - "Exclusive OR")**: `a ^ b`

```
  1010  (10)
^ 1100  (12)
------
  0110  (Hasil: 6)
```

  * Bit 1 (kanan): `0 ^ 0 = 0` (karena sama)
  * Bit 2: `1 ^ 0 = 1` (karena berbeda)
  * Bit 3: `0 ^ 1 = 1` (karena berbeda)
  * Bit 4 (kiri): `1 ^ 1 = 0` (karena sama)

-----

### **Contoh Shift (`<<` dan `>>`)**

**1. Left Shift `<<`** (Geser Kiri)
`10 << 1` (Geser `10` ke kiri sebanyak 1 bit)

  * `1010` (10)
  * Digeser 1 ke kiri: `10100` (angka 0 ditambahkan di kanan)
  * `10100` (Biner) = `20` (Desimal)

> **Praktik Terbaik:** Menggeser ke kiri 1 bit sama dengan mengalikan angka dengan 2. (`10 * 2 = 20`).

**2. Right Shift `>>`** (Geser Kanan)
`10 >> 1` (Geser `10` ke kanan sebanyak 1 bit)

  * `1010` (10)
  * Digeser 1 ke kanan: `101` (bit `0` paling kanan dibuang)
  * `101` (Biner) = `5` (Desimal)

> **Praktik Terbaik:** Menggeser ke kanan 1 bit sama dengan "pembagian bulat" (integer division) dengan 2. (`10 // 2 = 5`).

-----

### **Kasus Penggunaan Nyata: Sistem Perizinan (Flags)**

Ini adalah kasus penggunaan bitwise yang paling klasik. Bayangkan Anda memiliki izin (permission) untuk file:

  * `IZIN_BACA` = `4` (Biner: `100`)
  * `IZIN_TULIS` = `2` (Biner: `010`)
  * `IZIN_EKSEKUSI` = `1` (Biner: `001`)

**1. Memberikan Izin (Menggunakan `|` OR)**

Bagaimana jika seorang user boleh Membaca DAN Menulis?

```python
READ = 4
WRITE = 2
EXECUTE = 1

# Beri izin Baca dan Tulis
izin_user = READ | WRITE  # 4 | 2
# 100 | 010 = 110 (Biner) = 6 (Desimal)
print(f"Nilai izin user: {izin_user}") # Output: 6
```

Nilai `6` kini menyimpan kedua izin tersebut.

**2. Memeriksa Izin (Menggunakan `&` AND)**

Sekarang, mari kita periksa apakah `izin_user` (yang nilainya 6) punya `IZIN_BACA` (nilai 4).

```python
# izin_user = 6 (Biner: 110)
# READ = 4 (Biner: 100)

# Gunakan & untuk 'mengekstrak' bit yang relevan
cek_baca = izin_user & READ

# 110 & 100 = 100 (Biner) = 4 (Desimal)
# Hasilnya bukan 0, berarti izin ADA

if (izin_user & READ):
    print("User boleh MEMBACA")

if (izin_user & WRITE):
    print("User boleh MENULIS")

if (izin_user & EXECUTE):
    print("User boleh EKSEKUSI") # Ini tidak akan tercetak
```

**Mengapa ini berhasil?**

  * Cek Baca: `(izin_user & READ)` -\> `6 & 4` -\> `110 & 100` = `100` (Hasilnya `4`, \> 0, berarti `True`)
  * Cek Eksekusi: `(izin_user & EXECUTE)` -\> `6 & 1` -\> `110 & 001` = `000` (Hasilnya `0`, berarti `False`)

**Latihan**

> **Hitung Manual Bitwise**

Berapakah hasil dari `9 | 5`?

  * `9` (Biner: `...`)
  * `5` (Biner: `...`)
  * `9 | 5` = `...` (Biner) = `...` (Desimal)
  * Cek jawaban Anda menggunakan Python.
