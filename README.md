#Contours

Konsep active contours model pertama kali diperkenalkan oleh M. Kass et
al (1987). Active Contour menggunakan prinsip energi minimizing yang
mendeteksi fitur tertentu dalam suatu citra. Sistem ini terdiri dari sekumpulan titik
yang saling berhubungan dan terkontrol oleh garis lurus. Active contour
digambarkan sebagai sejumlah titik yang berurutan satu sama lain. Penentuan
obyek dalam citra melalui active contour merupakan proses interaktif, sehingga
contour akan tertarik kearah fitur didalam citra atau image karena pengaruh energi
internal yang menghasilkan gambar

import cv2: perintah untuk mengimpor pustaka OpenCV (Open Source Computer Vision Library).

import numpy:Ini adalah perintah untuk mengimpor pustaka NumPy. NumPy adalah pustaka Python yang digunakan untuk melakukan operasi numerik dan pemrosesan array multidimensi.

Fungsi cv2.imread() digunakan untuk membaca gambar dari file dan mengonversinya menjadi matriks NumPy yang mewakili citra.

cv2.resize() untuk mengubah ukuran gambar. Fungsi ini digunakan untuk mengubah ukuran gambar menjadi ukuran yang diinginkan. Argumen pertama adalah gambar yang ingin diubah ukurannya (image), argumen kedua (None) adalah ukuran gambar tujuan yang ingin diubah menjadi, dan argumen terakhir (fx=0.9,fy=0.9) adalah faktor skala dalam arah horizontal (fx) dan vertikal (fy). Dalam kode yang Anda berikan, faktor skala adalah 0.9, yang berarti gambar akan diubah menjadi 90% dari ukuran aslinya baik secara horizontal maupun vertikal.

cv2.cvtColor() digunakan untuk mengubah ruang warna (color space) dari citra. Argumen pertama (image) adalah citra yang ingin diubah ruang warnanya, dan argumen kedua (cv2.COLOR_BGR2GRAY) adalah kode konversi warna yang menentukan konversi dari BGR ke grayscale.

(cv2.THRESH_BINARY+cv2.THRESH_OTSU) adalah metode yang digunakan untuk menentukan ambang batas secara otomatis.

cv2.findContours() digunakan untuk menemukan kontur objek dalam citra biner. Argumen pertama (binary) adalah citra biner di mana kontur akan dicari. Argumen kedua (mode=cv2.RETR_TREE) adalah mode pengambilan kontur yang menentukan bagaimana hubungan hierarki antara kontur akan dihitung. Dalam kasus ini, mode cv2.RETR_TREE digunakan untuk menghitung semua hubungan hierarki kontur.

Argumen ketiga (method=cv2.CHAIN_APPROX_NONE) adalah metode aproksimasi kontur yang menentukan cara kontur akan direpresentasikan. Dalam kasus ini, cv2.CHAIN_APPROX_NONE digunakan untuk menyimpan semua titik kontur tanpa aproksimasi.

cv2.drawContours() digunakan untuk menggambar kontur pada gambar image_copy.

cv2.imshow('Grayscale Image', gray): Membuka jendela tampilan dengan judul "Grayscale Image" dan menampilkan citra skala abu-abu yang disimpan dalam variabel gray.

cv2.imshow('Drawn Contours', image_copy): Membuka jendela tampilan dengan judul "Drawn Contours" dan menampilkan gambar yang telah digambar konturnya yang disimpan dalam variabel image_copy.

cv2.imshow('Binary Image', binary): Membuka jendela tampilan dengan judul "Binary Image" dan menampilkan citra biner yang disimpan dalam variabel binary.

cv2.waitKey(0): Fungsi ini akan menunggu hingga pengguna menekan tombol apa pun pada keyboard. Jika nilai parameter yang diberikan adalah 0 (seperti dalam contoh ini), fungsi ini akan terus menunggu hingga pengguna menekan tombol apa pun. Setelah pengguna menekan tombol, program akan melanjutkan eksekusi.

cv2.destroyAllWindows(): Fungsi ini menutup semua jendela tampilan yang dibuka oleh OpenCV. Setelah fungsi ini dipanggil, semua jendela tampilan yang sebelumnya dibuka akan ditutup dan program akan selesai.

#referensi
https://www.tutorialspoint.com/matplotlib/matplotlib_contour_plot.htm

http://e-journal.uajy.ac.id/6120/3/MTF201846.pdf
