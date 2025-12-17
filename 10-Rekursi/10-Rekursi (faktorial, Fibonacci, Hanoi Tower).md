# **Modul Praktikum 10: Rekursi (*Recursion*)**

Selamat datang di modul 10!

Jika sebelumnya kita menggunakan `for` atau `while` (Iterasi) untuk melakukan pengulangan, hari ini kita akan mempelajari cara melakukan pengulangan **tanpa loop**.

**Rekursi** adalah teknik pemrograman di mana sebuah fungsi **memanggil dirinya sendiri** untuk menyelesaikan masalah.

> *"To understand recursion, you must first understand recursion."*

**Tujuan Pembelajaran:**

1. Memahami konsep dasar fungsi rekursif.
2. Memahami dua komponen wajib rekursi: **Base Case** dan **Recursive Case**.
3. Membedakan penggunaan **Rekursi** vs **Iterasi** (Kelebihan & Kekurangan).
4. **Studi Kasus:** Menghitung Faktorial, Deret Fibonacci, dan Simulasi Menara Hanoi.

## **1. Konsep Dasar Rekursi**

Bayangkan boneka **[Matryoshka](https://id.wikipedia.org/wiki/Matrioska)** (boneka Rusia). Saat Anda membuka boneka besar, ada boneka lebih kecil di dalamnya. Anda terus membukanya sampai menemukan boneka terkecil yang tidak bisa dibuka lagi.

Dalam pemrograman:

1. **Recursive Case (Boneka Besar):** Fungsi memanggil dirinya sendiri dengan masalah yang lebih kecil.
2. **Base Case (Boneka Terkecil):** Kondisi berhenti agar fungsi tidak memanggil dirinya terus-menerus (mencegah *Infinite Loop* / *Stack Overflow*).

## **2. Studi Kasus 1: Faktorial (!)**

Faktorial adalah contoh klasik rekursi.
Rumus Matematis: 5! = 5 \times 4 \times 3 \times 2 \times 1
Atau bisa ditulis: 5! = 5 \times 4!

### **Implementasi Iteratif (Menggunakan Loop)**

```python
def faktorial_iteratif(n):
    hasil = 1
    for i in range(1, n + 1):
        hasil = hasil * i
    return hasil
```

### **Implementasi Rekursif**

```python
def faktorial_rekursif(n):
    # 1. Base Case: Kondisi berhenti
    if n == 1 or n == 0:
        return 1
    
    # 2. Recursive Case: Panggil diri sendiri
    else:
        return n * faktorial_rekursif(n - 1)

# Uji Coba
angka = 5
print(f"Faktorial dari {angka} adalah {faktorial_rekursif(angka)}")
```

**Penelusuran (Tracing) Logika:**

```
faktorial(5) memanggil 5 * faktorial(4)
    faktorial(4) memanggil 4 * faktorial(3)
        faktorial(3) memanggil 3 * faktorial(2)
            faktorial(2) memanggil 2 * faktorial(1)
                faktorial(1) mengembalikan 1 (Base Case!)
            faktorial(2) mengembalikan 2 * 1 = 2
        faktorial(3) mengembalikan 3 * 2 = 6
    faktorial(4) mengembalikan 4 * 6 = 24
faktorial(5) mengembalikan 5 * 24 = 120

```

## **3. Studi Kasus 2: Deret Fibonacci**

Deret Fibonacci: `0, 1, 1, 2, 3, 5, 8, 13, ...`
Rumus: Angka sekarang adalah penjumlahan dua angka sebelumnya.
F(n) = F(n-1) + F(n-2)

### **Implementasi Rekursif**

```python
def fibonacci(n):
    # Base Case: Suku ke-0 adalah 0, Suku ke-1 adalah 1
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    
    # Recursive Case
    else:
        return fibonacci(n - 1) + fibonacci(n - 2)

# Mencetak 10 deret pertama
jumlah_deret = 10
print(f"Deret Fibonacci ({jumlah_deret} angka):")
for i in range(jumlah_deret):
    print(fibonacci(i), end=" ")
```

**Diskusi:** 

Coba masukkan angka `40` ke dalam fungsi Fibonacci rekursif di atas. Apakah program terasa lambat? Mengapa? (Karena rekursi Fibonacci melakukan perhitungan yang sama berulang-ulang secara eksponensial).

## **4. Perbandingan: Rekursi vs Iterasi**

| Aspek | Iterasi (`for`/`while`) | Rekursi |
| --- | --- | --- |
| **Definisi** | Mengulang blok kode. | Fungsi memanggil dirinya sendiri. |
| **Kondisi Berhenti** | Kondisi `False` pada loop atau batas range. | **Base Case**. |
| **Penggunaan Memori** | Efisien (Kecil). | Besar (Menumpuk di *Stack Memory*). |
| **Kecepatan** | Biasanya lebih cepat. | Bisa lebih lambat (overhead panggilan fungsi). |
| **Keterbacaan Kode** | Bisa panjang dan rumit untuk masalah kompleks. | Lebih elegan, singkat, dan dekat dengan rumus matematika. |
| **Kapan Dipakai?** | Masalah linear sederhana. | Masalah percabangan pohon (*Tree*), graf, atau algoritma *Divide & Conquer*. |

## **5. Demonstrasi Lanjutan: Tower of Hanoi**

Menara Hanoi adalah teka-teki memindahkan tumpukan cakram dari tiang A ke tiang C dengan bantuan tiang B.

Aturan: Cakram besar tidak boleh diletakkan di atas cakram kecil.

Sangat sulit diselesaikan dengan Iterasi, tetapi sangat mudah dengan Rekursi.

**Logika Algoritma:**
Untuk memindahkan `n` cakram dari A ke C:

1. Pindahkan `n-1` cakram dari A ke B (Bantuan).
2. Pindahkan cakram terbesar (terbawah) dari A ke C (Tujuan).
3. Pindahkan `n-1` cakram dari B ke C.

```python
def hanoi(n, asal, bantuan, tujuan):
    if n == 1:
        print(f"Pindahkan cakram 1 dari {asal} ke {tujuan}")
        return
    
    # Langkah 1: Pindahkan n-1 dari Asal ke Bantuan
    hanoi(n - 1, asal, tujuan, bantuan)
    
    # Langkah 2: Pindahkan cakram terbesar ke Tujuan
    print(f"Pindahkan cakram {n} dari {asal} ke {tujuan}")
    
    # Langkah 3: Pindahkan n-1 dari Bantuan ke Tujuan
    hanoi(n - 1, bantuan, asal, tujuan)

# Jalankan simulasi untuk 3 cakram
print("--- Simulasi Tower of Hanoi (3 Cakram) ---")
hanoi(3, 'A', 'B', 'C')
```

## **6. Tugas Praktikum (Latihan Mandiri)**

1. **Pangkat Rekursif:**

Buatlah fungsi `pangkat_rekursif(bilangan, pangkat)` yang menghitung hasil perpangkatan tanpa menggunakan operator `**` atau fungsi `pow()`, melainkan menggunakan rekursi.
* Rumus: x^n = x \times x^{n-1}
* Base case: x^0 = 1


2. **Penjumlahan List Rekursif:**

Buatlah fungsi rekursif untuk menghitung total jumlah elemen dalam sebuah list angka.
* Input: `[10, 20, 30]`
* Logika: `10 + sum([20, 30])` -> dst.
* Jangan gunakan fungsi `sum()` bawaan Python.


## **Referensi**

* [Thinking Recursively in Python - Real Python](https://realpython.com/python-recursion/)
* [Visualisasi Rekursi (PythonTutor)](https://pythontutor.com/) - *Sangat disarankan untuk melihat bagaimana stack bekerja.*