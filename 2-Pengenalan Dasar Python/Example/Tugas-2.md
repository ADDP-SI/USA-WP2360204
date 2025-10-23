Berikut adalah soal yang dirancang untuk menguji pemahaman Anda tentang **Operator Pembanding (Relasi)** dan **Operator Logika**.

> Tugas ini mengharuskan Anda membuat program yang meminta input dari pengguna dan kemudian mencetak hasil evaluasi logika (`True` atau `False`) berdasarkan kondisi yang diberikan.

---

## Tugas 1: Validasi Diskon Belanja

**Skenario:**
Sebuah toko online sedang mengadakan promo. Pelanggan akan mendapatkan diskon jika ia adalah **member** *dan* total belanjanya **di atas Rp 500.000,-**.

**Aturan Logika:**

Dapat Diskon = (`Status Member` == "ya") **AND** (`Total Belanja` > 500000)

**Tugas Anda:**

1.  Buat program yang meminta input `status_member` (string, "ya" atau "tidak").
2.  Minta input `total_belanja` (integer).
3.  Buat satu variabel `dapat_diskon` yang berisi hasil evaluasi logika dari aturan di atas.
4.  Cetak variabel `dapat_diskon` tersebut.

**Contoh Uji:**

* Input 1: `status_member` = "ya", `total_belanja` = 700000
    * Output yang Diharapkan: `True`
* Input 2: `status_member` = "tidak", `total_belanja` = 700000
    * Output yang Diharapkan: `False`
* Input 3: `status_member` = "ya", `total_belanja` = 300000
    * Output yang Diharapkan: `False`

---

## Tugas 2: Seleksi Beasiswa Mahasiswa

**Skenario:**

Sebuah universitas menyeleksi calon penerima beasiswa. Mahasiswa dianggap lolos seleksi tahap pertama jika memenuhi salah satu dari dua kriteria berikut:

1.  Nilai akademik (IPK) mereka **tepat 4.0**.
2.  *Atau*, pendapatan orang tua mereka **di bawah Rp 1.500.000,-**.

**Aturan Logika:**

Lolos Seleksi = (`IPK` == 4.0) **OR** (`Pendapatan Ortu` < 1500000)

**Tugas Anda:**

1.  Buat program yang meminta input `ipk` (float).
2.  Minta input `pendapatan_ortu` (integer).
3.  Buat satu variabel `lolos_seleksi` yang berisi hasil evaluasi logika dari aturan di atas.
4.  Cetak variabel `lolos_seleksi`.

**Contoh Uji:**

* Input 1: `ipk` = 4.0, `pendapatan_ortu` = 5000000
    * Output yang Diharapkan: `True`
* Input 2: `ipk` = 3.5, `pendapatan_ortu` = 1200000
    * Output yang Diharapkan: `True`
* Input 3: `ipk` = 3.8, `pendapatan_ortu` = 3000000
    * Output yang Diharapkan: `False`

---

## Tugas 3: Pengecekan Angka Ganjil (Menggunakan `not`)

**Skenario:**

Anda perlu membuat program untuk memvalidasi apakah sebuah angka merupakan angka ganjil. Kita tahu bahwa angka genap adalah angka yang habis dibagi 2 (sisa baginya `0`). Angka ganjil adalah kebalikannya.

**Aturan Logika:**

1.  `adalah_genap` = (`Angka` % 2 == 0)
2.  `adalah_ganjil` = **NOT** `adalah_genap`

**Tugas Anda:**

1.  Buat program yang meminta input `angka` (integer).
2.  Buat variabel `adalah_genap` yang mengecek apakah sisa bagi `angka` dengan `2` adalah `0`.
3.  Buat variabel `adalah_ganjil` dengan menggunakan operator `not` pada variabel `adalah_genap`.
4.  Cetak variabel `adalah_ganjil`.

**Contoh Uji:**

* Input 1: `angka` = 17
    * Output yang Diharapkan: `True`
* Input 2: `angka` = 20
    * Output yang Diharapkan: `False`

---

## Tugas 4: (Tantangan) Validasi Akses Ruang Server

**Skenario:**

Sebuah perusahaan memiliki aturan ketat untuk mengakses ruang server. Seseorang hanya boleh masuk jika:

1.  Dia adalah seorang "admin".
2.  *Atau*, dia adalah "teknisi" yang datang pada jam kerja (jam 8 pagi s.d. 17 sore, inklusif).

**Aturan Logika:**

Boleh Masuk = (`Level Akses` == "admin") **OR** ( (`Level Akses` == "teknisi") **AND** (`Jam Masuk` >= 8) **AND** (`Jam Masuk` <= 17) )

**Tugas Anda:**

1.  Minta input `level_akses` (string, misal: "admin", "teknisi", "user").
2.  Minta input `jam_masuk` (integer, 0-23).
3.  Buat satu variabel `boleh_masuk` yang berisi evaluasi logika dari aturan kompleks di atas.
4.  Cetak variabel `boleh_masuk`.

**Contoh Uji:**

* Input 1: `level_akses` = "admin", `jam_masuk` = 20
    * Output yang Diharapkan: `True` (Admin boleh masuk kapan saja)
* Input 2: `level_akses` = "teknisi", `jam_masuk` = 10
    * Output yang Diharapkan: `True` (Teknisi masuk di jam kerja)
* Input 3: `level_akses` = "teknisi", `jam_masuk` = 19
    * Output yang Diharapkan: `False` (Teknisi masuk di luar jam kerja)
* Input 4: `level_akses` = "user", `jam_masuk` = 14
    * Output yang Diharapkan: `False` (User tidak boleh masuk sama sekali)

---

Selamat mengerjakan!