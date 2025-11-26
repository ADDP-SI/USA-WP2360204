# **Modul Praktikum 7: Struktur Data Dasar (List & Tuple)**

Selamat datang di modul ketujuh\! Hingga saat ini, kita telah menggunakan variabel (seperti `nilai = 80`) untuk menyimpan **satu** data. Namun, dalam algoritma, kita seringkali perlu menyimpan **kumpulan** data.

Bayangkan Anda harus menyimpan 100 nilai mahasiswa. Apakah Anda akan membuat 100 variabel (`nilai1`, `nilai2`, `nilai3`, ...)? Tentu tidak. Di sinilah **Struktur Data** berperan. Kita akan fokus pada dua yang paling dasar di Python: **List** dan **Tuple**.

**Tujuan Pembelajaran:**

1.  Memahami konsep struktur data sebagai "wadah" untuk banyak nilai.
2.  Mampu menggunakan **List** (struktur yang *mutable*/bisa diubah) untuk menyimpan dan memanipulasi data.
3.  Mampu menggunakan **Tuple** (struktur yang *immutable*/tidak bisa diubah) untuk menyimpan data yang bersifat tetap.
4.  Mampu menerapkan List dan perulangan untuk membuat program studi kasus (Input Nilai Mahasiswa).

-----

## **1. List: "Rak" Data yang Fleksibel 🗃️**

**List** adalah struktur data yang paling umum di Python. Anggap saja ini seperti rak buku atau daftar belanja.

  * Didefinisikan menggunakan **kurung siku `[ ]`**.
  * **Mutable:** Isinya bisa diubah, ditambah, atau dihapus setelah dibuat.
  * **Ordered:** Urutan datanya tetap (item pertama akan selalu jadi item pertama).
  * Bisa berisi berbagai tipe data (meski biasanya kita simpan tipe yang seragam).

**Cara Membuat & Mengakses List:**

```python
# Membuat list
nilai_ulangan = [80, 95, 75, 100, 60]
nama_buah = ["Apel", "Jeruk", "Mangga"]
campuran = ["Budi", 90, True]

# Mengakses data (Indexing - Dimulai dari 0!)
print(f"Nilai ulangan pertama: {nilai_ulangan[0]}") # Output: 80
print(f"Nama buah ketiga: {nama_buah[2]}")      # Output: Mangga
print(f"Nilai ulangan terakhir: {nilai_ulangan[-1]}") # -1 berarti dari belakang
```

**Memanipulasi List (Karena Mutable):**

```python
# 1. Mengubah nilai
nilai_ulangan[0] = 85 # Mengganti nilai 80 menjadi 85
print(f"List setelah diubah: {nilai_ulangan}")

# 2. Menambah data ke akhir list (SANGAT PENTING!)
nilai_ulangan.append(90)
print(f"List setelah ditambah: {nilai_ulangan}")

# 3. Mengetahui panjang list
jumlah_data = len(nilai_ulangan)
print(f"Ada {jumlah_data} nilai di dalam list.")
```

-----

## **2. Tuple: "Kotak" Data yang Disegel**

**Tuple** (dibaca: *tapel* atau *tupel*) sangat mirip dengan List, tapi dengan satu perbedaan KUNCI.

  * Didefinisikan menggunakan **kurung biasa `( )`**.
  * **Immutable:** Isinya **TIDAK BISA DIUBAH** setelah dibuat.
  * **Ordered:** Urutannya tetap.

**Kapan Menggunakan Tuple?**
Saat Anda memiliki data yang *pasti* dan *tidak boleh* berubah. Contoh: koordinat (x, y), data warna RGB (Red, Green, Blue), atau konfigurasi yang bersifat tetap.

**Cara Membuat & Mengakses Tuple:**

```python
# Membuat tuple
koordinat_xy = (10, 20)
warna_merah_rgb = (255, 0, 0)
hari_dalam_seminggu = ("Senin", "Selasa", "Rabu", "Kamis", "Jumat", "Sabtu", "Minggu")

# Mengakses data (Sama seperti List, pakai indeks 0)
print(f"Nilai x: {koordinat_xy[0]}") # Output: 10
print(f"Hari pertama: {hari_dalam_seminggu[0]}") # Output: Senin
```

**Perbedaan Kunci (Immutable):**

