**Berikut adalah program Python yang meminta input dua angka dan menampilkan semua operasi aritmatika dasar:**

```python
# Meminta input dari pengguna
angka1 = float(input("Masukkan angka pertama: "))
angka2 = float(input("Masukkan angka kedua: "))

# Melakukan semua operasi aritmatika
penjumlahan = angka1 + angka2
pengurangan = angka1 - angka2
perkalian = angka1 * angka2
pembagian = angka1 / angka2
pembagian_bulat = angka1 // angka2
sisa_bagi = angka1 % angka2

# Menampilkan hasil dengan format yang jelas
print("\n--- Hasil Perhitungan ---")
print(f"{angka1} + {angka2} = {penjumlahan}")
print(f"{angka1} - {angka2} = {pengurangan}")
print(f"{angka1} * {angka2} = {perkalian}")
print(f"{angka1} / {angka2} = {pembagian}")
print(f"{angka1} // {angka2} = {pembagian_bulat}")
print(f"{angka1} % {angka2} = {sisa_bagi}")
``` 

**Contoh Output**
```python

Masukkan angka pertama: 15
Masukkan angka kedua: 4

--- Hasil Perhitungan ---
15.0 + 4.0 = 19.0
15.0 - 4.0 = 11.0
15.0 * 4.0 = 60.0
15.0 / 4.0 = 3.75
15.0 // 4.0 = 3.0
15.0 % 4.0 = 3.0
```

Kode ini juga menggunakan fungsi `input()` untuk mengambil input dari pengguna dan mengkonversi ke tipe data yang sesuai.

**Versi alternative dengan penanganan input yang lebih baik:**

```python
def kalkulator_aritmatika():
    try:
        # Meminta input dari pengguna
        angka1 = float(input("Masukkan angka pertama: "))
        angka2 = float(input("Masukkan angka kedua: "))
        
        print("\n--- Hasil Perhitungan ---")
        
        # Menampilkan hasil langsung tanpa variabel tambahan
        print(f"{angka1} + {angka2} = {angka1 + angka2}")
        print(f"{angka1} - {angka2} = {angka1 - angka2}")
        print(f"{angka1} * {angka2} = {angka1 * angka2}")
        print(f"{angka1} / {angka2} = {angka1 / angka2}")
        print(f"{angka1} // {angka2} = {angka1 // angka2}")
        print(f"{angka1} % {angka2} = {angka1 % angka2}")
        
    except ValueError:
        print("Error: Masukkan harus berupa angka!")
    except ZeroDivisionError:
        print("Error: Tidak bisa membagi dengan nol!")

# Menjalankan program
if __name__ == "__main__":
    kalkulator_aritmatika()
```

**Penjelasan operasi aritmatika:**

1. `+` → Penjumlahan
2. `-` → Pengurangan
3. `*` → Perkalian
4. `/` → Pembagian (hasil float)
5. `//` → Pembagian bulat (hasil integer)
6. `%` → Sisa bagi (modulus)


**Contoh Output dengan angka berbeda:**

```bash
Masukkan angka pertama: 10
Masukkan angka kedua: 3

--- Hasil Perhitungan ---
10.0 + 3.0 = 13.0
10.0 - 3.0 = 7.0
10.0 * 3.0 = 30.0
10.0 / 3.0 = 3.3333333333333335
10.0 // 3.0 = 3.0
10.0 % 3.0 = 1.0
```

Program ini akan bekerja untuk semua jenis angka (integer maupun float) dan menampilkan semua operasi aritmatika dasar dengan format yang mudah dibaca.

**Berikut program Python untuk konversi suhu dari Celcius ke Fahrenheit:**

**Versi Dasar (dengan nilai tetap)**

```python
# Variabel suhu dalam Celcius
suhu_celcius = 30

# Konversi ke Fahrenheit
suhu_fahrenheit = (suhu_celcius * 9/5) + 32

# Cetak hasil
print(f"Suhu: {suhu_celcius}°C = {suhu_fahrenheit}°F")
```

**Output:**
```
Suhu: 30°C = 86.0°F
```

**Versi dengan Input Pengguna (Tantangan)**

```python
# Meminta input dari pengguna
suhu_celcius = float(input("Masukkan suhu dalam Celcius: "))

# Konversi ke Fahrenheit
suhu_fahrenheit = (suhu_celcius * 9/5) + 32

# Cetak hasil
print(f"\n--- Hasil Konversi Suhu ---")
print(f"{suhu_celcius}°C = {suhu_fahrenheit}°F")
```

**Contoh Output:**

```bash
Masukkan suhu dalam Celcius: 30

--- Hasil Konversi Suhu ---
30.0°C = 86.0°F
```

**Versi Lengkap dengan Fungsi dan Penanganan Error**

```python
def konversi_suhu():
    """
    Fungsi untuk mengkonversi suhu dari Celcius ke Fahrenheit
    """
    try:
        # Meminta input dari pengguna
        suhu_celcius = float(input("Masukkan suhu dalam Celcius: "))
        
        # Konversi ke Fahrenheit
        suhu_fahrenheit = (suhu_celcius * 9/5) + 32
        
        # Menampilkan hasil dengan format yang rapi
        print(f"\n{'='*30}")
        print(f"HASIL KONVERSI SUHU")
        print(f"{'='*30}")
        print(f"Celcius     : {suhu_celcius}°C")
        print(f"Fahrenheit  : {suhu_fahrenheit:.2f}°F")
        print(f"{'='*30}")
        
    except ValueError:
        print("Error: Masukkan harus berupa angka!")

# Menjalankan program
if __name__ == "__main__":
    konversi_suhu()
```

