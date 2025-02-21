# Deteksi Tepi dan Segmentasi Citra dengan Python

Repositori ini berisi kode Python untuk mendemonstrasikan deteksi tepi dan segmentasi citra menggunakan berbagai metode populer dalam pemrosesan gambar digital. Kode ini memanfaatkan library seperti OpenCV, Scikit-image, NumPy, dan Matplotlib untuk melakukan operasi dan visualisasi.

## Deteksi Tepi

Deteksi tepi adalah proses fundamental dalam pemrosesan gambar yang bertujuan untuk mengidentifikasi perubahan signifikan dalam intensitas piksel. Ini berguna untuk mendeteksi batas objek, fitur, dan perubahan mendadak dalam suatu gambar. Kode ini mengimplementasikan empat operator deteksi tepi yang berbeda:

### 1. Operator Roberts

Operator Roberts adalah operator deteksi tepi berbasis gradien yang menggunakan kernel 2x2 untuk mendekati turunan gambar. Ia menghitung perbedaan intensitas piksel antara piksel yang berdekatan secara diagonal. Karena kesederhanaannya, operator Roberts relatif cepat tetapi sensitif terhadap noise dan mungkin tidak mendeteksi tepi yang lemah dengan baik.

### 2. Operator Sobel

Operator Sobel adalah operator deteksi tepi berbasis gradien lain yang menggunakan kernel 3x3 untuk menghitung aproksimasi gradien gambar. Ia lebih efektif dalam mendeteksi tepi vertikal dan horizontal dibandingkan dengan operator Roberts dan kurang sensitif terhadap noise.

### 3. Operator Prewitt

Operator Prewitt mirip dengan operator Sobel dalam hal menggunakan kernel 3x3, tetapi menggunakan bobot yang berbeda untuk menghitung gradien gambar. Ini menghasilkan respons yang sedikit berbeda dibandingkan dengan operator Sobel, dan terkadang dapat mendeteksi tepi tertentu dengan lebih baik.

### 4. Detektor Tepi Canny

Detektor tepi Canny adalah algoritma deteksi tepi multi-tahap yang memberikan deteksi tepi yang akurat dan kuat. Ia melibatkan penghalusan gambar dengan filter Gaussian, menghitung gradien intensitas gambar, menerapkan penekanan non-maksimum untuk mengidentifikasi tepi yang paling signifikan, dan menggunakan ambang batas ganda untuk melacak tepi yang lemah yang terhubung ke tepi yang kuat.

Kode tersebut memuat gambar, menerapkan setiap operator deteksi tepi, dan menampilkan gambar asli dan gambar tepi yang dihasilkan berdampingan untuk perbandingan.

## Segmentasi Citra

Segmentasi citra adalah proses membagi gambar menjadi beberapa segmen atau wilayah yang berbeda berdasarkan karakteristik seperti intensitas, warna, atau tekstur. Kode ini mendemonstrasikan segmentasi citra menggunakan algoritma K-Means, metode pengelompokan populer dalam pembelajaran mesin.

### Algoritma K-Means

Algoritma K-Means bekerja dengan mempartisi data ke dalam sejumlah klaster yang telah ditentukan sebelumnya berdasarkan jarak antara titik data dan pusat klaster. Dalam konteks segmentasi citra, setiap piksel diperlakukan sebagai titik data, dan algoritma mengelompokkan piksel yang serupa ke dalam klaster yang sama.

Kode tersebut pertama kali memuat gambar dan mengubahnya menjadi ruang warna RGB. Kemudian, piksel gambar diubah menjadi array NumPy, dan algoritma K-Means diterapkan untuk mengelompokkan piksel ke dalam sejumlah klaster yang telah ditentukan. Gambar yang tersegmentasi dibuat dengan menetapkan setiap piksel ke warna pusat klasternya. Gambar asli dan gambar yang tersegmentasi ditampilkan berdampingan untuk memvisualisasikan hasilnya.

## Cara Menjalankan Kode

1. Pastikan Anda telah menginstal library yang diperlukan: OpenCV, NumPy, Scikit-image, dan Matplotlib. Anda dapat menginstalnya menggunakan `pip`:
2. Unggah gambar Anda ke lingkungan Google Colab.
3. Jalankan kode tersebut. Anda akan diminta untuk memilih file gambar untuk diunggah.
4. Kode tersebut akan menampilkan gambar asli dan gambar tepi/segmentasi yang dihasilkan.
