# Modul Praktikum 6: Fungsi & Modularisasi

Selamat datang di modul keenam! Sampai saat ini, kita menulis kode program dalam satu blok panjang dari atas ke bawah. 

Cara ini bekerja untuk program kecil. Namun, bagaimana jika program Anda memiliki 1.000 atau 10.000 baris? Akan sangat sulit untuk mengelolanya.

Di sinilah Fungsi (`Functions`) berperan. Fungsi ini memungkinkan kita memecah program besar menjadi bagian-bagian kecil yang dapat digunakan kembali.

**Tujuan Pembelajaran:**

- Memahami konsep `Fungsi` sebagai `sub-program`.
- Memahami perbedaan `Parameter` (input) dan `Return `(output).
- Mampu memecah masalah kompleks menjadi beberapa fungsi kecil (`Modularisasi`).

**Studi Kasus:**

- Membuat Program Kalkulator Modular.

## 1. Konsep Dasar Fungsi
Bayangkan sebuah Blender.

1. **Input:** Anda memasukkan buah dan air.
2. **Proses:** Mesin berputar dan menghancurkan buah.
3. **Output:** Jus buah yang siap diminum.

Dalam pemrograman:

- **Blender** adalah `Fungsi`.
- **Buah** adalah` Parameter` (_Argument_).
- **Jus** adalah `Return Value` (Nilai Kembalian).

**Sintaks Dasar**

Di Python, kita mendefinisikan fungsi dengan kata kunci `def`.

```python
def nama_fungsi(parameter):
    # Blok kode fungsi
    hasil = parameter + ...
    return hasil
```

## 2. Contoh: Tahapan Membuat Fungsi

Mari kita lakukan demonstrasi bertahap dari fungsi paling sederhana hingga yang memiliki nilai kembalian.

### Tahap A: Fungsi Sederhana (Tanpa Input, Tanpa Output)

Hanya menjalankan perintah.

```python
def sapa_kampus():
    print("Halo! Selamat datang di Praktikum Python.")
    print("Jangan lupa presensi ya!")

# Cara memanggil fungsi:
sapa_kampus()
sapa_kampus() # Bisa dipanggil berkali-kali
```

### Tahap B: Fungsi dengan Parameter (Input)

Fungsi menjadi lebih fleksibel karena bisa menerima data dari luar.

```python
def sapa_nama(nama, prodi):
    print(f"Halo, {nama} dari prodi {prodi}!")

# Memanggil dengan data berbeda
sapa_nama("Budi", "Informatika")
sapa_nama("Siti", "Sistem Informasi")
```

### Tahap C: Fungsi dengan Return (Output) 

Mungkin banyak orang bingung antara `print` dan `return`.

- `print`: Hanya menampilkan ke layar (manusia melihat, komputer lupa).
- `return`: Mengembalikan nilai ke program utama untuk diolah lagi (disimpan ke variabel).

```python
def hitung_luas_persegi(sisi):
    luas = sisi * sisi
    return luas  # Mengirimkan hasil keluar

# Hasilnya kita tangkap dalam variabel
hasil_A = hitung_luas_persegi(5)
hasil_B = hitung_luas_persegi(10)

print(f"Luas A adalah {hasil_A} dan Luas B adalah {hasil_B}")
print(f"Total luas keduanya: {hasil_A + hasil_B}")
```
> Diskusi: Apa yang terjadi jika baris `return luas` diganti `print(luas)`? Bisakah kita melakukan penjumlahan di baris terakhir?


Jika `return luas` diganti dengan `print(luas)`, maka fungsi `hitung_luas_persegi` akan menampilkan nilai luas ke konsol, tetapi tidak akan mengembalikan nilai tersebut ke pemanggil fungsi.

Artinya, variabel `hasil_A` dan `hasil_B` tidak akan menangkap nilai numerik. Sebaliknya, mereka akan menyimpan nilai `None` (karena fungsi tanpa `return` eksplisit secara implisit mengembalikan `None`).

Oleh karena itu, baris `print(f"Total luas keduanya: {hasil_A + hasil_B}")` akan menghasilkan error, karena Anda tidak bisa menjumlahkan `None` dengan `None` (atau dengan angka). `print` hanya untuk menampilkan, `return` untuk mengembalikan nilai yang bisa diolah lebih lanjut.

## 3. Studi Kasus: Kalkulator Modular

Daripada membuat kalkulator dengan satu blok `if-elif-else` yang sangat panjang, kita akan memecah logika program menjadi beberapa fungsi terpisah.

Pendekatan modular ini membuat kode lebih **rapi**, **mudah dibaca**, dan **mudah diperbaiki** jika ada kesalahan pada operasi tertentu.

### Langkah 1: Buat Fungsi Operasi Matematika

```python
# File: kalkulator.py

def tambah(a, b):
    return a + b

def kurang(a, b):
    return a - b

def kali(a, b):
    return a * b

def bagi(a, b):
    if b == 0:
        return "Error: Tidak bisa membagi dengan nol!"
    return a / b
```

### Langkah 2: Buat Fungsi Menu & Input Pengguna

Kita pisahkan logika tampilan menu dan pengambilan input agar program utama tetap bersih dan rapi.

```python
def tampilkan_menu():
    print("\n--- KALKULATOR MODULAR ---")
    print("1. Penjumlahan")
    print("2. Pengurangan")
    print("3. Perkalian")
    print("4. Pembagian")
    print("5. Keluar")

def minta_input_angka():
    # Fungsi ini mengembalikan dua angka sekaligus (Tuple)
    angka1 = float(input("Masukkan angka pertama: "))
    angka2 = float(input("Masukkan angka kedua: "))
    return angka1, angka2
```

### Langkah 3: Program Utama (Main Loop)

