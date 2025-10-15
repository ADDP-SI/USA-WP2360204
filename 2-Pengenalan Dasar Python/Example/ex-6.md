**Berikut program Python untuk simulasi poin game dengan berbagai kejadian:**

```python
# Inisialisasi skor awal
skor = 0
print(f"Skor awal: {skor}")

# 1. Pemain mendapatkan 100 poin karena menyelesaikan level
skor += 100
print(f"Setelah menyelesaikan level, skor menjadi: {skor}")

# 2. Pemain kehilangan 25 poin karena terkena jebakan
skor -= 25
print(f"Setelah terkena jebakan, skor menjadi: {skor}")

# 3. Pemain mendapatkan bonus poin dua kali lipat dari skor saat ini
skor *= 2
print(f"Setelah mendapatkan bonus 2x, skor menjadi: {skor}")
```

**Output:**
```
Skor awal: 0
Setelah menyelesaikan level, skor menjadi: 100
Setelah terkena jebakan, skor menjadi: 75
Setelah mendapatkan bonus 2x, skor menjadi: 150
```

**Versi Lengkap dengan Penjelasan Detail**

```python
def simulasi_game():
    """
    Simulasi sistem skor game dengan berbagai kejadian
    """
    # Inisialisasi skor awal
    skor = 0
    print("🎮 SIMULASI SISTEM SKOR GAME 🎮")
    print(f"\n📊 Skor awal: {skor}")
    
    # Kejadian 1: Menyelesaikan level
    print(f"\n🎉 Pemain menyelesaikan level!")
    print(f"   +100 poin")
    skor += 100
    print(f"   📊 Skor sekarang: {skor}")
    
    # Kejadian 2: Terkena jebakan
    print(f"\n💥 Pemain terkena jebakan!")
    print(f"   -25 poin")
    skor -= 25
    print(f"   📊 Skor sekarang: {skor}")
    
    # Kejadian 3: Bonus dua kali lipat
    print(f"\n🚀 Pemain mendapatkan bonus 2x!")
    print(f"   Skor {skor} × 2 = {skor * 2}")
    skor *= 2
    print(f"   📊 Skor sekarang: {skor}")
    
    # Ringkasan akhir
    print(f"\n{'='*40}")
    print(f"🏆 SKOR AKHIR: {skor}")
    print(f"{'='*40}")

# Menjalankan simulasi
if __name__ == "__main__":
    simulasi_game()
```

**Output Versi Lengkap:**
```
🎮 SIMULASI SISTEM SKOR GAME 🎮

📊 Skor awal: 0

🎉 Pemain menyelesaikan level!
   +100 poin
   📊 Skor sekarang: 100

💥 Pemain terkena jebakan!
   -25 poin
   📊 Skor sekarang: 75

🚀 Pemain mendapatkan bonus 2x!
   Skor 75 × 2 = 150
   📊 Skor sekarang: 150

========================================
🏆 SKOR AKHIR: 150
========================================
```

**Penjelasan Operator Penugasan:**

1. **`+=`** (Penugasan Penjumlahan):
   ```python
   skor += 100  # Sama dengan: skor = skor + 100
   ```

2. **`-=`** (Penugasan Pengurangan):
   ```python
   skor -= 25   # Sama dengan: skor = skor - 25
   ```

3. **`*=`** (Penugasan Perkalian):
   ```python
   skor *= 2    # Sama dengan: skor = skor * 2
   ```

**Versi Interaktif dengan Input Pengguna**

```python
def simulasi_game_interaktif():
    """
    Simulasi game dengan input dari pengguna
    """
    skor = 0
    print("🎮 SIMULASI GAME INTERAKTIF 🎮")
    print(f"Skor awal: {skor}")
    
    while True:
        print("\nPilih aksi:")
        print("1. Selesaikan level (+100 poin)")
        print("2. Terkena jebakan (-25 poin)")
        print("3. Dapatkan bonus 2x")
        print("4. Keluar")
        
        pilihan = input("Masukkan pilihan (1-4): ")
        
        if pilihan == "1":
            skor += 100
            print(f"🎉 Level selesai! Skor: {skor}")
        elif pilihan == "2":
            skor -= 25
            print(f"💥 Terkena jebakan! Skor: {skor}")
        elif pilihan == "3":
            print(f"🚀 Bonus 2x! {skor} → {skor * 2}")
            skor *= 2
            print(f"Skor: {skor}")
        elif pilihan == "4":
            print(f"\n🏆 Skor akhir: {skor}")
            print("Terima kasih telah bermain!")
            break
        else:
            print("Pilihan tidak valid!")

# Menjalankan game interaktif
if __name__ == "__main__":
    simulasi_game_interaktif()
```

