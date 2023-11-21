

# Cloud Computing Part 6 [ Pemateri : Tiara Dwi Maulita Sari ]

## Introduction
Pada Journey kali ini kita akan belajar : 
- Amazon Elastic Block Store (Amazon EBS)
- Amazon Simple Storage Service (Amazon S3)
- Amazon Elastic File System (Amazon EFS)
- Amazon Simple Storage Service Glacier

## Cloud Research
# Amazon Elastic Block Store ( Amazon EBS )
Amazon EBS memungkinkan Anda membuat volume penyimpanan individu dan melampirkannya ke instans Amazon EC2. Amazon EBS menawarkan penyimpanan tingkat blok, tempat volume direplikasi secara otomatis di Availability Zone-nya. Amazon EBS didesain untuk menyediakan penyimpanan tingkat blok yang tahan lama dan dapat dilepas (seperti hard drive eksternal) bagi instans Amazon EC2. Karena dipasang langsung pada instans, volume tersebut dapat menyediakan latensi rendah di antara tempat data disimpan dan tempat volume tersebut mungkin digunakan pada instans. Dengan demikian, volume tersebut dapat digunakan untuk menjalankan basis data dengan instans Amazon EC2. Volume Amazon EBS disertakan sebagai bagian dari cadangan instans ke Amazon Machine Image (atau AMI). AMI disimpan di Amazon S3 dan dapat digunakan kembali untuk membuat instans Amazon EC2 baru nantinya.Cadangan volume Amazon EBS disebut snapshot. Snapshot pertama disebut snapshot dasar. Snapshot lain setelah yang dasar hanya menangkap apa yang berbeda dari snapshot sebelumnya. 
Penggunaan volume Amazon EBS mencakup: 
- Volume boot dan penyimpanan untuk instans Amazon EC2
- Penyimpanan data dengan sistem file
- Host basis data
- Aplikasi korporas
Fitur Amazon EBS
- Snapshot
- Enkripsi
- Elastisitas

# Amazon Simple Storage Service ( Amazon S3 )
Amazon S3 adalah penyimpanan tingkat objek, yang artinya jika Anda ingin mengubah satu bagian file, Anda harus melakukan perubahan, lalu mengunggah ulang seluruh file yang diubah. Amazon S3 menyimpan data sebagai objek dalam sumber daya yang disebut bucket.
## Kelas Penyimpanan Amazon S3 
- Amazon S3 Standart
- Amazon S3 Intelligent-Tiering
- Amazon S3 Standard-Infrequent Access (Amazon S3 Standard-IA)
- Amazon S3 One Zone-Infrequent Access (Amazon S3 One Zone-IA)
- Amazon S3 Glacier
- Amazon S3 Glacier Deep Archive

# Amazon Elastic File System ( Amazon EFS )
Amazon Elastic File System (Amazon EFS)menyediakan penyimpanan file yang sederhana, dapat diskalakan, dan elastis untuk digunakan dengan layanan AWS dan sumber daya on-premise. Sistem ini memiliki antarmuka praktis yang memungkinkan Anda membuat dan mengonfigurasi sistem file dengan cepat dan mudah.Amazon EFS dibangun untuk menskalakan sesuai permintaan secara dinamis tanpa mengganggu aplikasi—yang akan tumbuh dan menyusut secara otomatis saat Anda menambahkan dan menghapus file. Amazon EFS didesain agar aplikasi Anda memiliki penyimpanan yang dibutuhkan, saat aplikasi membutuhkannya
## Fitur Amazon EFS
- Penyimpanan file di AWS Cloud
- Bekerja dengan baik untuk big data dan analitik, alur kerja pemrosesan media, manajemen konten, penayangan web, dan direktori rumah
- Sistem file berskala peta byte dan latensi rendah
- Penyimpanan bersama•Kapasitas elastis
- Mendukung Sistem File Jaringan(NFS) versi4.0 dan 4.1 (NFSv4)
- Kompatibel dengan semua AMI berbasis-Linux untuk Amazon EC2 

# Amazon S3 Glacier
Amazon S3 Glacier adalah layanan pengarsipan data yang didesain untuk keamanan, ketahanan, dan sangat hemat biaya.
- Amazon S3 Glacier didesain untuk memberikan daya tahan hingga 99,999999999% pada objek.
- Mendukung enkripsi data bergerak dan data diam melalui Secure Sockets Layer (SSL) atau Transport Layer Security (TLS).
- Fitur Vault Lock memberlakukan kepatuhan melalui kebijakan.
- Desain berbiaya sangat rendah ini ideal untuk pengarsipan jangka panjang.
- Menyediakan tiga opsi akses ke arsip—dipercepat, standar, dan massal—rentang waktu pengambilan berkisar dari beberapa menit hingga beberapa jam.