Menyatukan semua “potongan puzzle” di atas menjadi satu program yang utuh.

```python
while True:
    tampilkan_menu()
    pilihan = input("Pilih operasi (1-5): ")

    if pilihan == '5':
        print("Terima kasih telah menggunakan aplikasi ini.")
        break # Keluar dari loop

    if pilihan in ('1', '2', '3', '4'):
        # Panggil fungsi input
        num1, num2 = minta_input_angka()
        
        if pilihan == '1':
            hasil = tambah(num1, num2)
            print(f"Hasil: {num1} + {num2} = {hasil}")
        
        elif pilihan == '2':
            hasil = kurang(num1, num2)
            print(f"Hasil: {num1} - {num2} = {hasil}")

        elif pilihan == '3':
            hasil = kali(num1, num2)
            print(f"Hasil: {num1} * {num2} = {hasil}")

        elif pilihan == '4':
            hasil = bagi(num1, num2)
            print(f"Hasil: {num1} / {num2} = {hasil}")
            
    else:
        print("Pilihan tidak valid, silakan coba lagi.")
```

### Final Kode

```python
# --- BAGIAN 1: DEFINISI FUNGSI OPERASI ---
def tambah(a, b):
    return a + b

def kurang(a, b):
    return a - b

def kali(a, b):
    return a * b

def bagi(a, b):
    if b == 0:
        return "Error: Tidak bisa membagi dengan nol!"
    return a / b

# --- BAGIAN 2: FUNGSI MENU & INPUT ---
def tampilkan_menu():
    print("\n--- KALKULATOR MODULAR ---")
    print("1. Penjumlahan")
    print("2. Pengurangan")
    print("3. Perkalian")
    print("4. Pembagian")
    print("5. Keluar")

def minta_input_angka():
    # Menggunakan try-except agar tidak error jika user memasukkan huruf
    try:
        angka1 = float(input("Masukkan angka pertama: "))
        angka2 = float(input("Masukkan angka kedua: "))
        return angka1, angka2
    except ValueError:
        print("Input harus berupa angka!")
        return 0, 0

# --- BAGIAN 3: PROGRAM UTAMA (MAIN LOOP) ---
if __name__ == "__main__":
    while True:
        tampilkan_menu()
        pilihan = input("Pilih operasi (1-5): ")

        if pilihan == '5':
            print("Terima kasih telah menggunakan aplikasi ini.")
            break # Keluar dari loop (Program berhenti)

        if pilihan in ('1', '2', '3', '4'):
            # Panggil fungsi input
            num1, num2 = minta_input_angka()
            
            if pilihan == '1':
                hasil = tambah(num1, num2)
                print(f"Hasil: {num1} + {num2} = {hasil}")
            
            elif pilihan == '2':
                hasil = kurang(num1, num2)
                print(f"Hasil: {num1} - {num2} = {hasil}")

            elif pilihan == '3':
                hasil = kali(num1, num2)
                print(f"Hasil: {num1} * {num2} = {hasil}")

            elif pilihan == '4':
                hasil = bagi(num1, num2)
                print(f"Hasil: {num1} / {num2} = {hasil}")
                
        else:
            print("Pilihan tidak valid, silakan coba lagi.")
```

### Cara Menggunakan Program

1. Setelah dijalankan, menu akan muncul:

```bash
--- KALKULATOR MODULAR ---
1. Penjumlahan
2. Pengurangan
...
Pilih operasi (1-5):
```
2. Ketik angka (misalnya `1`) lalu tekan Enter.

3. Program akan meminta angka pertama. Ketik (misalnya `10`) lalu Enter.

4. Program akan meminta angka kedua. Ketik (misalnya `5`) lalu Enter.

5. Hasil akan muncul, dan menu akan ditampilkan kembali (karena kita menggunakan while True).

6. Untuk berhenti, pilih menu 5.

## 4. Latihan / Tugas Praktikum

Untuk memastikan kamu benar-benar memahami konsep modularisasi, kerjakan tugas berikut:

### Tugas: Program Penghitung Luas & Keliling Bangun Datar (Modular)

Buatlah program Python yang terdiri dari fungsi-fungsi terpisah untuk menghitung luas dan keliling bangun datar.

***Persyaratan fungsi yang harus dibuat:***

- `luas_persegi(sisi)` → mengembalikan luas persegi
- `keliling_persegi(sisi)` → mengembalikan keliling persegi
- `luas_lingkaran(jari_jari)` → mengembalikan luas lingkaran (gunakan π = 3.14)
- `keliling_lingkaran(jari_jari)` → mengembalikan keliling lingkaran
- `tampilkan_menu()` → menampilkan pilihan bangun datar
- Program utama menggunakan perulangan `while` `True` dan hanya berhenti ketika user memilih Keluar.

***Contoh Output:***

```bash
--- PILIH BANGUN DATAR ---
1. Persegi
2. Lingkaran
3. Keluar
Pilih bangun datar (1-3):
```

### Contoh Input:

```bash
Pilih bangun datar (1-3): 1
Masukkan sisi persegi: 5
```

### Contoh Output:

```bash
Luas persegi: 25
Keliling persegi: 20
```

Kriteria Penilaian:

- Semua perhitungan berada di dalam fungsi terpisah (`def`)
- Fungsi menggunakan `return`, bukan `print` langsung
- Program tetap berjalan (loop) sampai user memilih Keluar
- Penanganan input yang salah (misalnya huruf bukan angka)
- Kode rapi, ada komentar, dan mudah dibaca

Selamat mengerjakan!

## Referensi Tambahan

- [Python Functions - W3Schools](https://www.w3schools.com/python/python_functions.asp)
- [Defining Functions - Python Docs](https://docs.python.org/3/tutorial/controlflow.html#defining-functions)