Program ini menunjukkan bagaimana operator penugasan dapat digunakan untuk memodifikasi nilai variabel secara dinamis, yang sangat berguna dalam pengembangan game!

**Berikut program Python untuk menghitung bunga sederhana tabungan:**

**Versi Dasar**

```python
# Variabel awal
saldo_awal = 1000000
bunga_tahunan = 0.05  # 5%

# Menghitung saldo setelah satu tahun
saldo_setahun = saldo_awal * (1 + bunga_tahunan)

# Cetak hasil
print(f"Saldo awal: Rp {saldo_awal:,}")
print(f"Bunga tahunan: {bunga_tahunan * 100}%")
print(f"Saldo setelah 1 tahun: Rp {saldo_setahun:,.2f}")
```

**Output:**
```
Saldo awal: Rp 1,000,000
Bunga tahunan: 5.0%
Saldo setelah 1 tahun: Rp 1,050,000.00
```

**Versi dengan Operator Penugasan** `*=`

```python
# Variabel awal
saldo = 1000000
bunga_tahunan = 0.05  # 5%

print(f"Saldo awal: Rp {saldo:,}")

# Menggunakan operator *= untuk menghitung bunga
saldo *= (1 + bunga_tahunan)

print(f"Bunga tahunan: {bunga_tahunan * 100}%")

# Mencetak saldo akhir
print(f"Saldo setelah 1 tahun: Rp {saldo:,.2f}")
```

**Output:**
```
Saldo awal: Rp 1,000,000
Bunga tahunan: 5.0%
Saldo setelah 1 tahun: Rp 1,050,000.00
```

## Versi Lengkap dengan Simulasi Beberapa Tahun

```python
def simulasi_bunga():
    """
    Simulasi pertumbuhan tabungan dengan bunga sederhana
    """
    # Variabel awal
    saldo = 1000000
    bunga_tahunan = 0.05  # 5%
    
    print("💰 SIMULASI PERTUMBUHAN TABUNGAN 💰")
    print(f"\nSaldo awal: Rp {saldo:,}")
    print(f"Suku bunga tahunan: {bunga_tahunan * 100}%")
    print(f"\n{'='*50}")
    
    # Simulasi untuk 5 tahun
    for tahun in range(1, 6):
        saldo_lama = saldo
        saldo *= (1 + bunga_tahunan)  # Operator penugasan *=
        bunga_didapat = saldo - saldo_lama
        
        print(f"Tahun {tahun}:")
        print(f"  Saldo awal tahun : Rp {saldo_lama:,.2f}")
        print(f"  Bunga didapat    : Rp {bunga_didapat:,.2f}")
        print(f"  Saldo akhir tahun: Rp {saldo:,.2f}")
        print(f"  {'-'*40}")

# Menjalankan simulasi
if __name__ == "__main__":
    simulasi_bunga()
```

**Output Versi Lengkap:**
```
💰 SIMULASI PERTUMBUHAN TABUNGAN 💰

Saldo awal: Rp 1,000,000
Suku bunga tahunan: 5.0%

==================================================
Tahun 1:
  Saldo awal tahun : Rp 1,000,000.00
  Bunga didapat    : Rp 50,000.00
  Saldo akhir tahun: Rp 1,050,000.00
  ----------------------------------------
Tahun 2:
  Saldo awal tahun : Rp 1,050,000.00
  Bunga didapat    : Rp 52,500.00
  Saldo akhir tahun: Rp 1,102,500.00
  ----------------------------------------
... (dan seterusnya)
```

## Versi Interaktif dengan Input Pengguna

```python
def kalkulator_bunga_interaktif():
    """
    Kalkulator bunga dengan input dari pengguna
    """
    try:
        print("💰 KALKULATOR BUNGA TABUNGAN 💰")
        
        # Input dari pengguna
        saldo = float(input("Masukkan saldo awal: Rp "))
        bunga_tahunan = float(input("Masukkan bunga tahunan (%): ")) / 100
        tahun = int(input("Masukkan jangka waktu (tahun): "))
        
        print(f"\n{'='*60}")
        print(f"SIMULASI TABUNGAN")
        print(f"{'='*60}")
        print(f"Saldo awal     : Rp {saldo:,.2f}")
        print(f"Bunga tahunan  : {bunga_tahunan * 100}%")
        print(f"Jangka waktu   : {tahun} tahun")
        print(f"{'='*60}")
        
        saldo_awal = saldo  # Simpan saldo awal untuk perhitungan
        
        for t in range(1, tahun + 1):
            saldo *= (1 + bunga_tahunan)  # Operator penugasan *=
            print(f"Tahun {t:2d}: Rp {saldo:,.2f}")
        
        total_bunga = saldo - saldo_awal
        print(f"{'='*60}")
        print(f"Saldo akhir    : Rp {saldo:,.2f}")
        print(f"Total bunga    : Rp {total_bunga:,.2f}")
        print(f"Pertumbuhan    : {(saldo/saldo_awal - 1) * 100:.2f}%")
        
    except ValueError:
        print("Error: Masukkan harus berupa angka!")

# Menjalankan kalkulator
if __name__ == "__main__":
    kalkulator_bunga_interaktif()
```

