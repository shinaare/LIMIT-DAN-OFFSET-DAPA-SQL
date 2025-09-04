Proyek Portofolio: Analisis Data Aktor dengan SQL
Tujuan Proyek
Proyek ini bertujuan untuk menganalisis data dari tabel actor dalam database sampel dvdrental menggunakan SQL. Fokusnya adalah pada operasi data dasar seperti mengambil, mengurutkan, dan menghitung jumlah baris untuk mendapatkan wawasan tentang aktor-aktor yang terdaftar.

Dataset
Dataset yang digunakan adalah tabel actor dari database sampel dvdrental. Tabel ini berisi informasi tentang nama depan dan nama belakang aktor, serta waktu terakhir data mereka diperbarui.

Alat yang Digunakan
Database: PostgreSQL

Aplikasi Database: DBeaver

Bahasa Pemrograman: SQL

Langkah-Langkah Teknis
Berikut adalah Queri SQL yang digunakan untuk analisis data aktor.

1. Menampilkan Semua Aktor

Kueri ini mengambil semua kolom dari tabel actor untuk melihat struktur data secara keseluruhan.

SELECT *
FROM actor;

2. Mengambil Informasi Aktor Tertentu

Untuk melihat data dari aktor dengan ID tertentu, kita bisa menggunakan klausa WHERE.

SELECT
    first_name,
    last_name
FROM
    actor
WHERE
    actor_id = 1;

3. Mengurutkan Nama Aktor

Kita bisa mengurutkan data berdasarkan nama belakang (last_name) secara alfabetis untuk mendapatkan daftar aktor yang rapi.

SELECT
    first_name,
    last_name
FROM
    actor
ORDER BY
    last_name ASC;

4. Menggunakan LIMIT dan OFFSET untuk Paginasi

Untuk mendemonstrasikan kemampuan paginasi, saya akan mengambil 10 aktor pertama dan 10 aktor berikutnya dari daftar yang sudah diurutkan.

Halaman Pertama (10 Aktor Teratas):

SELECT
    first_name,
    last_name
FROM
    actor
ORDER BY
    last_name ASC
LIMIT 10;

Halaman Kedua (10 Aktor Berikutnya):

SELECT
    first_name,
    last_name
FROM
    actor
ORDER BY
    last_name ASC
LIMIT 10 OFFSET 10;


Kesimpulan dan Wawasan
Proyek ini menunjukkan bahwa saya memiliki kemampuan dasar yang kuat dalam menggunakan SQL untuk:

Mengambil dan memfilter data dari tabel.

Mengurutkan data untuk presentasi yang lebih baik.

Melakukan paginasi menggunakan LIMIT dan OFFSET, yang penting untuk mengelola dataset besar.

Menghitung jumlah data yang ada.

Ini adalah contoh yang baik untuk menunjukkan bagaimana keterampilan SQL dasar dapat digunakan untuk mendapatkan wawasan cepat dari data, yang merupakan langkah pertama dalam analisis data yang lebih kompleks.
