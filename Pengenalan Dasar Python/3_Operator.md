# **3. Operator**

**Operator** adalah simbol khusus yang digunakan untuk melakukan operasi pada variabel dan nilai.

## **a. Operator Aritmatika**

Digunakan untuk melakukan operasi matematika umum.

| Operator | Nama                 | Contoh        | Hasil |
| :------- | :------------------- | :------------ | :---- |
| `+`      | Penjumlahan          | `10 + 5`      | `15`  |
| `-`      | Pengurangan          | `10 - 5`      | `5`   |
| `*`      | Perkalian            | `10 * 5`      | `50`  |
| `/`      | Pembagian (float)    | `10 / 4`      | `2.5` |
| `//`     | Pembagian (bulat)    | `10 // 4`     | `2`   |
| `%`      | Modulo (sisa bagi)   | `10 % 3`      | `1`   |
| `**`     | Pangkat              | `10 ** 2`     | `100` |

## **b. Operator Perbandingan**

Digunakan untuk membandingkan dua nilai. Hasilnya selalu `True` atau `False`.

| Operator | Deskripsi             | Contoh       | Hasil |
| :------- | :-------------------- | :----------- | :---- |
| `==`     | Sama dengan           | `5 == 5`     | `True`|
| `!=`     | Tidak sama dengan     | `5 != 3`     | `True`|
| `>`      | Lebih besar dari      | `5 > 3`      | `True`|
| `<`      | Lebih kecil dari      | `5 < 3`      | `False`|
| `>=`     | Lebih besar atau sama | `5 >= 5`     | `True`|
| `<=`     | Lebih kecil atau sama | `5 <= 3`     | `False`|

**Contoh Kode:**

```python
a = 15
b = 4

# Aritmatika
print("Hasil a + b =", a + b)

# Perbandingan
print("Apakah a sama dengan b?", a == b)
print("Apakah a lebih besar dari b?", a > b)
```

**Latihan 3:**

Buat program sederhana untuk menghitung luas persegi panjang. Buat dua variabel, `panjang` dan `lebar`, lalu hitung luasnya (`panjang * lebar`). Cetak hasilnya dengan format: "Luas persegi panjang adalah: [hasil]".

-----

## **4. Input & Output**

## **a. Output**

Kita sudah sering menggunakannya. Fungsi `print()` digunakan untuk menampilkan informasi (output) ke layar atau konsol.

**Contoh Kode:**

```python
nama = "Andi"
umur = 22

# Menggabungkan teks dan variabel
print("Nama saya", nama, "dan umur saya", umur, "tahun.")

# Menggunakan f-string (cara yang lebih modern dan direkomendasikan)
print(f"Nama saya {nama} dan umur saya {umur} tahun.")
```

## **b. Input**

Untuk membuat program yang interaktif, kita perlu menerima masukan (input) dari pengguna. Fungsi `input()` digunakan untuk tujuan ini.

**Penting:** Secara *default*, semua masukan dari fungsi `input()` akan dianggap sebagai tipe data **string (`str`)**. Jika Anda membutuhkan angka, Anda harus mengubahnya (melakukan *casting*).

**Contoh Kode:**

```python
# Meminta input nama dari pengguna
nama_pengguna = input("Silakan masukkan nama Anda: ")

# Meminta input umur, lalu mengubahnya menjadi integer
umur_pengguna = int(input("Masukkan umur Anda: "))

# Menampilkan hasil input
print(f"Halo, {nama_pengguna}! Tahun depan umur Anda adalah {umur_pengguna + 1}.")
```

**Latihan 4:**

Buat program yang meminta pengguna memasukkan alas dan tinggi sebuah segitiga. Program kemudian harus menghitung dan menampilkan luas segitiga tersebut. Ingat, rumus luas segitiga adalah $0.5 \\times alas \\times tinggi$. Pastikan input dari pengguna diubah menjadi tipe data yang sesuai (float atau integer).