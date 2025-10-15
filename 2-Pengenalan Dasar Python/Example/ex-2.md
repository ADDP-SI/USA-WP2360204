```python
def tampilkan_produk(nama, harga, stok):
    # Menampilkan nama produk
    print(f"Nama Produk     : {nama}")
    # Menampilkan harga produk dengan format ribuan (misal: 15,000,000)
    print(f"Harga           : Rp {harga:,}")
    # Menampilkan jumlah stok yang tersedia
    print(f"Stok Tersedia   : {stok} unit")

if __name__ == "__main__":
    # Mendefinisikan nama produk
    nama_produk = "Laptop Gaming ASUS ROG"
    # Mendefinisikan harga produk
    harga = 15000000
    # Mendefinisikan stok yang tersedia
    stok_tersedia = 5

    # Memanggil fungsi untuk menampilkan detail produk
    tampilkan_produk(nama_produk, harga, stok_tersedia)
```

Berikut penjelasan aturan penulisan kode Python tersebut:

## 1. **Definisi Fungsi (`def`)**
```python
def tampilkan_produk(nama, harga, stok):
```
- **`def`**: Keyword untuk mendefinisikan fungsi
- **`tampilkan_produk`**: Nama fungsi (menggunakan snake_case)
- **`(nama, harga, stok)`**: Parameter fungsi - variabel yang diterima oleh fungsi

## 2. **Docstring dan Komentar**
```python
    # Menampilkan nama produk
```
- **`#`**: Simbol untuk komentar single-line
- Komentar digunakan untuk dokumentasi dan tidak dieksekusi

## 3. **f-string (Formatted String)**
```python
    print(f"Nama Produk     : {nama}")
```
- **`f"..."`**: f-string untuk string formatting
- **`{nama}`**: Placeholder yang akan diganti dengan nilai variabel `nama`

## 4. **Formatting Angka dengan Separator**
```python
    print(f"Harga           : Rp {harga:,}")
```
- **`{harga:,}`**: Format angka dengan separator ribuan
- Contoh: `15000000` menjadi `15,000,000`

## 5. **Indentasi (Penulisan Blok Kode)**
```python
    print(f"Nama Produk     : {nama}")
    print(f"Harga           : Rp {harga:,}")
    print(f"Stok Tersedia   : {stok} unit")
```
- **4 spasi**: Standard indentasi untuk blok fungsi
- Semua perintah dalam fungsi harus di-indentasi

## 6. **Main Guard**
```python
if __name__ == "__main__":
```
- **Konvensi Python**: Menjamin kode hanya dieksekusi ketika file di-run langsung
- **`__name__`**: Variabel khusus Python
- **`"__main__"`**: Nilai ketika file di-run langsung

## 7. **Deklarasi Variabel**
```python
    nama_produk = "Laptop Gaming ASUS ROG"
    harga = 15000000
    stok_tersedia = 5
```
- **Tanpa tipe data**: Python menggunakan dynamic typing
- **Snake_case**: Konvensi penamaan variabel di Python

## 8. **Pemanggilan Fungsi**
```python
    tampilkan_produk(nama_produk, harga, stok_tersedia)
```
- **Nama fungsi** diikuti **`()`**
- **Argument**: Nilai yang dikirim ke parameter fungsi

## Aturan Penting Python:

1. **Case Sensitivity**: `harga` ≠ `Harga` ≠ `HARGA`
2. **Indentasi**: Wajib untuk blok kode (fungsi, if, loop)
3. **Snake_case**: Untuk variabel dan fungsi (`nama_produk`)
4. **PascalCase**: Untuk class (`NamaKelas`)
5. **Komentar**: Gunakan `#` untuk single-line, `"""` untuk multi-line

Kode ini mengikuti **PEP 8** - Style Guide for Python Code yang merupakan standar penulisan kode Python.