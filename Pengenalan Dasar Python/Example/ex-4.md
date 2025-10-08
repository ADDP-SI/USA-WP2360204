# Penjelasan Detail Kode: Sistem Data Mahasiswa

## **Deskripsi Program**
Program ini adalah sistem sederhana untuk menyimpan dan menampilkan data mahasiswa baru menggunakan berbagai tipe data Python.

---

## **Penjelasan Baris per Baris**

### 1. **Dokumentasi Program**
```python
"""
Buat program sederhana untuk menyimpan data mahasiswa baru
"""
```
- **Fungsi**: Memberikan penjelasan tentang tujuan program
- **Best Practice**: Selalu gunakan docstring untuk dokumentasi

### 2. **Variabel dan Tipe Data**

#### **String (Text)**
```python
nama_mahasiswa = "Jhon Doe"
nim = "202507001"
```
- **Tipe Data**: `str` (string)
- **Fungsi**: Menyimpan data teks
- **Contoh**: Nama, NIM, alamat, dll.
- **Ciri**: Diapit tanda kutip (`" "` atau `' '`)

#### **Integer (Bilangan Bulat)**
```python
usia = 19
```
- **Tipe Data**: `int`
- **Fungsi**: Menyimpan bilangan bulat
- **Contoh**: Usia, jumlah, tahun, dll.
- **Ciri**: Tidak ada koma/desimal

#### **Float (Bilangan Desimal)**
```python
tinggi_badan = 170.5
```
- **Tipe Data**: `float`
- **Fungsi**: Menyimpan bilangan desimal
- **Contoh**: Tinggi badan, berat badan, nilai IPK, dll.
- **Ciri**: Menggunakan titik desimal

#### **Boolean (True/False)**
```python
aktif = True
```
- **Tipe Data**: `bool`
- **Fungsi**: Menyimpan nilai kebenaran
- **Nilai**: `True` atau `False`
- **Contoh**: Status aktif, lulus, terdaftar, dll.

#### **List (Daftar)**
```python
mata_kuliah = ["Algoritma dan Dasar Pemrograman", "Bahasa Indonesia", "Sistem Operasi"]
```
- **Tipe Data**: `list`
- **Fungsi**: Menyimpan kumpulan data
- **Ciri**: Diapit `[ ]`, elemen dipisah koma
- **Contoh**: Daftar mata kuliah, nilai, hobbi, dll.

---

##  *Bagian Output*

### 3. **Menampilkan Data**
```python
print("=== DATA MAHASISWA ===")
```
- **Fungsi**: Menampilkan judul/tanda
- **Output**: 
  ```
  === DATA MAHASISWA ===
  ```

### 4. **Formatted String (f-string)**
```python
print(f"Nama: {nama_mahasiswa} (tipe: {type(nama_mahasiswa)})")
```
- **Struktur**: `f"text {variabel} text"`
- **Fungsi**: Menyisipkan nilai variabel dalam string
- **`type()`**: Fungsi untuk mengecek tipe data
- **Output**:
  ```
  Nama: Budi Santoso (tipe: <class 'str'>)
  ```

---

##  *Contoh Output Lengkap*
```
=== DATA MAHASISWA ===
Nama: Budi Santoso (tipe: <class 'str'>)
NIM: 202407001 (tipe: <class 'str'>)
Usia: 19 tahun (tipe: <class 'int'>)
Tinggi Badan: 170.5 cm (tipe: <class 'float'>)
Status Aktif: True (tipe: <class 'bool'>)
Mata Kuliah: ['Matematika', 'Fisika', 'Pemrograman'] (tipe: <class 'list'>)
```

---

##  *Konsep Python yang Dipelajari*

### 1. **Dynamic Typing**
- Python menentukan tipe data secara otomatis
- Tidak perlu deklarasi tipe data explisit

### 2. **Variable Assignment**
```python
nama_variabel = nilai
```

### 3. **Built-in Functions**
- `print()`: Menampilkan output
- `type()`: Mengecek tipe data

### 4. **String Formatting**
- f-string untuk template yang rapi

---

##  *Modifikasi & Eksperimen*

Coba ubah nilai variabel dan amati perubahannya:

```python
# Modifikasi nilai
usia = 20                        # Ubah integer
tinggi_badan = 175.0            # Ubah float
aktif = False                   # Ubah boolean
mata_kuliah.append("Bahasa")    # Tambah item list

# Atau ubah tipe data
usia = "dua puluh"              # Integer → String
```

---

##  *Pelajaran yang Didapat*

1. ✅ Memahami 5 tipe data dasar Python
2. ✅ Cara membuat dan menggunakan variabel
3. ✅ Teknik menampilkan output yang informatif
4. ✅ Cara memeriksa tipe data variabel
5. ✅ Penggunaan f-string untuk formatting

Program ini menjadi fondasi untuk memahami bagaimana Python menyimpan dan memanipulasi data!