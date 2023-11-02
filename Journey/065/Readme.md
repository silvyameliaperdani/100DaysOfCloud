# Cloud Computing Part 2 [ Pemateri : Tiara Dwi Maulita Sari ]

## Introduction
Untuk journey kali ini adalah gabungan dari Modul 2 dan Modul 3, pada kesempatan kali ini kita akan mempelajari tentang :

## Pada Modul 2
- Dasar-Dasar Harga
- Total Biaya Kepemilikan
- AWS Organization
- Dukungan Teknis

## Pada Modul 3
- Infrastruktur Global AWS
- Ikhtisar Layanan AWS dan Kategori Layanan

## Cloud Research
# Dasar-Dasar Harga 
*Komputasi*  Dikenai biaya per jam / detik dan bervariasi sesuai tipe instance
*Penyimpanan* Dikenai biaya per GB
*Transfer Data* Data keluar dijumblahkan dan dikenakan biaya sedangkan data masuk tidak dikenai biaya dan dikenai biaya per GB

AWS menawarkan berbagai layanan komputasi cloud. Untuk setiap layanan, Anda membayar persis dengan jumlah sumber daya yang benar-benar Anda perlukan. Model harga bergaya utilitas ini meliputi:
- Bayar sesuai penggunaan
- Bayar lebih sedikit ketika melakukan pemesanan
- Bayar lebih sedikit saat menggunakan lebih banyak
- Bayar jauh lebih sedikit seiring berkembangnya AWS

### Bayar sesuai pemakaian 
Dengan AWS, Anda hanya membayar untuk layanan yang Anda konsumsi tanpa biaya di muka yang besar. Anda dapat menurunkan biaya variabel sehingga Anda tidak perlu lagi mendedikasikan sumber daya berharga untuk membangun infrastruktur berbiaya mahal, termasuk pembelian server, lisensi perangkat lunak, atau menyewa fasilitas

### Bayar lebih sedikit ketika melakukan pemesanan
Saat Anda membeli Instans Terpesan, Anda akan menerima diskon yang lebih besar saat melakukan pembayaran di muka yang lebih besar. Untuk memaksimalkan penghematan, Anda dapat membayar lunas di awal dan menerima potongan harga terbesar. RI Uang Muka Sebagian menawarkan potongan harga lebih rendah, tetapi memberikan pilihan untuk mengeluarkan biaya lebih sedikit di awal. Terakhir, Anda bisa memilih untuk tidak membayar apa pun di awal dan menerima potongan harga lebih kecil, yang memungkinkan Anda bebas menggunakan modal di proyek lain.

### Bayar lebih sedikit saat menggunakan lebih banyak
Dengan AWS, Anda bisa mendapatkan diskon berbasis volume dan mewujudkan penghematan penting seiring meningkatnya penggunaan Anda. Untuk layanan seperti Amazon Simple Storage Service (Amazon S3), harga memiliki tingkatan, yang artinya Anda membayar lebih sedikit per GB saat Anda menggunakan lebih banyak. Selain itu, transfer data masuk selalu gratis. Beberapa layanan penyimpanan memberikan biaya penyimpanan yang lebih rendah berdasarkan kebutuhan Anda. Hasilnya, seiring dengan meningkatnya kebutuhan penggunaan AWS Anda, Anda mendapat keuntungan dari skala ekonomi yang memungkinkan Anda meningkatkan adopsi dan menjaga biaya tetap terkendali.

### Bayar jauh lebih sedikit seiring berkembangnya AWS
AWS terus berfokus pada pengurangan biaya perangkat keras pusat data, meningkatkan efisiensi operasional, menurunkan konsumsi daya, dan secara umum menurunkan biaya dalam menjalankan bisnis.

# Total Biaya Kepemilikan
On-premise vs cloud adalah pertanyaan yang diajukan banyak bisnis. Perbedaan antara kedua opsi ini adalah bagaimana mereka di-deploy.Infrastruktur on-premise diinstal secara on-premise pada komputer dan server milik perusahaan. Ada beberapa biaya tetap yang juga dikenal sebagai biaya modal, yang berkaitan dengan infrastruktur tradisional. Biaya modal meliputi fasilitas, perangkat keras, lisensi, dan staf pemeliharaan. Meningkatkan skala mahal dan menyita waktu. Menurunkan skala tidak mengurangi biaya tetap

## Apa itu biaya kepemilikan ?
Total Biaya Kepemilikan adalah perkiraan keuangan untuk membantu mengidentifikasikan biaya langsung dan tidak langsung dari suatu sistem.
Di lingkungan cloud, TCO digunakan untuk membandingkan biaya menjalankan seluruh lingkungan infrastruktur untuk beban kerja tertentu di fasilitas on-premise atau kolokasi, dengan beban kerja yang sama berjalan di infrastruktur berbasis cloud. Perbandingan ini dilakukan untuk tujuan penganggaran atau guna membangun kasus bisnis untuk keputusan bisnis tentang solusi deployment optimal.

# AWS Organization
AWS Organizations adalah layanan manajemen akun yang memungkinkan Anda menggabungkan beberapa akun AWS ke sebuahorganisasiyang Anda buat dan kelola secara terpusat. AWS Organizations meliputi tagihan terkonsolidasi dan kemampuan manajemen akun yang membantu Anda memenuhi anggaran, keamanan, dan kebutuhan kepatuhan bisnis Anda dengan lebih baik.
Manfaat utama AWS Organizations adalah:
- Mengelola kebijakan akses secara terpusat di beberapa akun AWS.
- Mengontrol akses ke layanan AWS
- Mengautomasi pembuatan dan pengelolaan akun AWS
- Tagihan terkonsolidasi di beberapa akun AWS

