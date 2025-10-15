# **4. Input & Output**

## **a. Output**

Kita sudah sering menggunakannya. Fungsi `print()` digunakan untuk menampilkan informasi (output) ke layar atau konsol.

### **Contoh Kode:**

```python
nama = "Andi"
umur = 22

# Menggabungkan teks dan variabel
print("Nama saya", nama, "dan umur saya", umur, "tahun.")

# Menggunakan f-string (cara yang lebih modern dan direkomendasikan) 

# F-string memungkinkan penulisan variabel langsung di dalam string dengan menggunakan tanda kurung kurawal {}

# F-string juga mendukung ekspresi Python, format angka, dan lain-lain.

# Contoh lain penggunaan f-string:

angka = 10
kalimat = f"Nilai angka adalah {angka}"
print(kalimat)

# Bisa juga melakukan operasi di dalam f-string
hasil = f"Lima ditambah lima sama dengan {5 + 5}"
print(hasil)

# Format desimal pada f-string
harga = 25.567
format_harga = f"Harga barang adalah Rp {harga:.2f}"  # Dua angka di belakang koma
print(format_harga)
```

## **b. Input**

Untuk membuat program yang interaktif, kita perlu menerima masukan (input) dari pengguna. Fungsi `input()` digunakan untuk tujuan ini.

**Penting:** Secara *default*, semua masukan dari fungsi `input()` akan dianggap sebagai tipe data **string (`str`)**. Jika Anda membutuhkan angka, Anda harus mengubahnya (melakukan *casting*) adalah informasi penting yang perlu diketahui.

### **Contoh Kode:**

```python
# Meminta input nama dari pengguna
nama_pengguna = input("Silakan masukkan nama Anda: ")

# Meminta input umur, lalu mengubahnya menjadi integer
umur_pengguna = int(input("Masukkan umur Anda: "))

# Menampilkan hasil input
print(f"Halo, {nama_pengguna}! Tahun depan umur Anda adalah {umur_pengguna + 1}.")
```

**Latihan 4:**

Buat program yang meminta pengguna memasukkan alas dan tinggi sebuah segitiga. Program kemudian harus menghitung dan menampilkan luas segitiga tersebut. 

Ingat, rumus luas segitiga adalah 

```bash
$0.5 \\times alas \\times tinggi$. 
```

Pastikan input dari pengguna diubah menjadi tipe data yang sesuai `(float atau integer)`.