**Contoh Output Versi Lengkap:**

```bash
Masukkan suhu dalam Celcius: 30

==============================
HASIL KONVERSI SUHU
==============================
Celcius     : 30.0°C
Fahrenheit  : 86.00°F
==============================
```

**Penjelasan Rumus:**

_Rumus Konversi:_

```bash
F = (C × 9/5) + 32
```

**Contoh perhitungan untuk 30°C:**

```bash
F = (30 × 9/5) + 32
  = (30 × 1.8) + 32
  = 54 + 32
  = 86°F
```

**Beberapa contoh konversi lainnya:**

- 0°C = 32°F (titik beku air)
- 100°C = 212°F (titik didih air)
- 37°C = 98.6°F (suhu tubuh normal)

Program ini dapat menerima input angka desimal (seperti 25.5) dan akan mengkonversinya dengan akurat ke Fahrenheit.


**Berikut program Python untuk mengkonversi total detik menjadi format jam, menit, dan detik:**

**Versi Dasar (dengan nilai tetap)**

```python
# Variabel total detik
total_detik = 3661

# Menghitung jam, menit, dan detik
jam = total_detik // 3600          # 3600 detik = 1 jam
sisa_detik = total_detik % 3600    # Sisa setelah diambil jam
menit = sisa_detik // 60           # 60 detik = 1 menit
detik = sisa_detik % 60            # Sisa setelah diambil menit

# Cetak hasil
print(f"Total detik: {total_detik}")
print(f"Jam: {jam}, Menit: {menit}, Detik: {detik}")
```

**Output:**
```
Total detik: 3661
Jam: 1, Menit: 1, Detik: 1
```

**Versi dengan Input Pengguna**

```python
# Meminta input dari pengguna
total_detik = int(input("Masukkan total detik: "))

# Menghitung jam, menit, dan detik
jam = total_detik // 3600
sisa_detik = total_detik % 3600
menit = sisa_detik // 60
detik = sisa_detik % 60

# Cetak hasil
print(f"\n--- Hasil Konversi ---")
print(f"Total detik: {total_detik}")
print(f"Jam: {jam}, Menit: {menit}, Detik: {detik}")
```

**Contoh Output:**

```bash
Masukkan total detik: 3661

--- Hasil Konversi ---
Total detik: 3661
Jam: 1, Menit: 1, Detik: 1
```

**Versi Lengkap dengan Format yang Lebih Baik**

```python
def konversi_detik():
    """
    Fungsi untuk mengkonversi total detik menjadi jam, menit, detik
    """
    try:
        # Meminta input dari pengguna
        total_detik = int(input("Masukkan total detik: "))
        
        if total_detik < 0:
            print("Error: Masukkan harus bilangan positif!")
            return
        
        # Menghitung jam, menit, dan detik
        jam = total_detik // 3600
        sisa_detik = total_detik % 3600
        menit = sisa_detik // 60
        detik = sisa_detik % 60
        
        # Menampilkan hasil dengan format yang rapi
        print(f"\n{'='*40}")
        print(f"HASIL KONVERSI WAKTU")
        print(f"{'='*40}")
        print(f"Total detik  : {total_detik} detik")
        print(f"Format waktu : {jam:02d}:{menit:02d}:{detik:02d}")
        print(f"Detail       : {jam} jam, {menit} menit, {detik} detik")
        print(f"{'='*40}")
        
    except ValueError:
        print("Error: Masukkan harus berupa bilangan bulat!")

# Menjalankan program
if __name__ == "__main__":
    konversi_detik()
```

**Contoh Output Versi Lengkap:**
```
Masukkan total detik: 3661

========================================
HASIL KONVERSI WAKTU
========================================
Total detik  : 3661 detik
Format waktu : 01:01:01
Detail       : 1 jam, 1 menit, 1 detik
========================================
```

**Contoh Lain dengan Berbagai Input:**

**Input: 7200 detik**
```
Total detik: 7200
Jam: 2, Menit: 0, Detik: 0
```

**Input: 12345 detik**

```bash
Total detik: 12345
Jam: 3, Menit: 25, Detik: 45
```

**Input: 65 detik**

```bash
Total detik: 65
Jam: 0, Menit: 1, Detik: 5
```

**Penjelasan Perhitungan:**

**Untuk 3661 detik:**

1. **Jam** = `3661 // 3600` = `1` (pembagian bulat)
2. **Sisa detik** = `3661 % 3600` = `61` (sisa bagi)
3. **Menit** = `61 // 60` = `1`
4. **Detik** = `61 % 60` = `1`

**Verifikasi:**

```bash
1 jam = 3600 detik
1 menit = 60 detik
1 detik = 1 detik
Total = 3600 + 60 + 1 = 3661 detik ✓
```

Program ini dapat mengkonversi berapa pun jumlah detik menjadi format waktu yang mudah dibaca!