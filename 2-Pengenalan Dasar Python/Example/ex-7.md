
### **Bagian 1: Operator Pembanding / Relasi**

**Jawaban Latihan 1.1: Cek Batas Umur (SIM)**

```python
# 1. Meminta input usia
usia_pengguna = int(input("Masukkan usia Anda: "))

# 2. Periksa apakah usia >= 17
memenuhi_syarat = usia_pengguna >= 17

# 3. Cetak hasil
print(f"Apakah Anda memenuhi syarat membuat SIM? {memenuhi_syarat}")
```

**Pembahasan:**

Operator `>=` (lebih besar dari atau sama dengan) sangat penting di sini. Jika pengguna memasukkan `17`, hasilnya akan `True`. Jika kita hanya menggunakan `>`, maka `17 > 17` akan menjadi `False`.

-----

**Jawaban Latihan 1.2: Perbandingan Password**

```python
# 1. Password yang benar
password_sistem = "SuperAman123"

# 2. Minta input pengguna
password_input = input("Masukkan password Anda: ")

# 3. Bandingkan
apakah_cocok = password_input == password_sistem

# 4. Cetak hasil
print(f"Password yang Anda masukkan benar: {apakah_cocok}")
```

**Pembahasan Tantangan:**

Jika Anda memasukkan "superaman123" (semua huruf kecil), hasilnya akan `False`. 

Ini karena operator `==` pada string bersifat **case-sensitive** (membedakan huruf besar dan kecil). `"SuperAman123"` dianggap berbeda dari `"superaman123"`.

-----

### **Bagian 2: Operator Logika**

**Jawaban Latihan 2.1: Validasi Login Lengkap**

```python
# 1. Data yang benar
username_benar = "admin"
password_benar = "SuperAman123"

# 2. Minta input username
username_input = input("Masukkan username: ")
# 3. Minta input password
password_input = input("Masukkan password: ")

# 4. Cek kedua kondisi dengan 'and'
login_berhasil = (username_input == username_benar) and (password_input == password_benar)

# 5. Cetak status
print(f"Status Login Berhasil: {login_berhasil}")
```

**Pembahasan:**
Penggunaan `and` memastikan bahwa program hanya akan menghasilkan `True` jika *kedua* perbandingan (`username_input == username_benar` dan `password_input == password_benar`) bernilai `True`.

-----

**Jawaban Latihan 2.2: Syarat Kelulusan**

```python
# 1. Minta input nilai
nilai_teori = float(input("Masukkan nilai teori: "))
nilai_praktik = float(input("Masukkan nilai praktik: "))

# 2. Cek status kelulusan
lulus = (nilai_teori > 75) and (nilai_praktik > 75)

print(f"Status Kelulusan: {lulus}")
```

**Pembahasan:**

Jika `nilai_teori` adalah 80 (True) tapi `nilai_praktik` adalah 70 (False), maka `True and False` akan menghasilkan `False`. Keduanya harus di atas 75.

-----

**Jawaban Latihan 2.3: Pengecekan Hari Libur**

```python
# 1. Variabel kondisi
is_weekend = False
is_tanggal_merah = True

# 2. Tentukan apakah akan piknik
pergi_piknik = is_weekend or is_tanggal_merah

# 3. Cetak hasil
print(f"Pergi piknik? {pergi_piknik}")
```

**Pembahasan:**

Karena `is_tanggal_merah` bernilai `True`, maka kondisi `False or True` akan menghasilkan `True`. Operator `or` hanya butuh salah satu kondisi bernilai `True` untuk menghasilkan `True`.

-----

**Jawaban Latihan 2.4: Menggunakan `not`**

```python
# 1. Variabel kondisi
sedang_sibuk = True

# 2. Gunakan 'not' untuk membalik nilai
apakah_saya_bebas = not sedang_sibuk

# 3. Cetak hasil
print(f"Apakah saya sedang sibuk? {sedang_sibuk}")
print(f"Apakah saya bebas? {apakah_saya_bebas}")
```

**Pembahasan:**

`not` adalah cara sederhana untuk membalikkan nilai Boolean. `not True` menjadi `False`.

-----

**Jawaban Tantangan (Gabungan): Pengecekan Tiket Wahana**

```python
# 1. Minta semua input
tinggi_badan = int(input("Masukkan tinggi badan Anda (cm): "))
usia = int(input("Masukkan usia Anda (tahun): "))
jawaban_penyakit = input("Apakah Anda punya riwayat penyakit jantung? (ya/tidak): ")

# 2. Konversi input string ke boolean
# Kita ingin True jika dia punya penyakit, jadi kita cek apakah jawabannya "ya"
punya_penyakit_jantung = (jawaban_penyakit == "ya")

# 3. Evaluasi semua kondisi
syarat_tinggi = (tinggi_badan >= 160)
syarat_usia = (usia >= 14)
syarat_kesehatan = not punya_penyakit_jantung # Kita ingin dia TIDAK punya penyakit

# Gabungkan semua syarat dengan 'and'
boleh_naik = syarat_tinggi and syarat_usia and syarat_kesehatan

# 4. Cetak hasil akhir
print(f"Tinggi >= 160 cm: {syarat_tinggi}")
print(f"Usia >= 14 tahun: {syarat_usia}")
print(f"Tidak punya penyakit jantung: {syarat_kesehatan}")
print(f"--- Boleh Naik Wahana: {boleh_naik} ---")
```

**Pembahasan:**

Ini adalah contoh bagaimana logika kompleks dibangun:

1.  Kita ubah input "ya" menjadi `True` (`punya_penyakit_jantung`).

2.  Di syarat akhir, kita butuh `not punya_penyakit_jantung`. Jika pengguna menjawab "ya", `punya_penyakit_jantung` menjadi `True`, dan `not True` menjadi `False` (syarat kesehatan tidak terpenuhi).

3.  Ketiga kondisi (`syarat_tinggi`, `syarat_usia`, `syarat_kesehatan`) harus `True` agar hasil akhirnya `True`.