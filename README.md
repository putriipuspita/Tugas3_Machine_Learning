# K-Means Clustering pada Dataset Online Retail

[![Profil](https://img.shields.io/badge/1237050111-Putri%20Puspita-8A2BE2)](https://github.com/putriipuspita)

## Deskripsi Project

Project ini merupakan implementasi algoritma **K-Means Clustering** menggunakan dataset **Online Retail**. Tujuan dari project ini adalah mengelompokkan data transaksi berdasarkan karakteristik pembelian menggunakan variabel **Quantity** dan **UnitPrice**.

Metode clustering digunakan untuk menemukan pola atau kelompok data yang memiliki karakteristik serupa tanpa memerlukan label kelas sebelumnya.

---

## Dataset

Dataset yang digunakan adalah **Online Retail Dataset** yang berisi informasi transaksi penjualan suatu toko online.

### Atribut yang digunakan

* Quantity
* UnitPrice

Atribut lain tidak digunakan dalam proses clustering karena tidak secara langsung merepresentasikan karakteristik transaksi yang akan dikelompokkan.

---

## Tahapan Analisis

### 1. Import Library

Library yang digunakan:

* Pandas
* NumPy
* Matplotlib
* Scikit-Learn

### 2. Data Preprocessing

Tahapan preprocessing yang dilakukan:

* Membaca dataset CSV
* Mengubah tipe data UnitPrice menjadi numerik (float)
* Menghapus missing value
* Menghapus data tidak valid (Quantity ≤ 0 dan UnitPrice ≤ 0)
* Menghapus outlier ekstrem untuk meningkatkan kualitas clustering

### 3. Normalisasi Data

Data dinormalisasi menggunakan metode **MinMaxScaler** agar seluruh fitur berada pada rentang nilai yang sama.

### 4. K-Means Clustering

Model K-Means dibangun dengan parameter:

* Jumlah cluster (K) = 3
* Random State = 42

### 5. Evaluasi Model

Evaluasi dilakukan menggunakan **Silhouette Score** untuk mengukur kualitas cluster yang terbentuk.

---

## Hasil Clustering

### Jumlah Data Setiap Cluster

| Cluster | Jumlah Data |
| ------- | ----------: |
| 0       |      20.172 |
| 1       |         697 |
| 2       |       2.599 |

### Rata-rata Karakteristik Tiap Cluster

| Cluster | Quantity | UnitPrice |
| ------- | -------: | --------: |
| 0       |     4.69 |      3.27 |
| 1       |    60.88 |      1.41 |
| 2       |    25.07 |      1.56 |

---

## Interpretasi Cluster

### Cluster 0

Karakteristik:

* Quantity rendah
* UnitPrice relatif lebih tinggi dibanding cluster lain

Cluster ini merepresentasikan transaksi dengan jumlah pembelian kecil namun harga produk relatif lebih tinggi.

### Cluster 1

Karakteristik:

* Quantity paling tinggi
* UnitPrice rendah

Cluster ini menunjukkan transaksi pembelian dalam jumlah besar dengan harga produk yang relatif murah.

### Cluster 2

Karakteristik:

* Quantity menengah
* UnitPrice rendah

Cluster ini merepresentasikan transaksi dengan jumlah pembelian sedang dan harga produk yang relatif murah.

---

## Evaluasi Model

Nilai Silhouette Score yang diperoleh:

```text
0.6113936930582735
```

Nilai tersebut menunjukkan bahwa cluster yang terbentuk memiliki kualitas yang baik karena berada di atas 0.5. Hal ini menunjukkan bahwa data dalam satu cluster cukup mirip satu sama lain dan memiliki pemisahan yang cukup jelas dengan cluster lainnya.

---

## Kesimpulan

Berdasarkan hasil implementasi algoritma K-Means Clustering pada dataset Online Retail, berhasil terbentuk tiga kelompok transaksi dengan karakteristik yang berbeda.

Hasil evaluasi menggunakan Silhouette Score sebesar 0.6114 menunjukkan bahwa model clustering memiliki kualitas yang baik dalam memisahkan data ke dalam kelompok yang sesuai.

Metode K-Means dapat digunakan untuk membantu memahami pola transaksi pelanggan berdasarkan jumlah pembelian dan harga produk sehingga dapat mendukung proses segmentasi data dan analisis perilaku pelanggan.

---

## Tools dan Library

* Python
* Pandas
* NumPy
* Matplotlib
* Scikit-Learn

---

## Author

Putri Puspita
