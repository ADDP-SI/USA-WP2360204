# Deskripsi Tugas

Buatlah program Python yang mengimplementasikan berbagai operasi aritmatika dan penugasan untuk menyelesaikan masalah praktis dalam kehidupan sehari-hari.

## Learning Objectives

- Memahami penggunaan operator aritmatika (+, -, *, /, %, **, //)
- Menguasai operator penugasan (=, +=, -=, *=, /=, dll.)
- Menerapkan konsep dalam studi kasus nyata
- Mengembangkan logika pemrograman yang terstruktur

# Tugas 1: Kalkulator Keuangan Pribadi

## Deskripsi

Buat program untuk mengelola keuangan pribadi dengan fitur penghitungan pemasukan, pengeluaran, dan investasi.

## Persyaratan:

```python
# Data Awal
saldo_awal = 5000000
pemasukan_bulanan = 7500000
pengeluaran_tetap = 4500000
investasi_bulanan = 1000000

# TODO 1: Hitung saldo setelah pemasukan dan pengeluaran
# Gunakan operator aritmatika dasar
saldo_setelah_transaksi = # your code here

# TODO 2: Hitung total investasi setelah 6 bulan dengan bunga 5%
# Gunakan operator penugasan dan aritmatika
investasi_6_bulan = # your code here

# TODO 3: Hitung persentase tabungan dari pemasukan
# Gunakan operator modulus dan pembagian
persentase_tabungan = # your code here

# TODO 4: Prediksi saldo setelah 1 tahun dengan asumsi sama
# Gunakan operator penugasan majemuk
saldo_1_tahun = saldo_awal
# your code here - update saldo_1_tahun selama 12 bulan
```

## Output yang di harapkan:

```bash
=== HASIL KALKULASI KEUANGAN ===
Saldo Awal: Rp 5,000,000
Pemasukan Bulanan: Rp 7,500,000
Pengeluaran Tetap: Rp 4,500,000
Investasi Bulanan: Rp 1,000,000
========================================
1. Saldo setelah transaksi: Rp 8,000,000
2. Investasi 6 bulan (5% bunga): Rp 1,340,095.64
3. Persentase tabungan: 40.00%
4. Prediksi saldo 1 tahun: Rp 29,000,000
```

### Tips:

- Gunakan f-string untuk formatting output
