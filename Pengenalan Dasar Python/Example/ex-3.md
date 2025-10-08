
## Solusi Python

```python
# Inisialisasi variabel dengan nilai float
suhu_celcius = 27.5

# Periksa dan cetak tipe data awal
print("Nilai awal:", suhu_celcius)
print("Tipe data awal:", type(suhu_celcius))
print("Tipe data awal (nama):", type(suhu_celcius).__name__)

# Ubah nilai variabel menjadi string (teks)
suhu_celcius = "dua puluh tujuh"

# Periksa dan cetak tipe data setelah perubahan
print("\nSetelah diubah:")
print("Nilai baru:", suhu_celcius)
print("Tipe data baru:", type(suhu_celcius))
print("Tipe data baru (nama):", type(suhu_celcius).__name__)
```

## Output yang Dihasilkan:
```
Nilai awal: 27.5
Tipe data awal: <class 'float'>
Tipe data awal (nama): float

Setelah diubah:
Nilai baru: dua puluh tujuh
Tipe data baru: <class 'str'>
Tipe data baru (nama): str
```

## Penjelasan Best Practices:

### 1. **Penamaan Variabel yang Deskriptif**
- Menggunakan `suhu_celcius` yang jelas dan mudah dipahami
- Mengikuti konvensi snake_case untuk Python

### 2. **Komentar yang Jelas**
- Setiap bagian kode dijelaskan dengan komentar
- Memudahkan pemahaman alur program

### 3. **Output yang Informatif**
- Menampilkan nilai dan tipe data
- Format output yang rapi dengan pemisah (`\n`)

### 4. **Versi Alternatif dengan Fungsi (Lebih Terstruktur)**

```python
def demonstrasi_tipe_data():
    """
    Demonstrasi perubahan tipe data variabel dalam Python.
    """
    # Inisialisasi variabel
    suhu_celcius = 27.5
    
    # Tampilkan informasi awal
    print_informasi_variabel(suhu_celcius, "Awal")
    
    # Ubah tipe data
    suhu_celcius = "dua puluh tujuh"
    
    # Tampilkan informasi setelah perubahan
    print_informasi_variabel(suhu_celcius, "Setelah perubahan")

def print_informasi_variabel(variabel, status):
    """
    Cetak informasi lengkap tentang variabel.
    
    Args:
        variabel: Variabel yang akan diperiksa
        status (str): Status variabel (Awal/Setelah perubahan)
    """
    print(f"\n=== Status {status} ===")
    print(f"Nilai: {variabel}")
    print(f"Tipe data: {type(variabel)}")
    print(f"Representasi: {repr(variabel)}")

# Eksekusi program
if __name__ == "__main__":
    demonstrasi_tipe_data()
```

## Poin Pembelajaran:

1. **Dynamic Typing**: Python memungkinkan perubahan tipe data variabel secara dinamis
2. **Type Checking**: Fungsi `type()` digunakan untuk memeriksa tipe data
3. **Variable Reassignment**: Nilai dan tipe data variabel dapat diubah selama eksekusi program

## Hasil Observasi:
- **Awal**: `suhu_celcius` bertipe `float` dengan nilai `27.5`
- **Setelah perubahan**: `suhu_celcius` bertipe `str` dengan nilai `"dua puluh tujuh"`
- Python secara dinamis mengubah tipe data variabel ketika diberikan nilai baru

