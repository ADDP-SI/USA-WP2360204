# **Modul Praktikum 8: Algoritma Pengurutan (*Sorting*)**

Selamat datang di modul kedelapan! 

Pernahkah Anda melihat daftar kontak di HP Anda yang berantakan? Atau daftar harga di Tokopedia yang tidak urut? Tentu akan sulit mencari barang termurah.

**Pengurutan (Sorting)** adalah proses menyusun kembali elemen-elemen dalam daftar (list) berdasarkan urutan tertentu (biasanya numerik atau alfabetis), baik dari kecil ke besar (*Ascending*) atau besar ke kecil (*Descending*).

**Tujuan Pembelajaran:**

1. Memahami logika di balik bagaimana komputer mengurutkan data.
2. Mampu mengimplementasikan algoritma **Bubble Sort**.
3. Mampu mengimplementasikan algoritma **Selection Sort**.
4. Mampu mengimplementasikan algoritma **Insertion Sort**.
5. Memahami konsep efisiensi algoritma secara sederhana.
6. **Studi Kasus:** Program Pengurutan Nilai Ujian Mahasiswa.

## **1. Bubble Sort (Metode Gelembung) 🫧**

Ini adalah algoritma yang paling sederhana namun juga paling lambat untuk data besar.

**Konsep:**

Bayangkan gelembung udara di air yang naik ke permukaan. Algoritma ini bekerja dengan **membandingkan dua elemen yang bersebelahan** secara berulang-ulang dan menukarnya (swap) jika urutannya salah. Elemen terbesar akan "mengapung" ke posisi paling kanan pada setiap putaran.

**Visualisasi Logika:** `[5, 1, 4, 2]`

1. Bandingkan 5 & 1 -> Tukar -> `[1, 5, 4, 2]`
2. Bandingkan 5 & 4 -> Tukar -> `[1, 4, 5, 2]`
3. Bandingkan 5 & 2 -> Tukar -> `[1, 4, 2, 5]` (5 sudah di posisi benar)
4. Ulangi lagi dari depan untuk sisa angka.

**Implementasi Python:**

```python
def bubble_sort(data):
    n = len(data)
    # Loop untuk setiap elemen
    for i in range(n):
        # Loop untuk membandingkan elemen bersebelahan
        # (n-i-1) karena bagian belakang sudah pasti urut
        for j in range(0, n - i - 1):
            if data[j] > data[j + 1]:
                # Tukar posisi (Swap)
                data[j], data[j + 1] = data[j + 1], data[j]
    return data

nilai = [64, 34, 25, 12, 22, 11, 90]
print(f"Bubble Sort: {bubble_sort(nilai)}")
```

## **2. Selection Sort (Metode Seleksi)**

Algoritma ini bekerja dengan mencari elemen **terkecil** (atau terbesar) dari daftar yang belum urut, lalu menukarnya dengan elemen di posisi awal.

**Konsep:**

1. Cari angka terkecil di seluruh list.
2. Tukar angka terkecil tersebut ke posisi indeks ke-0.
3. Cari angka terkecil lagi dari sisa list (indeks 1 sampai akhir).
4. Tukar ke posisi indeks ke-1.
5. Ulangi.

**Implementasi Python:**

```python
def selection_sort(data):
    n = len(data)
    for i in range(n):
        # Anggap elemen ke-i adalah yang terkecil sementara
        min_idx = i
        
        # Cari yang lebih kecil di sisa list sebelah kanan
        for j in range(i + 1, n):
            if data[j] < data[min_idx]:
                min_idx = j
        
        # Tukar elemen terkecil yang ditemukan dengan elemen ke-i
        data[i], data[min_idx] = data[min_idx], data[i]
    return data

nilai = [64, 34, 25, 12, 22, 11, 90]
print(f"Selection Sort: {selection_sort(nilai)}")
```
## **3. Insertion Sort (Metode Penyisipan)**

Algoritma ini mirip dengan cara orang mengurutkan **kartu remi** di tangan.

**Konsep:**
Kita membagi list menjadi dua bagian: bagian kiri (sudah urut) dan bagian kanan (belum urut). Kita ambil satu elemen dari kanan, lalu **sisipkan** ke posisi yang tepat di bagian kiri.

