# **Modul Praktikum 7: Algoritma Pencarian (*Searching*)**

Selamat datang di modul ketujuh\! 

Kita memiliki data yang tersimpan di dalam List (seperti yang dipelajari di Modul 5). 

Masalahnya, bagaimana jika datanya ada ribuan atau jutaan? Bagaimana cara kita menemukan **satu** data spesifik dengan cepat?

Di sinilah **Algoritma Pencarian** berperan. Kita akan mempelajari dua metode paling fundamental: 
1. **Linear Search** dan 
2. **Binary Search**.

**Tujuan Pembelajaran:**

1.  Memahami logika dasar pencarian data.
2.  Mampu mengimplementasikan **Linear Search** (pencarian berurutan).
3.  Mampu mengimplementasikan **Binary Search** (pencarian bagi dua) pada data terurut.
4.  Memahami perbedaan performa/kecepatan antara keduanya.
5.  **Studi Kasus:** Program Pencarian Data Mahasiswa.

## **1. Linear Search (Pencarian Berurutan)**

Ini adalah metode yang paling sederhana dan alami.

**Konsep:**
Bayangkan Anda mencari baju merah di tumpukan pakaian yang berantakan. Anda akan mengambil satu per satu baju dari atas sampai bawah hingga menemukan yang merah.

  * Cek elemen pertama -\> Bukan? -\> Cek elemen kedua -\> Bukan? -\> dst.

**Kelebihan & Kekurangan:**

  * ✅ **Kelebihan:** Sangat mudah dikoding, tidak perlu data yang terurut (bisa acak).
  * ❌ **Kekurangan:** Lambat jika datanya sangat banyak (misal 1 juta data).

**Implementasi Python:**

```python
def linear_search(data_list, target):
    # Telusuri dari indeks 0 sampai akhir
    for i in range(len(data_list)):
        if data_list[i] == target:
            return i  # Mengembalikan indeks jika ketemu
    return -1  # Mengembalikan -1 jika tidak ketemu

# Contoh Penggunaan
data_angka = [10, 50, 30, 70, 80, 20]
cari = 30

hasil = linear_search(data_angka, cari)
if hasil != -1:
    print(f"Data ditemukan pada indeks ke-{hasil}")
else:
    print("Data tidak ditemukan.")
```

-----

## **2. Binary Search (Pencarian Bagi Dua)**

Ini adalah metode yang jauh lebih cerdas dan cepat, **TAPI** memiliki satu syarat mutlak: **Data harus SUDAH TERURUT (Sorted)**.

**Konsep:**
Bayangkan Anda mencari kata "Komputer" di Kamus Besar Bahasa Indonesia.

1.  Anda tidak akan membuka dari halaman 1 (seperti Linear Search).
2.  Anda akan membuka langsung di **tengah**.
3.  Jika halaman tengah berawalan huruf "M", dan Anda mencari "K" (sebelum "M"), maka Anda membuang bagian kanan (N-Z) dan hanya fokus mencari di bagian kiri (A-M).
4.  Ulangi proses membagi dua ini sampai ketemu.

**Implementasi Python:**

```python
def binary_search(data_list, target):
    low = 0
    high = len(data_list) - 1

    while low <= high:
        mid = (low + high) // 2  # Cari titik tengah
        guess = data_list[mid]

        if guess == target:
            return mid  # Ketemu!
        if guess > target:
            high = mid - 1  # Target ada di sebelah kiri
        else:
            low = mid + 1   # Target ada di sebelah kanan
            
    return -1  # Tidak ketemu

# PENTING: Data harus urut dulu!
data_urut = [10, 20, 30, 50, 70, 80] 
cari = 70

hasil = binary_search(data_urut, cari)
print(f"Binary Search: Data ditemukan pada indeks ke-{hasil}")
```

-----

## **3. Diskusi: Linear vs Binary**

Coba diskusikan skenario ini:

Anda memiliki buku telepon cetak berisi 1.000.000 nama yang sudah urut abjad.

1.  **Menggunakan Linear Search:**
      * Kasus Terburuk: Nama yang dicari ada di halaman terakhir (misal: "Zoro"). Anda harus mengecek 1.000.000 kali.
2.  **Menggunakan Binary Search:**
      * Kasus Terburuk: Berapa kali Anda perlu membagi buku itu?
      * Hanya butuh sekitar **20 langkah**\! ($2^{20} \approx 1.000.000$).

**Kesimpulan:** Binary search jauh lebih efisien untuk data besar, tetapi "biaya"-nya adalah kita harus mengurutkan datanya terlebih dahulu.

-----

## **4. Tugas Praktikum: Pencarian Data Mahasiswa**

Buatlah program pencarian data mahasiswa sederhana yang menggabungkan konsep **`List`**, **`Fungsi`**, dan **`Searching`**.

**Skenario:**
Anda adalah admin yang memiliki daftar Nomor Induk Mahasiswa (NIM) yang hadir pada ujian. Daftar ini masih acak (belum urut).

**Data Awal (Copy ke kodemu):**

```python
nim_hadir = [
    "1015", "1002", "1010", "1008", 
    "1020", "1005", "1012", "1001"
]
```

**Instruksi Tugas:**

1.  Buat fungsi `linear_search_nim(list_nim, cari_nim)` untuk mencari NIM.
2.  Di program utama, minta user memasukkan NIM yang ingin dicari.
3.  Tampilkan pesan "Mahasiswa dengan NIM [X] HADIR" atau "TIDAK HADIR".
4.  **(Tantangan/Bonus):**
      * Urutkan list `nim_hadir` menggunakan metode `.sort()`.
      * Buat fungsi `binary_search_nim` dan gunakan untuk mencari NIM tersebut.
      * Bandingkan hasilnya (pastikan outputnya sama).

**Contoh Output Program:**

```
Daftar NIM Hadir: ['1015', '1002', '1010', ...]

Masukkan NIM yang dicari: 1005
Status: Mahasiswa dengan NIM 1005 HADIR (Ditemukan di indeks 5)

Masukkan NIM yang dicari: 9999
Status: Mahasiswa dengan NIM 9999 TIDAK HADIR
```