# Cloud Computing Part 7 [ Pemateri : Tiara Dwi Maulita Sari ]

## Introduction
Pada kali ini kita akan belajar tentang :
- Amazon Relational Database Service ( Amazon RDS )
- Amazon DynamoDB
- Amazon Redshift
- Amazon Aurora

## Cloud Research

#  Amazon Relational Database Service ( Amazon RDS )
Amazon RDS adalah layanan terkelola yang mengatur dan mengoperasikan basis data relasional di cloud. Untuk mengatasi tantangan menjalankan basis data relasional yang mandiri dan tidak dikelola, AWS menyediakan layanan yang mengatur, mengoperasikan, dan menskalakan basis data relasional tanpa administrasi yang terus-menerus. Amazon RDS menyediakan kapasitas hemat biaya dengan ukuran yang dapat diubah, dan mengotomatiskan tugas administrasi yang menyita waktu. Amazon RDS memungkinkan Anda fokus pada aplikasi agar dapat memberikan kinerja, ketersediaan tinggi, keamanan, dan kompatibilitas yang dibutuhkan aplikasi. Dengan Amazon RDS, fokus utama Anda adalah data dan mengoptimalkan aplikasi Anda. Dengan Amazon RDS, Anda mengelola optimalisasi aplikasi Anda. AWS mengelola penginstalan dan patching sistem operasi, penginstalan dan patching perangkat lunak basis data, pencadangan otomatis, dan ketersediaan tinggi.

 Instans basis data adalah lingkungan basis data terisolasi yang dapat berisi beberapa basis data yang dibuat pengguna. Basis data ini dapat diakses menggunakan alat bantu dan aplikasi yang sama seperti yang Anda gunakan dengan instans basis data mandiri. Sumber daya dalam instans basis data ditentukan oleh kelas instans basis data, dan tipe penyimpanan ditentukan oleh tipe disk. 

## Ketersediaan tinggi dengan Deployment multi-AZ (1 dari 2)
Salah satu fitur yang paling kuat dari Amazon RDS adalah kemampuan untuk mengonfigurasi instans basis data Anda untuk ketersediaan tinggi dengan Deployment multi-AZ. Setelah Deployment multi-AZ dikonfigurasi, Amazon RDS secara otomatis membuat salinan siaga instans basis data di Availability Zone lain dalam VPC yang sama. Setelah salinan basis data dihasilkan, transaksi direplikasi ke salinan siaga secara sinkronis.

## Ketersediaan tinggi dengan Deployment multi-AZ (2 dari 2)
Oleh karena itu, jika instans basis data utama gagal dalam Deployment multi-AZ, Amazon RDS akan secara otomatis memunculkan instans basis data siaga daring sebagai instans utama yang baru. Replikasi sinkron meminimalkan potensi kehilangan data. Karena aplikasi Anda merujuk basis data berdasarkan nama menggunakan endpoint Sistem Nama Domain (DNS) Amazon RDS.

## Kapan Menggunakan Amazon RDS
Gunakan Amazon RDS saat aplikasi Anda memerlukan: 
- Transaksi kompleks atau kueri kompleks
- Tingkat kueri atau tulis medium ke tinggi –hingga 30.000 IOPS (15.000 baca + 15.000 tulis)
- Tidak lebih dari satu node pekerja atau shard.
- Ketahanan tinggi
Jangan gunakan Amazon RDS ketika aplikasi Anda memerlukan:
- Nilai baca/tulis besar (misalnya, 150.000 tulis per detik)
- Sharding karena permintaan ukuran data atau throughput yang tinggi
- Permintaan GET atau PUT sederhana dan kueri yang dapat ditangani basis data NoSQL
- Atau, penyesuaian sistem manajemen basis data relasional (RDBMS)

# Amazon DynamoDB
Amazon DynamoDB adalah layanan basis data NoSQL yang cepat dan fleksibel untuk semua aplikasi yang memerlukan latensi satu digit milidetik yang konsisten pada segala skala. Amazon mengelola semua infrastruktur data inti untuk layanan ini dan secara redundan menyimpan data di beberapa fasilitas di Wilayah AS asli sebagai bagian dari arsitektur yang toleran terhadap kesalahan. Dengan DynamoDB, Anda dapat membuat tabel dan item. Anda dapat menambahkan item ke dalam tabel. Sistem akan secara otomatis membagi data Anda dan memiliki penyimpanan tabel untuk memenuhi persyaratan workload. Tidak ada batas praktis pada jumlah item yang dapat Anda simpan dalam tabel. Misalnya, beberapa pelanggan memiliki tabel produksi yang berisi miliaran item.

Komponen DynamoDB inti adalah tabel, item, dan atribut.
- Tabel adalah kumpulan data.
- Item adalah grup atribut yang dapat diidentifikasi secara unik di antara semua item lainnya.
- Atribut adalah elemen data dasar, sesuatu yang tidak perlu diuraikan lebih lanjut

# Amazon Redshift
Amazon Redshift adalahgudang data yang cepat dan terkelola penuh, yang memudahkan dan menghemat biaya dalam menganalisis semua data Anda menggunakan SQL standar dan alat bantu Kecerdasan Bisnis (BI) Anda yang sudah ada. Berikut adalah apa yang ditawarkan Amazon Redshift dan cara menggunakannya untuk aplikasi analitik. Analitik penting untuk bisnis saat ini, tetapi membangun gudang data tidaklah mudah dan tentunya mahal. Penyiapan gudang data dapat berlangsung selama berbulan-bulan dan menghabiskan anggaran secara signifikan

# Amazon Aurora
Amazon Aurora adalah basis data relasional yang kompatibel dengan MySQL dan PostgreSQL yang dibangun untuk cloud. Basis data ini menggabungkan kinerja dan ketersediaan basis data komersial kelas atas dengan kesederhanaan dan penghematan biaya basis data sumber terbuka. Menggunakan Amazon Aurora dapat mengurangi biaya basis data Anda, sekaligus meningkatkan keandalan dan ketersediaan basis data. Sebagai layanan terkelola penuh, Aurora didesain untuk mengotomatiskan tugas-tugas yang menyita waktu seperti penyediaan, patching, pencadangan, pemulihan, deteksi kegagalan, dan perbaikan.

## Manfaat layanan Amazon Aurora
- Ketersediaan Tinggi
- Desain Tangguh

# Knowledge 
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/7d316441-a66b-422d-9ea0-c2af6ff5d323)


