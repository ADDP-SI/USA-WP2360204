# **Modul Praktikum 4: Struktur Kontrol Perulangan**

Selamat datang di modul keempat\! Setelah kita belajar bagaimana program bisa "memilih" jalur (percabangan), sekarang kita akan belajar bagaimana program bisa **mengulang** tugas secara otomatis. Ini adalah salah satu konsep paling kuat dalam pemrograman, yang memungkinkan kita melakukan ribuan operasi hanya dengan beberapa baris kode.

**Struktur Kontrol Perulangan** (atau *Loops*) digunakan untuk mengeksekusi satu blok kode berulang kali selama kondisi tertentu masih terpenuhi.

**Tujuan Pembelajaran:**

1.  Memahami konsep **iterasi** (perulangan) dan kebutuhannya dalam algoritma.
2.  Mampu mengimplementasikan perulangan `for` untuk iterasi yang terhitung (pasti).
3.  Mampu mengimplementasikan perulangan `while` untuk iterasi yang tidak terhitung (selama kondisi terpenuhi).
4.  Mampu mengimplementasikan **perulangan bersarang** (*nested loops*) untuk kasus yang lebih kompleks.
5.  Menerapkan logika perulangan untuk memecahkan studi kasus (Tabel Perkalian & Deret Bilangan).

-----

## **1. Perulangan `for` (Perulangan Terhitung)**

Perulangan `for` digunakan ketika kita **sudah tahu pasti** berapa kali kita ingin mengulang sebuah blok kode.

**Analogi:** Seperti instruktur senam yang berkata, "Lompat 10 kali\!" Anda tahu persis kapan harus memulai dan kapan harus berhenti.

Di Python, `for` sering digunakan bersama fungsi `range()` untuk menghasilkan urutan angka.

**Sintaks:**

```python
for variabel_iterasi in range(jumlah_perulangan):
    # Blok kode yang akan diulang
    pernyataan_1

# Menggunakan range(start, stop, step)
# range(1, 11) -> 1, 2, 3, 4, 5, 6, 7, 8, 9, 10
# range(0, 10, 2) -> 0, 2, 4, 6, 8
```

### **Contoh 1: Menghitung 1 sampai 5**

```python
print("Memulai hitungan:")

for i in range(1, 6): # range(1, 6) berarti 1, 2, 3, 4, 5
    print(f"Hitungan ke-{i}")

print("Selesai!")
```

### **Contoh (Studi Kasus): Program Deret Bilangan**

Mari kita buat program untuk mencetak semua bilangan genap dari 1 sampai 20.

```python
print("--- Deret Bilangan Genap (1-20) ---")

# Kita mulai dari 2 (genap pertama)
# Kita berhenti di 21 (agar 20 ikut)
# Kita melompat 2 langkah (step=2)
for angka in range(2, 21, 2):
    print(angka)
```

**Diskusi:** Bagaimana jika kita ingin mencetak bilangan *ganjil*? Apa yang akan Anda ubah dari kode `range()` di atas?

-----

## **2. Perulangan `while` (Perulangan Tak Terhitung)**

Perulangan `while` digunakan ketika kita ingin mengulang kode **selama (while)** sebuah kondisi bernilai `True`. Kita tidak tahu pasti berapa kali perulangan akan terjadi, tapi kita tahu kapan harus berhenti.

**Analogi:** Seperti bermain game, "Terus main **selama** nyawa kamu masih di atas 0."

**Sintaks:**

```python
# (1) Inisialisasi variabel kondisi
variabel_kondisi = nilai_awal

while kondisi: # (2) Pengecekan kondisi
    # Blok kode yang akan diulang
    pernyataan_1
    
    # (3) Pembaruan variabel kondisi (PENTING!)
    variabel_kondisi = nilai_baru
```

> **Peringatan:** Jika Anda lupa bagian (3) atau pembaruan tidak pernah membuat kondisi menjadi `False`, program Anda akan mengalami **Infinite Loop** (perulangan tak berakhir) dan harus dihentikan paksa\!

### **Contoh 3: `while` vs `for`**

Mari kita buat ulang "Menghitung 1 sampai 5" menggunakan `while`.

