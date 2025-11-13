# **UJIAN TENGAH SEMESTER (UTS)**

- **Mata Kuliah:** Algoritma dan Dasar Pemrograman
- **Keterangan:** Ujian ini mengevaluasi pemahaman konsep algoritma dasar (input, proses, output, logika) dan kemampuan implementasinya dalam bahasa pemrograman Python.

**Materi:**

  * Konsep Algoritmik (Input, Proses, Output)
  * Struktur Dasar Python: Variabel, Tipe Data, Konversi Tipe
  * Ekspresi dan Operator: Aritmatika, Penugasan, Pembanding, Logika
  * Logika Kondisional: Operator Ternary
  * Operasi Tingkat Lanjut: Operator Bitwise

**Petunjuk:**

1.  Baca setiap soal dengan teliti sebelum menjawab.
2.  Upload jawaban ke dalam folder `UTS` Sesuai Kelas melalui google drive
3.  Buat folder baru dengan nama "UTS_`NIM`" anda dan letakkan semua file jawaban Anda di dalam folder tersebut.
4.  Total skor adalah 100 poin.

-----

## **Bagian A: Pilihan Ganda (Bobot: 40 Poin)**

**Petunjuk:** Pilihlah satu (1) jawaban yang paling tepat.

1.  Dalam algoritma, proses menerima data dari pengguna disebut **Input**. Fungsi Python yang digunakan untuk implementasi ini, `input()`, secara *default* menghasilkan data dengan tipe?
    - A. `int`
    - B. `float`
    - C. `str` (String)
    - D. `bool`

2.  Manakah dari berikut ini yang merupakan nama **variabel** (penyimpan data) yang **tidak valid** dalam sintaks Python?
    - A. `_data_mahasiswa`
    - B. `totalNilai`
    - C. `nilai_uts`
    - D. `1_semester`

3.  Dalam banyak algoritma, kita perlu mencari "sisa bagi". Operator Python yang tepat untuk `13` dibagi `4` agar menghasilkan sisa `1` adalah:
    - A. `/`
    - B. `//`
    - C. `%`
    - D. `**`

4.  Perhatikan kode berikut, yang merepresentasikan proses akumulasi nilai:

    ```python
    x = 10
    x += 5
    ```

    Berapakah nilai akhir `x` setelah proses dieksekusi?
    A. `5`
    B. `10`
    C. `15`
    D. `Error`

5.  Manakah dari ekspresi logika berikut yang akan dievaluasi menjadi `True`?
    - A. `(10 > 5) and (5 > 10)`
    - B. `(10 == "10")`
    - C. `(5 != 5) or (10 < 100)`
    - D. `not (True)`

6.  Apa hasil dari operasi `13 // 4` (pembagian bulat)?
    - A. `3`
    - B. `3.25`
    - C. `1`
    - D. `4`

7.  Operator Ternary adalah bentuk ringkas dari algoritma kondisional (Jika-Maka-Lainnya). Perhatikan:

    ```python
    skor = 70
    status = "Lulus" if skor >= 75 else "Remedial"
    ```

    Apa nilai dari variabel `status`?
    - A. `Lulus`
    - B. `Remedial`
    - C. `70`
    - D. `True`

8.  Apa hasil dari operasi bitwise `10 & 12`? (Biner 10: `1010`, Biner 12: `1100`)
    - A. `8` (Biner: `1000`)
    - B. `14` (Biner: `1110`)
    - C. `6` (Biner: `0110`)
    - D. `2` (Biner: `0010`)

9.  Apa hasil dari operasi bitwise `10 | 12`? (Biner 10: `1010`, Biner 12: `1100`)
    - A. `8` (Biner: `1000`)
    - B. `14` (Biner: `1110`)
    - C. `6` (Biner: `0110`)
    - D. `2` (Biner: `0010`)

10. Apa hasil dari operasi bitwise `5 << 1` (Geser Kiri)?
    - A. `2`
    - B. `10`
    - C. `5`
    - D. `2.5`

-----

## **Bagian B: Esai Singkat & Analisis Algoritma (Bobot: 30 Poin)**

**Petunjuk:** Jawablah pertanyaan berikut dengan singkat dan jelas.

1.  **Jelaskan** perbedaan fundamental antara operator `==` (pembanding) dan `=` (penugasan) dalam konteks algoritma dan pemrograman. Berikan contoh implementasinya di Python.

2.  **Konversikan** algoritma kondisional (percabangan) berikut menjadi satu baris ekspresi menggunakan **Operator Ternary** di Python.

    ```python
    # Algoritma Awal
    umur = 17

    if umur < 17:
        keterangan = "Belum Cukup Umur"
    else:
        keterangan = "Sudah Cukup Umur"
    ```

    *Tuliskan jawaban Anda dalam satu baris kode.*

3.  **Jelaskan** sebuah skenario algoritma di mana Anda harus menggunakan operator logika `or`. Kemudian, jelaskan skenario lain di mana Anda harus menggunakan operator logika `and`.

-----

## **Bagian C: Studi Kasus Implementasi Algoritma (Bobot: 30 Poin)**

**Petunjuk:** Rancang dan tuliskan program Python lengkap untuk memecahkan masalah berikut.

**Skenario: Algoritma Seleksi Karyawan**

Sebuah perusahaan menetapkan algoritma seleksi untuk calon karyawan baru. Calon dianggap **DITERIMA** jika memenuhi **semua** kondisi berikut:

1.  Nilai tes potensi akademik (TPA) **minimal 80**.
2.  Nilai tes wawancara (HR) **minimal 75**.
3.  Calon **TIDAK** buta warna (direpresentasikan dengan `False`).

**Tugas Anda:**

1.  Buatlah program yang meminta 3 input dari pengguna:
      * `nilai_tpa` (sebagai integer)
      * `nilai_wawancara` (sebagai integer)
      * `apakah_buta_warna` (sebagai string, misal: "ya" atau "tidak")
2.  Lakukan konversi tipe data yang sesuai. (Ubah input "ya" menjadi `True` dan "tidak" menjadi `False`).
3.  Buat satu variabel boolean bernama `diterima` yang berisi **ekspresi logika** untuk mengevaluasi ketiga syarat di atas menggunakan operator yang tepat.
4.  Cetak hasil akhir dari variabel `diterima` (`True` jika lolos, `False` jika tidak).

**Contoh Output 1:**

```
Masukkan nilai TPA: 85
Masukkan nilai Wawancara: 80
Apakah buta warna (ya/tidak): tidak

Status Diterima: True
```

**Contoh Output 2:**

```
Masukkan nilai TPA: 85
Masukkan nilai Wawancara: 80
Apakah buta warna (ya/tidak): ya

Status Diterima: False
```

-----

## **SELAMAT MENGERJAKAN\!**