**Contoh Output Interaktif:**
```
💰 KALKULATOR BUNGA TABUNGAN 💰
Masukkan saldo awal: Rp 1000000
Masukkan bunga tahunan (%): 5
Masukkan jangka waktu (tahun): 3

============================================================
SIMULASI TABUNGAN
============================================================
Saldo awal     : Rp 1,000,000.00
Bunga tahunan  : 5.0%
Jangka waktu   : 3 tahun
============================================================
Tahun  1: Rp 1,050,000.00
Tahun  2: Rp 1,102,500.00
Tahun  3: Rp 1,157,625.00
============================================================
Saldo akhir    : Rp 1,157,625.00
Total bunga    : Rp 157,625.00
Pertumbuhan    : 15.76%
```

**Penjelasan Operator** `*=`

```python
saldo *= (1 + bunga_tahunan)
```

**Sama dengan:**
```python
saldo = saldo * (1 + bunga_tahunan)
```

**Contoh perhitungan:**

- Saldo awal: Rp 1,000,000
- Bunga: 5% = 0.05
- `saldo *= (1 + 0.05)` = `saldo *= 1.05`
- Hasil: Rp 1,000,000 × 1.05 = Rp 1,050,000

Program ini menunjukkan bagaimana operator penugasan `*=` dapat digunakan untuk menghitung pertumbuhan bunga secara efisien!


**Penjelasan tentang `:.2f` dalam kode Python:**

**`:.2f` - Format Specifier untuk Angka Desimal**

`:.2f` adalah **format specifier** yang digunakan dalam f-string untuk memformat tampilan angka floating-point (desimal).

**Breakdown Komponen:**

- **`:`** - Menandakan awal dari format specifier
- **`.2`** - Menunjukkan 2 digit di belakang koma
- **`f`** - Singkatan dari "fixed-point" atau "float"

**Contoh Penggunaan:**

```python
angka = 3.14159

print(f"Angka asli: {angka}")
print(f"Format 2f: {angka:.2f}")
```

**Output:**
```
Angka asli: 3.14159
Format 2f: 3.14
```

**Contoh Lain dalam Konteks Uang:**

```python
saldo = 1050000.756

print(f"Tanpa format: {saldo}")
print(f"Dengan :.2f: {saldo:.2f}")
print(f"Dengan separator ribuan: {saldo:,.2f}")
```

**Output:**
```
Tanpa format: 1050000.756
Dengan :.2f: 1050000.76
Dengan separator ribuan: 1,050,000.76
```

**Perbandingan Berbagai Format:**

```python
harga = 1234.56789

print(f"Default: {harga}")          # 1234.56789
print(f".0f: {harga:.0f}")          # 1235 (pembulatan)
print(f".1f: {harga:.1f}")          # 1234.6
print(f".2f: {harga:.2f}")          # 1234.57
print(f".3f: {harga:.3f}")          # 1234.568
print(f",.2f: {harga:,.2f}")        # 1,234.57
```

**Dalam Konteks Program Bunga:**

```python
saldo = 1050000

# Tanpa format
print(f"Tanpa format: Rp {saldo}")           # Rp 1050000

# Dengan format uang yang baik
print(f"Dengan format: Rp {saldo:,.2f}")     # Rp 1,050,000.00
```

**Kenapa penting dalam konteks uang:**

1. **Konsistensi** - Selalu menampilkan 2 digit desimal (sen)
2. **Pembulatan** - Membulatkan ke 2 digit terdekat
3. **Readability** - Lebih mudah dibaca untuk nilai uang
4. **Profesional** - Format standar untuk laporan keuangan

**Aturan Pembulatan:**
```python
print(f"3.141 → {3.141:.2f}")    # 3.14
print(f"3.145 → {3.145:.2f}")    # 3.15 (pembulatan ke atas)
print(f"3.149 → {3.149:.2f}")    # 3.15
```

**Kombinasi dengan Format Lain:**
```python
saldo = 1500000.456

print(f"Rp {saldo:,.2f}")           # Rp 1,500,000.46
print(f"USD {saldo:,.2f}")          # USD 1,500,000.46
print(f"€{saldo:,.2f}")             # €1,500,000.46
```

Jadi, **`:.2f`** sangat penting dalam aplikasi keuangan untuk memastikan tampilan uang selalu konsisten dengan 2 digit desimal dan format yang rapi!