```python
print("Memulai hitungan (versi while):")
i = 1 # (1) Inisialisasi

while i <= 5: # (2) Kondisi
    print(f"Hitungan ke-{i}")
    i += 1 # (3) Pembaruan (i = i + 1)

print("Selesai!")
```

**Diskusi:** Kapan sebaiknya kita pakai `for` dan kapan pakai `while`? (Singkat: `for` untuk hitungan pasti, `while` untuk kondisi, misal `while input_user != 'keluar'`).

-----

## **3. Perulangan Bersarang (*Nested Loops*)**

*Nested Loop* adalah perulangan di dalam perulangan. Ini sangat umum digunakan untuk bekerja dengan data dua dimensi, seperti tabel, matriks, atau membuat pola.

**Analogi:** Seperti jarum jam. Untuk setiap 1 putaran jarum jam (loop luar), jarum menit (loop dalam) harus berputar 60 kali.

### **Contoh 4 (Studi Kasus): Program Tabel Perkalian**

Ini adalah studi kasus klasik untuk *nested loop*. Kita ingin mencetak tabel perkalian dari 1 sampai 10.

```python
print("--- Tabel Perkalian (1-10) ---")

# Loop Luar: Mengatur perkalian ke-i (Perkalian 1, Perkalian 2, dst)
for i in range(1, 11):
    print(f"\n=== Perkalian {i} ===")
    
    # Loop Dalam: Mengatur pengali ke-j (i * 1, i * 2, dst)
    for j in range(1, 11):
        hasil = i * j
        # print(f"{i} x {j} = {hasil}")
        
        # Menggunakan \t (tab) agar lebih rapi
        print(f"{i} x {j} = {hasil}", end="\t|\t") 
    print() # Pindah baris setelah satu tabel selesai
```

**Diskusi:** Perhatikan bagaimana `j` (loop dalam) harus menyelesaikan seluruh putarannya (1-10) sebelum `i` (loop luar) bisa berpindah ke angka berikutnya.

-----

## **Latihan Praktikum**

Sekarang, coba terapkan konsep perulangan untuk memecahkan masalah berikut.

### **Latihan 1: Deret Fibonacci Sederhana**

Buatlah program yang mencetak **10 angka pertama** dari deret Fibonacci.

  * Deret Fibonacci adalah deret di mana angka berikutnya adalah jumlah dari dua angka sebelumnya.
  * Dimulai dengan `0` dan `1`.
  * **Output yang Diharapkan:** `0, 1, 1, 2, 3, 5, 8, 13, 21, 34`

**Petunjuk:**

1.  Buat dua variabel awal, misal `a = 0` dan `b = 1`.
2.  Cetak `a` dan `b` terlebih dahulu.
3.  Gunakan perulangan `for` untuk 8 kali sisanya (`range(8)`).
4.  Di dalam loop: hitung `c = a + b`, cetak `c`, lalu "geser" nilainya: `a = b` dan `b = c`.

### **Latihan 2: Pola Bintang (Nested Loop)**

Buatlah program menggunakan *nested loop* untuk menghasilkan output pola segitiga siku-siku seperti di bawah ini:

```
*
**
***
****
*****
```

**Petunjuk:**

1.  Gunakan loop luar (misal, `i`) untuk menentukan jumlah baris (misal, 5 baris).
2.  Gunakan loop dalam (misal, `j`) untuk mencetak bintang di baris tersebut.
3.  Jumlah bintang yang dicetak di loop dalam harus sama dengan nomor baris saat ini (`i`).

-----

## **Referensi**

  * Dokumentasi Resmi Python - `for` Statements: [https://docs.python.org/3/tutorial/controlflow.html\#for-statements](https://www.google.com/search?q=https://docs.python.org/3/tutorial/controlflow.html%23for-statements)
  * Dokumentasi Resmi Python - `while` Statements: [https://docs.python.org/3/tutorial/controlflow.html\#while-statements](https://www.google.com/search?q=https://docs.python.org/3/tutorial/controlflow.html%23while-statements)
  * W3Schools - Python Loops: [https://www.w3schools.com/python/python\_loops.asp](https://www.google.com/search?q=https://www.w3schools.com/python/python_loops.asp)