## Fitur Utama dan Manfaat AWS Organization
AWS Organizations memungkinkan Anda:
- Membuat service control policies (SCP) yang secara terpusat mengontrol penggunaan layanan AWS di beberapa akun AWS
- Membuat grup akun dan kemudian melampirkan kebijakan ke dalam grup untuk memastikan kebijakan yang benar diterapkan di seluruh akun tersebut
- Menyederhanakan pengelolaan akun menggunakan antarmuka pemrograman aplikasi (API)untuk mengautomasi pembuatan dan pengelolaan akun AWS baru
- Menyederhanakan proses penagihan dengan menyiapkan metode pembayaran tunggal untuk semua akun AWS di organisasi Anda. Dengan tagihan terkonsolidasi, Anda dapat melihat tampilan tagihan terkonsolidasi yang dikeluarkan oleh semua akun Anda, dan Anda dapat memanfaatkan keuntungan harga dari penggunaan gabungan. Tagihan terkonsolidasi menyediakan lokasi pusat untuk mengelola penagihan di semua akun AWS Anda, dan kemampuan untuk mendapatkan keuntungan dari diskon volume

## Keamanan dengan AWS Organization
AWS Organizations tidak menggantikan kebijakan AWS Identity and Access Management (IAM)terkait dengan pengguna, grup, dan peran dalam akun AWS.Dengan kebijakan IAM, Anda dapat mengizinkan atau menolak akses ke layanan AWS (seperti Amazon S3), sumber daya AWS individu (seperti bucket S3 tertentu), atau tindakan API individu (seperti s3:CreateBucket). Kebijakan IAM hanya dapat diterapkan pada pengguna, grup, atau IAM role, dan tidak dapat membatasi root user akun AWS.

# Dukungan Teknis
- Menyediakan Kombinasi alat dan keahlian yang unik
   - AWS Support
   - Paket AWS Support
- Dukungan disediakan untuk
   - Bereksperimen dengan AWS
   - Penggunaan produksi AWS
   - Penggunaan AWS untuk bisnis penting
AWS Support dikembangkan untuk memberikan dukungan lengkap dan sumber daya yang tepat untuk membantu kesuksesan Anda. Kami ingin mendukung semua pelanggan kami, termasuk pelanggan yang mungkin bereksperimen dengan AWS, yaitu mereka yang mencari penggunaan produksi AWS, dan juga pelanggan yang menggunakan AWS sebagai sumber daya bisnis yang penting. AWS Support bervariasi berdasarkan jenis dukungan yang disediakan, tergantung pada kebutuhan dan tujuan pelanggan
Dengan AWS, pelanggan dapat merencanakan, men-deploy, dan mengoptimalkan dengan percaya diri.Jika Anda ingin bimbingan proaktif, AWS Support memiliki Manajer Akun Teknis (MAT)yang ditunjuk sebagai kontak utama pengguna. MAT dapat memberikan panduan, tinjauan arsitektur, dan komunikasi berkelanjutan yang terus menerus untuk memberi Anda informasi dan persiapan saat Anda merencanakan, men-deploy, dan mengoptimalkan solusi Anda.Jika Anda ingin memastikan bahwa Anda mengikuti praktik terbaik untuk meningkatkan performa dan toleransi kesalahan di lingkungan AWS, AWS Support memiliki AWS Trusted Advisor. AWS Trusted Advisor seperti ahli cloud yang disesuaikan. Ini adalah sumber daya online yang memeriksa peluang untuk mengurangi pengeluaran bulanan dan meningkatkan produktivitas. Untuk bantuan akun, Support Conciergeadalah ahli penagihan dan akun yang akan memberikan analisis cepat dan efisien mengenai masalah penagihan dan akun. Concierge menangani semua pertanyaan tingkat penagihan dan akun nonteknis

### Paket Basic Support menawarkan:
- Akses 7x24 jam ke layanan pelanggan, dokumentasi, whitepaper, dan forum dukungan.
- Akses ke enam pemeriksaan Trusted Advisor inti.
- Akses ke Personal Health Dashboard.
### Paket Developer Support
menawarkan sumber daya bagi pelanggan yang menguji atau melakukan pengembangan awal di AWS, serta semua pelanggan yang:
- Menginginkan akses ke panduan dan dukungan teknis.
- Menjelajahi cara cepat untuk menggunakan AWS.
- Menggunakan AWS untuk beban kerja atau aplikasi nonproduksi.
- Paket Business Supportmenawarkan sumber daya untuk pelanggan yang menjalankan beban kerja produksi di AWS dan semua pelanggan yang:
  - Menjalankan satu atau beberapa aplikasi di lingkungan produksi
  - Mengaktifkan beberapa layanan, atau menggunakan layanan utama secara ekstensif.
  - Bergantung pada solusi bisnis mereka agar tersedia, dapat diskalakan, dan aman.
### Paket Enterprise Support
  menawarkan sumber daya untuk pelanggan yang menjalankan bisnis dan beban kerja yang sangat penting di AWS dan semua pelanggan yang ingin:
  - Berfokus pada manajemen proaktif untuk meningkatkan efisiensi dan ketersediaan
  - Membangun dan mengoperasikan beban kerja yang mengikuti praktik terbaik AWS.
  - Menggunakan keahlian AWS untuk mendukung peluncuran dan migrasi.
  - Menggunakan Manajer Akun Teknis (MAT), yang menyediakan keahlian teknis untuk berbagai layanan AWS, serta memperoleh pemahaman detail tentang kasus penggunaan dan arsitektur teknologi Anda. Manajer Akun Teknis adalah kontak utama untuk kebutuhan dukungan yang sedang berjalan