**Implementasi Python:**

```python
def insertion_sort(data):
    for i in range(1, len(data)):
        key = data[i] # Elemen yang akan disisipkan
        j = i - 1
        
        # Geser elemen yang lebih besar dari key ke kanan
        while j >= 0 and key < data[j]:
            data[j + 1] = data[j]
            j -= 1
        
        # Letakkan key di posisi yang kosong
        data[j + 1] = key
    return data

nilai = [64, 34, 25, 12, 22, 11, 90]
print(f"Insertion Sort: {insertion_sort(nilai)}")
```

## **4. Diskusi: Efisiensi Algoritma**

Dalam ilmu komputer, kita mengukur efisiensi dengan **Big O Notation**.

* Ketiga algoritma di atas (Bubble, Selection, Insertion) memiliki kompleksitas waktu **O(n^2)**.
* **Artinya:** Jika data bertambah 10 kali lipat, waktu yang dibutuhkan bertambah 100 kali lipat (10^2).
* **Kesimpulan:** Algoritma ini bagus untuk belajar logika dan data jumlah kecil (< 1.000), tapi sangat lambat untuk data besar.

* *Catatan:* Python memiliki fungsi bawaan `.sort()` yang menggunakan algoritma **Timsort** (gabungan Merge Sort & Insertion Sort) yang jauh lebih cepat (O(n \log n)). Namun, di mata kuliah ini, kita wajib belajar cara membuatnya secara manual.

## **5. Studi Kasus: Pengurutan Nilai Ujian Mahasiswa**

**Tugas Praktikum:**

Anda adalah seorang asisten dosen. Anda memiliki tumpukan nilai ujian mahasiswa yang masih acak. Dosen meminta Anda mengurutkan nilai tersebut dari yang **tertinggi ke terendah (Descending)** agar mudah menentukan ranking.

**Instruksi:**

1. Buatlah list berisi nilai acak: `[78, 90, 56, 98, 75, 80, 45, 92]`.
2. Pilih **SATU** algoritma pengurutan manual (Bubble, Selection, atau Insertion).
3. Modifikasi kodenya agar mengurutkan secara **Descending** (Besar ke Kecil).
* *Petunjuk:* Ubah tanda perbandingannya (misal dari `<` menjadi `>`).


4. Tampilkan nilai sebelum dan sesudah diurutkan.
5. Tampilkan nilai tertinggi (Ranking 1) dan terendah.

**Contoh Solusi (Menggunakan Bubble Sort Descending):**

```python
def urutkan_nilai_descending(data):
    n = len(data)
    for i in range(n):
        for j in range(0, n - i - 1):
            # Perhatikan tanda '<' untuk Descending
            if data[j] < data[j + 1]: 
                # Tukar posisi
                data[j], data[j + 1] = data[j + 1], data[j]
    return data

# Program Utama
nilai_ujian = [78, 90, 56, 98, 75, 80, 45, 92]

print(f"Nilai Awal    : {nilai_ujian}")

# Proses Sorting
nilai_urut = urutkan_nilai_descending(nilai_ujian)

print("-" * 40)
print(f"Nilai Urut (Ranking): {nilai_urut}")
print(f"Nilai Tertinggi     : {nilai_urut[0]}")
print(f"Nilai Terendah      : {nilai_urut[-1]}"
```

## **Tugas Latihan Mandiri**

Cobalah gunakan algoritma **Insertion Sort** untuk mengurutkan nama-nama mahasiswa berikut sesuai abjad (A-Z):
`nama = ["Zainab", "Budi", "Andi", "Siti", "Doni"]`

*Tips:* Python bisa membandingkan string sama seperti angka (`"Andi" < "Budi"` bernilai `True`).


## **Referensi**

* [Visualisasi Sorting Algorithms (Visualgo.net)](https://visualgo.net/en/sorting) - *Sangat disarankan untuk dilihat saat praktikum.*
* [Sorting Algorithms in Python - Real Python](https://realpython.com/sorting-algorithms-python/)