Proyek Portofolio: Paginasi Data dengan LIMIT dan OFFSET di PostgreSQL
Ringkasan Proyek
Proyek ini bertujuan untuk mendemonstrasikan keahlian dalam menggunakan klausa LIMIT dan OFFSET pada SQL. Analisis ini menunjukkan bagaimana cara mengambil data dalam jumlah terbatas dan membaginya menjadi halaman-halaman yang lebih kecil (paginasi), sebuah teknik fundamental dalam pengembangan aplikasi yang berurusan dengan data dalam jumlah besar.

Dataset
Dataset yang digunakan adalah database sampel dvdrental, sebuah skema database umum untuk latihan PostgreSQL. Database ini berisi informasi rinci tentang toko penyewaan DVD, termasuk tabel untuk film, aktor, pelanggan, dan transaksi penyewaan.

Alat yang Digunakan
Database: PostgreSQL

Aplikasi Database: DBeaver

Bahasa Pemrograman: SQL

Implementasi dan Kode SQL
Berikut adalah contoh kueri SQL yang menunjukkan penggunaan LIMIT dan OFFSET untuk paginasi data pada tabel film.

1. Mengambil 10 Film Termahal (Halaman Pertama)
Kueri ini menggunakan LIMIT untuk mengambil 10 film dengan biaya penyewaan (rental rate) tertinggi.

SELECT
    title,
    rental_rate
FROM
    film
ORDER BY
    rental_rate DESC
LIMIT 10;

2. Mengambil 10 Film Berikutnya (Halaman Kedua)
Kueri ini menggunakan OFFSET untuk melewati 10 baris pertama dan mengambil 10 baris berikutnya, yang efektif untuk paginasi.

SELECT
    title,
    rental_rate
FROM
    film
ORDER BY
    rental_rate DESC
LIMIT 10 OFFSET 10;

Kesimpulan
Proyek ini menunjukkan pemahaman saya tentang:

Paginasi Data: Menggunakan LIMIT dan OFFSET untuk mengelola dan menampilkan data dalam jumlah besar secara efisien.

Kueri SQL yang Efisien: Menulis kueri yang dioptimalkan untuk performa.

Manajemen Data: Mengurutkan dan memfilter data untuk mendapatkan wawasan yang relevan.

Ini adalah bukti kemampuan saya dalam menerapkan konsep SQL untuk memecahkan tantangan umum dalam analisis dan pengembangan data.
