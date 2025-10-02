# 5 Aturan Penulisan Sintaks Python yang Harus dipatuhi

## Table of Contents
- [5 Aturan Penulisan Sintaks Python yang Harus dipatuhi](#5-aturan-penulisan-sintaks-python-yang-harus-dipatuhi)
  - [Table of Contents](#table-of-contents)
  - [1. Penulisan Statement Python](#1-penulisan-statement-python)
  - [2. Penulisan `String` pada Python](#2-penulisan-string-pada-python)
  - [3. Penulisan `Case` pada Python](#3-penulisan-case-pada-python)
    - [Case Style](#case-style)
      - [Snake `Case` digunakan pada:](#snake-case-digunakan-pada)
      - [`CamelCase` digunakan pada:](#camelcase-digunakan-pada)
      - [`ALL CAPS` digunakan pada:](#all-caps-digunakan-pada)
  - [4. Penulisan Blok Program Python](#4-penulisan-blok-program-python)
    - [Blok Percabangan `if`](#blok-percabangan-if)
    - [Blok perulangan `for`](#blok-perulangan-for)
    - [Blok Percabangan `if`](#blok-percabangan-if-1)
    - [Blok perulangan `for`](#blok-perulangan-for-1)
  - [5. Cara Penulisan Komentar pada Python](#5-cara-penulisan-komentar-pada-python)
    - [Menggunakan Tanda Pagar (#)](#menggunakan-tanda-pagar-)
    - [Menggunakan Tanda Petik](#menggunakan-tanda-petik)
    - [Menggunakan Triple Tanda Petik](#menggunakan-triple-tanda-petik)
  - [Apa Selanjutnya?](#apa-selanjutnya)
  - [Referensi](#referensi)

---

 ## 1. Penulisan Statement Python

`Statement` adalah sebuah instruksi atau kalimat perintah yang akan dieksekusi oleh komputer.

**Contoh:**

```python
print("Hello World!")
print("Belajar Python dari Nol")
nama = "Yanyan Sofiyan"
```

Penulisan satu `statement` tidak diakhiri dengan tanda titik-koma.

Sedangkan, bila kita ingin menulis lebih dari satu `statement` dalam satu baris, maka kita harus memisahnya dengan `titik-koma`.

**Contoh:**

```python
print("Hello"); print("World"); print("Belajar Python untuk Pemula")
nama_depan = "Yanyan"; nama_belakang = "Sofiyan"
```

Tapi…

> Menurut beberapa `style guide Python`, tidak dianjurkan menulis lebih dari satu `statement` dalam satu baris karena akan sulit dibaca.
> 

## 2. Penulisan `String` pada Python

`String` adalah teks atau kumpulan dari karakter.

`String` dalam pemrograman biasanya ditulis dengan dibungkus menggunakan `tanda petik.`

Bisa menggunakan tanda petik tunggal maupun ganda.

**Contoh:**

```python
judul = "Belajar Pemrograman Python sampai Bisa"
penulis = 'Yanyan Sofiyan'
```

Atau kita juga bisa menggunakan `triple tanda petik`.

**Contoh:**

```python
judul = """Belajar Python dengan Cepat"""
penulis = '''Yanyan Sofiyan'''
```

## 3. Penulisan `Case` pada Python

Sintaks Python bersifat _case sensitive_, artinya `teksini` dengan `TeksIni` dibedakan.

**Contoh:**

```python
judul = "Belajar Dasar-dasar Python"
Judul = "Belajar Membuat Program Python"
```

Antara _variabel_ `judul` dengan `Judul` itu dibedakan.

### Case Style

Menurut rekomendasi [style guide Google](https://google.github.io/styleguide/pyguide.html), berikut ini contoh penulisan `case` yang disarankan:

#### Snake `Case` digunakan pada:

- `module_name`
- `package_name`
- `method_name`
- `function_name`
- `global_var_name`
- `instance_var_name`
- `function_parameter_name`
- `local_var_name`

#### `CamelCase` digunakan pada:

- `ClassName`
- `ExceptionName`

#### `ALL CAPS` digunakan pada:

- `GLOBAL_CONSTANT_NAME`


## 4. Penulisan Blok Program Python

Blok program adalah kumpulan dari beberapa `statement` yang digabungkan dalam satu _blok_.

> Penulisan blok program harus ditambahkan indentasi (tab atau spasi 2x/4x).

```python
print("hello")

if nama == 'yanyan':
    print(nama)
    print("selamat datang")

print("world")
```

![alt text](https://i.ibb.co.com/99GJjBzn/Untitled-2025-04-16-0129.png)

✅ **Contoh yang benar:**

### Blok Percabangan `if`

```python
if username == 'petanikode':
    print("Selamat Datang Admin")
    print("Silakan ambil tempat duduk")
```

### Blok perulangan `for`

```python
for i in range(10):
    print(i)
```

❌ **Contoh yang salah:**

### Blok Percabangan `if`

```python
if username == 'petanikode':
print("Selamat Datang Admin")
print("Silakan ambil tempat duduk")
```

### Blok perulangan `for`

```python
for i in range(10):
print(i)
```

Ada beberapa macam blok program:

- Blok Percabangan
- Blok Perulangan
- Blok Fungsi
- Blok Class
- Blok Exception
- Blok With

## 5. Cara Penulisan Komentar pada Python

Komentar merupakan baris kode yang tidak akan dieksekusi.

Komentar digunakan untuk memberikan informasi tambahan dan untuk menonaktifkan kode.

Ada beberapa cara menulis komentar pada pemrograman Python.

### Menggunakan Tanda Pagar (#)

Cara pertama menggunakan tanda pagar (`#`).

Cara ini paling sering digunakan.

**Contoh:**

```python
# ini adalah komentar
# Ini juga komentar
```

### Menggunakan Tanda Petik

Selain untuk mengapit teks (_string_), tanda petik juga dapat digunakan untuk membuat komentar.

**Contoh:**

```python
"Ini adalah komentar dengan tanda petik ganda"
'Ini juga komentar, tapi dengan tanda petik tunggal'
```

> Penulisan komentar dengan tanda petik jarang digunakan, kebanyakan orang lebih memilih untuk menggunakan tanda pagar. Jadi… tidak direkomendasikan.

### Menggunakan Triple Tanda Petik

Sedangkan triple tanda petik sering digunakan untuk menuliskan `dokumentasi`.

**Contoh:**

```python
class Pagar:
    """kelas pagar untuk membuat objek pagar. Dibuat oleh Yanyan Sofiyan sebagai contoh saja."""
    def __init__(self, warna, tinggi, bahan):
        self.warna = warna
        self.tinggi = tinggi
        self.bahan = bahan


# Mengakses dokumentasi kelas

print(Pagar.__doc__)
input('\ntekan [enter] untuk melihat bantuan (dokumentasi) kelas: ')
help(Pagar)  # untuk melihat dokumentasi kelas
```

**Hasilnya:**

```bash
$ python kelas_pagar.py
kelas pagar untuk membuat objek pagar.
dibuat oleh Yanyan Sofiyan
sebagai contoh saja.

tekan [enter] untuk melihat bantuan (dokumentasi) kelas:
```
Setelah _Enter_ ditekan:

```bash
Help on class Pagar in module main:
class Pagar
| kelas pagar untuk membuat objek pagar.
| dibuat oleh Yanyan Sofiyan
| sebagai contoh saja.
|
| Methods defined here:
|
| __init__(self, warna, tinggi, bahan)
(END)
```

## Apa Selanjutnya?

Itulah beberapa aturan dasar penulisan sintaks Python.

Selebihnya anda bisa pelajari atau bisa membaca beberapa _style guide_ seperti:

- PEP 8 – Style Guide for Python Code https://www.python.org/dev/peps/pep-0008/
- Python Style Guide Google https://github.com/google/styleguide/blob/gh-pages/pyguide.md

Selanjutnya kita akan belajar tentang:

- `Variabel` dan `Tipe` data pada Python

## Referensi

- https://docs.python.org/3/
- https://www.python.org/dev/peps/pep-0008/
- Python Style Guide Google https://github.com/google/styleguide/blob/gh-pages/pyguide.md