
# **Tipe Data**

Setiap nilai yang disimpan dalam variabel memiliki **tipe data**. Tipe data menentukan jenis nilai tersebut dan operasi apa saja yang bisa dilakukan padanya. Python secara otomatis mengenali tipe data saat Anda memberikan nilai ke variabel (*dynamic typing*).

### Berikut adalah tipe data dasar yang paling umum:

  * **String (`str`)**: Teks atau kumpulan karakter. Ditulis dengan tanda kutip tunggal (`'...'`) atau ganda (`"..."`).
      * Contoh: `"Halo Dunia"`, `'Python 101'`
  * **Integer (`int`)**: Bilangan bulat, tanpa desimal.
      * Contoh: `10`, `-5`, `2023`
  * **Float (`float`)**: Bilangan desimal atau pecahan.
      * Contoh: `3.14`, `99.9`, `-0.5`
  * **Boolean (`bool`)**: Hanya memiliki dua nilai, `True` atau `False`. Biasanya digunakan untuk menyatakan kondisi.

### **Contoh Kode & Pengecekan Tipe Data:**

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

### **Latihan 2:**

Buat sebuah variabel bernama `suhu_celcius` dengan nilai `27.5`. Periksa dan cetak tipe datanya. Kemudian, coba ubah nilai variabel tersebut menjadi sebuah teks (misalnya, `"dua puluh tujuh"`) dan periksa kembali tipe datanya. Amati perubahannya.

### **Latihan 3:**

Sistem Pendaftaran Mahasiswa

```python
"""
Buat program sederhana untuk menyimpan data mahasiswa baru
"""

# Data mahasiswa
nama_mahasiswa = "John Doe"
nim = "202507001"
usia = 19
tinggi_badan = 170.5
aktif = True
mata_kuliah = ["Algoritma dan Dasar Pemrograman", "Bahasa Indonesia", "Sistem Operasi"]

print("=== DATA MAHASISWA ===")
print(f"Nama: {nama_mahasiswa} (tipe: {type(nama_mahasiswa)})")
print(f"NIM: {nim} (tipe: {type(nim)})")
print(f"Usia: {usia} tahun (tipe: {type(usia)})")
print(f"Tinggi Badan: {tinggi_badan} cm (tipe: {type(tinggi_badan)})")
print(f"Status Aktif: {aktif} (tipe: {type(aktif)})")
print(f"Mata Kuliah: {mata_kuliah} (tipe: {type(mata_kuliah)})")

```
 ### Tugas Tambahan untuk Dipraktikkan:

- Modifikasi setiap program dengan menambahkan data baru
- Ubah `tipe data` beberapa `variabel` dan amati efeknya
- Buat program baru dengan konsep yang sama untuk kasus berbeda