## **Jawaban Latihan 1: Konversi ke Ternary**

Tugasnya adalah mengubah blok `if-else` ini menjadi satu baris:

```python
# Kode Asli
umur = 20
kategori = ""

if umur < 18:
    kategori = "Anak-anak"
else:
    kategori = "Dewasa"
```

**Solusi Menggunakan Operator Ternary:**

```python
umur = 20

# Solusi:
kategori = "Anak-anak" if umur < 18 else "Dewasa"

print(kategori)
```

**Output:**

```
Dewasa
```

**Pembahasan:**

  * **Kondisi:** `umur < 18` (Hasilnya `False` karena `20 < 18` adalah `False`).
  * **Nilai jika True:** `"Anak-anak"`
  * **Nilai jika False:** `"Dewasa"`
    Karena kondisi bernilai `False`, operator ternary mengembalikan "Nilai jika False", yaitu `"Dewasa"`.

-----

## **Jawaban Latihan 2.1: Hitung Manual Bitwise**

Tugasnya adalah menghitung hasil dari `9 | 5`.

**1. Konversi ke Biner:**

  * Angka `9` dalam biner adalah `1001`
      * $(1 \times 2^3) + (0 \times 2^2) + (0 \times 2^1) + (1 \times 2^0) = 8 + 0 + 0 + 1 = 9$
      * (Bisa juga dicek dengan `bin(9)` -\> `'0b1001'`)
  * Angka `5` dalam biner adalah `0101`
      * $(0 \times 2^3) + (1 \times 2^2) + (0 \times 2^1) + (1 \times 2^0) = 0 + 4 + 0 + 1 = 5$
      * (Bisa juga dicek dengan `bin(5)` -\> `'0b101'`. Kita tambahkan 0 di depan agar sejajar: `0101`)

**2. Operasi `|` (OR):**

Operator `|` (OR) akan menghasilkan `1` jika **salah satu** bitnya adalah `1`.

```
  1001  (Desimal 9)
| 0101  (Desimal 5)
-------
  1101
```

  * Bit kanan: `1 | 1 = 1`
  * Bit kedua: `0 | 0 = 0`
  * Bit ketiga: `0 | 1 = 1`
  * Bit kiri: `1 | 0 = 1`

**3. Konversi Hasil ke Desimal:**

Hasil binernya adalah `1101`.

  * $(1 \times 2^3) + (1 \times 2^2) + (0 \times 2^1) + (1 \times 2^0)$
  * $= 8 + 4 + 0 + 1$
  * $= 13$

**Jadi, hasil dari `9 | 5` adalah `13`.**

**4. Verifikasi di Python:**

```python
print(9 | 5)
```

**Output:**

```
13
```