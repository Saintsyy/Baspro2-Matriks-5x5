
# 📊 Perkalian Matriks Sederhana dengan Python

Proyek ini adalah contoh sederhana bagaimana melakukan **perkalian matriks** manual menggunakan bahasa pemrograman Python, tanpa bantuan library eksternal.

## 🧩 Deskripsi Singkat

Program ini melakukan operasi perkalian antara dua matriks 5x5, yaitu **Matriks A** dan **Matriks B**. Prosesnya dilakukan menggunakan **nested loop** atau perulangan bersarang untuk menghitung setiap elemen hasil matriks.

## 📂 Penjelasan Kode

Berikut penjelasan mendetail dari setiap bagian kode:

### 1. Definisi Matriks A dan B

```python
A = [
    [1, 2, 3, 4, 5],
    [6, 7, 8, 9, 10],
    [11, 12, 13, 14, 15],
    [16, 17, 18, 19, 20],
    [21, 22, 23, 24, 25]
]

B = [
    [1, 0, 0, 0, 1],
    [0, 1, 0, 1, 0],
    [0, 0, 1, 0, 0],
    [0, 1, 0, 1, 0],
    [1, 0, 0, 0, 1]
]
```
- **Matriks A** adalah matriks dengan angka berurutan dari 1 sampai 25.
- **Matriks B** adalah matriks dengan pola tertentu, menyerupai kombinasi dari matriks identitas dan pola tambahan.

### 2. Persiapan Variabel untuk Hasil

```python
hasil = []
```
- List kosong ini akan menyimpan hasil akhir dari perkalian matriks A dan B.

### 3. Proses Perkalian Matriks

```python
for i in range(5):
    baris = []
    for j in range(5):
        total = 0
        for k in range(5):
            total += A[i][k] * B[k][j]
        baris.append(total)
    hasil.append(baris)
```
- **Perulangan pertama (`for i in range(5)`):**  
  Mengakses setiap baris dalam Matriks A.
  
- **Perulangan kedua (`for j in range(5)`):**  
  Mengakses setiap kolom dalam Matriks B.
  
- **Perulangan ketiga (`for k in range(5)`):**  
  Melakukan operasi perkalian elemen yang sesuai antara baris Matriks A dan kolom Matriks B, kemudian menjumlahkan hasil perkalian tersebut.

- **Hasilnya** disimpan dalam list `baris`, lalu setiap `baris` ditambahkan ke dalam list `hasil`.

### 4. Menampilkan Hasil

```python
print("Hasil Perkalian Matriks A dan B: ")
for row in hasil:
    print(row)
```
- Setelah semua perhitungan selesai, program akan mencetak hasil perkalian dalam format matriks.

## 💻 Hasil Output

Saat program dijalankan, hasilnya akan seperti berikut:

```
Hasil Perkalian Matriks A dan B:
[6, 6, 3, 6, 6]
[16, 17, 8, 17, 16]
[26, 28, 13, 28, 26]
[36, 39, 18, 39, 36]
[46, 50, 23, 50, 46]
```

## 📝 Catatan Tambahan

- Kode ini menggunakan metode manual agar lebih memahami proses perkalian matriks.
- Untuk penggunaan lebih lanjut atau matriks besar, disarankan menggunakan library seperti **NumPy** agar lebih efisien dan cepat.

Proyek ini open-source dan bebas digunakan untuk pembelajaran maupun pengembangan lebih lanjut.
