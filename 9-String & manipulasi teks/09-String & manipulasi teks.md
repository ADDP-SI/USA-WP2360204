# **Modul Praktikum 9: Manipulasi String & Teks**

Selamat datang di modul 9!

Dalam dunia pemrograman, data tidak selalu berupa angka. Kita sering berurusan dengan nama, alamat, email, atau paragraf teks.

Di Python, **String** bukan sekadar tulisan. String adalah urutan karakter yang memiliki banyak "senjata" (metode) bawaan untuk memotong, mencari, mengganti, dan memformat teks tersebut.

**Tujuan Pembelajaran:**

1. Memahami konsep String sebagai urutan karakter (*sequence*).
2. Mampu menggunakan teknik **Slicing** untuk mengambil bagian teks.
3. Menguasai metode manipulasi dasar (`upper`, `lower`, `strip`, `replace`, `split`).
4. **Studi Kasus:** Membuat Program Validasi Email Sederhana & Formatter Teks.

## **1. String sebagai Sequence (Slicing)**

Karena string adalah urutan karakter, kita bisa mengambil isinya berdasarkan indeks (nomor urut), sama seperti List.

**Konsep:**

* Indeks dimulai dari **0**.
* Indeks negatif (`-1`) berarti karakter paling belakang.

**Contoh Kode:**

```python
teks = "Politeknik"

print(teks[0])      # Output: P (Huruf pertama)
print(teks[-1])     # Output: k (Huruf terakhir)

# Slicing [start:stop]
# Ingat: Indeks 'stop' tidak ikut diambil
print(teks[0:4])    # Output: Poli
print(teks[4:])     # Output: teknik (Dari indeks 4 sampai habis)
```
## **2. Operasi Dasar Manipulasi String**

Python menyediakan banyak fungsi bawaan (method) yang menempel pada objek string. Berikut yang paling sering digunakan:

### **a. Mengubah Case (Huruf Besar/Kecil)**

```python
kata = "belajar python"
print(kata.upper())      # "BELAJAR PYTHON"
print(kata.lower())      # "belajar python"
print(kata.title())      # "Belajar Python" (Huruf awal kapital)

```

### **b. Membersihkan Spasi (Cleaning)**

Sangat penting untuk membersihkan input user yang tidak sengaja menekan spasi.

```python
input_user = "   admin   "
print(input_user.strip()) # "admin" (Hilangkan spasi depan & belakang)

```

### **c. Mengganti & Mencari (Replace & Find)**

```python
kalimat = "Saya suka Java"
# Mengganti kata
kalimat_baru = kalimat.replace("Java", "Python") 
print(kalimat_baru) # "Saya suka Python"

# Mencari posisi kata (Return indeks pertama ditemukan)
posisi = kalimat.find("suka")
print(posisi) # Output: 5
# Jika tidak ketemu, .find() mengembalikan -1

```

### **d. Memecah & Menggabung (Split & Join) 🌟 PENTING**

Ini adalah jembatan antara **String** dan **List**.

```python
data_csv = "Andi,Budi,Caca,Dedi"

# String -> List (Memecah berdasarkan koma)
list_nama = data_csv.split(",") 
print(list_nama) # ['Andi', 'Budi', 'Caca', 'Dedi']

# List -> String (Menggabung dengan pemisah)
gabung_lagi = " - ".join(list_nama)
print(gabung_lagi) # "Andi - Budi - Caca - Dedi"

```

## **3. Diskusi: Immutability (Ketidakubah-an)**

Coba diskusikan kode berikut. Mengapa terjadi error?

```python
nama = "Budi"
# nama[0] = "R"  <-- Error! Mengapa?
print(nama)

```

**Penjelasan:** String di Python bersifat **Immutable**. Artinya, setelah dibuat, isinya tidak bisa diubah per huruf. Jika ingin mengubah "Budi" menjadi "Rudi", Anda harus membuat string **baru** (`nama = "R" + nama[1:]`).

## **4. Studi Kasus 1: Program Formatter Teks (Laporan)**

**Skenario:**
Anda memiliki data nama mahasiswa yang berantakan (huruf besar kecil acak, ada spasi berlebih). Tugas Anda adalah merapikannya menjadi format judul (Title Case).

**Kode Program:**

```python
def rapikan_teks(daftar_nama):
    print("--- HASIL FORMATTING ---")
    for nama in daftar_nama:
        # 1. strip() buang spasi depan belakang
        # 2. title() ubah jadi Huruf Besar Di Awal
        nama_bersih = nama.strip().title()
        print(f"Original: '{nama}' -> Rapih: '{nama_bersih}'")

# Data kotor
data_mahasiswa = ["  aNDi sAPutra ", "BUDI SANTOSO", "siti aminah   "]
rapikan_teks(data_mahasiswa)
```

## **5. Studi Kasus 2: Validasi Format Email**

**Skenario:**

Sebelum data disimpan ke database, kita harus memastikan input user terlihat seperti email yang valid.
Meskipun validasi sempurna membutuhkan *Regular Expression* (Materi Lanjutan), kita bisa menggunakan manipulasi string dasar untuk pengecekan sederhana.

**Syarat Validasi Sederhana:**

1. Harus memiliki simbol `@`.
2. Harus memiliki simbol `.` (titik).
3. Simbol `@` tidak boleh di awal atau di akhir kalimat.
4. Tidak boleh ada spasi.

**Kode Program:**

```python
def cek_validasi_email(email):
    # 1. Cek spasi
    if " " in email:
        return False, "Email tidak boleh mengandung spasi."
    
    # 2. Cek keberadaan @ dan .
    if "@" not in email or "." not in email:
        return False, "Email harus memiliki '@' dan '.'."
    
    # 3. Cek posisi @ (tidak boleh di depan atau belakang)
    # email.startswith("@") sama dengan email[0] == "@"
    if email.startswith("@") or email.endswith("@"):
        return False, "Posisi '@' tidak valid."
    
    # 4. Cek apakah titik ada setelah @ (misal: andi@gmail.com)
    posisi_at = email.find("@")
    posisi_titik = email.find(".", posisi_at) # Cari titik SETELAH posisi @
    
    if posisi_titik == -1:
        return False, "Domain email tidak valid (titik harus setelah @)."

    return True, "Email Valid!"

# --- Program Utama ---
print("=== VALIDASI EMAIL ===")
input_email = input("Masukkan email Anda: ")

is_valid, pesan = cek_validasi_email(input_email)

if is_valid:
    print(f"SUKSES: {pesan}")
    # Lakukan proses simpan data di sini...
else:
    print(f"GAGAL: {pesan}")

```

**Analisis Diskusi:**

* Coba masukkan `andi@.com`. Apakah program menganggapnya valid? (Kemungkinan valid, padahal domain kosong). Bagaimana cara memperbaikinya?
* Coba masukkan `andi@@gmail.com`. Apakah valid?

## **Tugas Latihan Mandiri**

**Program "Sensor Kata Kasar"**
Buatlah program yang meminta input kalimat dari user. Jika kalimat mengandung kata terlarang (misal: "bodoh", "jelek"), ganti kata tersebut dengan tanda sensor (`*****`).

* *Input:* "Dasar kamu bodoh dan jelek sekali."
* *Output:* "Dasar kamu ***** dan ***** sekali."
* *Petunjuk:* Gunakan `.replace()` atau `.split()` dengan perulangan.

---

## **Referensi**

* [Python String Methods (W3Schools)](https://www.w3schools.com/python/python_ref_string.asp)
* [Real Python - Strings and Character Data](https://realpython.com/python-strings/)