```python
# Jika kita coba mengubah data tuple, akan terjadi ERROR
# koordinat_xy[0] = 5 # Baris ini akan error (TypeError)

# Tuple juga tidak punya metode .append()
# koordinat_xy.append(30) # Baris ini juga akan error (AttributeError)
```

-----

## **3. Melakukan Perulangan pada List/Tuple**

Cara paling umum untuk memproses setiap item dalam List atau Tuple adalah menggunakan perulangan `for`.

```python
nilai_ulangan = [80, 95, 75, 100, 60]

print("--- Daftar Nilai ---")
# Loop akan mengambil setiap item satu per satu
for nilai in nilai_ulangan:
    print(f"Nilai: {nilai}")
```

-----

## **4. Praktikum (Studi Kasus): Program Input Nilai Mahasiswa**

Ini adalah tugas inti kita. Kita akan membuat program yang:

1.  Menjadi "wadah" kosong untuk menampung nilai (kita pakai **List**).
2.  Bertanya kepada pengguna berapa banyak nilai yang ingin dimasukkan.
3.  Melakukan **perulangan** sebanyak itu, meminta nilai, dan **memasukkan (`append`)** nilai itu ke List.
4.  Setelah semua nilai terkumpul, hitung total dan rata-ratanya.

### **Contoh: Menghitung Rata-rata**

```python
print("--- Program Perhitungan Rata-rata Nilai ---")

# 1. Buat "wadah" kosong (List kosong)
daftar_nilai = []

# 2. Tanya berapa data yang akan dimasukkan
try:
    jumlah_data = int(input("Berapa jumlah nilai yang akan dimasukkan? "))
except ValueError:
    print("Input tidak valid, harus angka.")
    exit() # Keluar dari program jika input salah

# 3. Lakukan perulangan untuk input
print("-" * 20)
for i in range(jumlah_data):
    # 'i+1' agar hitungan dimulai dari 1 (lebih user-friendly)
    while True: # Loop kecil untuk validasi input
        try:
            nilai = float(input(f"Masukkan nilai ke-{i + 1}: "))
            daftar_nilai.append(nilai) # Masukkan nilai ke list
            break # Keluar dari loop validasi jika sukses
        except ValueError:
            print("Input salah! Masukkan angka.")

# 4. Proses data setelah loop selesai
print("-" * 20)
print(f"Data nilai yang terkumpul: {daftar_nilai}")

# Menghitung total (Python punya cara mudah!)
total_nilai = sum(daftar_nilai)
print(f"Total semua nilai: {total_nilai}")

# Menghitung jumlah data (bisa juga pakai 'jumlah_data')
jumlah_nilai_terkumpul = len(daftar_nilai)

# Menghitung rata-rata
if jumlah_nilai_terkumpul > 0:
    rata_rata = total_nilai / jumlah_nilai_terkumpul
    # :.2f artinya format menjadi 2 angka di belakang koma
    print(f"Rata-rata nilai: {rata_rata:.2f}") 
else:
    print("Tidak ada data untuk dihitung rata-ratanya.")

```

## **5. Diskusi Kelompok**

Diskusikan pertanyaan-pertanyaan berikut dengan kelompok Anda:

1.  **Mengapa** pada studi kasus di atas kita menggunakan **List** dan bukan **Tuple**?
      * *(Jawaban petunjuk: Apakah kita perlu menambah data saat program berjalan?)*
2.  Bagaimana cara kita (tanpa menggunakan fungsi `sum()`) menghitung `total_nilai` menggunakan perulangan `for`?
      * *(Petunjuk: Buat variabel `total = 0` sebelum loop...)*
3.  Bagaimana cara program di atas diubah agar dapat menemukan **nilai tertinggi** dan **nilai terendah** dari list `daftar_nilai`?
      * *(Petunjuk: Python punya fungsi `max()` dan `min()`)*.
4.  Apa yang akan terjadi jika kita mencoba mengakses `daftar_nilai[10]` padahal kita hanya memasukkan 3 nilai? (Istilah untuk error ini adalah...).

-----

## **Referensi**

  * Dokumentasi Resmi Python - Lists: [https://docs.python.org/3/tutorial/datastructures.html](https://docs.python.org/3/tutorial/datastructures.html)
  * W3Schools - Python Lists: [https://www.w3schools.com/python/python\_lists.asp](https://www.w3schools.com/python/python_lists.asp)
  * W3Schools - Python Tuples: [https://www.w3schools.com/python/python\_tuples.asp](https://www.w3schools.com/python/python_tuples.asp)