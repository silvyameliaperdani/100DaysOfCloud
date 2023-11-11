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

# Infrastruktur Global AWS
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/3b1b2b6c-b494-4bd8-b5ed-b11b61a5df62)
Untuk mempelajari lebih lanjut tentang Wilayah AWS yang saat ini tersedia, lihat: https://aws.amazon.com/about-aws/global-infrastructure/

Infrastruktur AWS Cloud dibangun di sekitar Wilayah. AWS memiliki 22 Wilayah di seluruh dunia. Satu Wilayah AWSadalah lokasi geografis fisik dengan satu atau beberapa Availability Zone. Availability Zone terdiri dari satu atau beberapa pusat data.Untuk mencapai toleransi kesalahan dan stabilitas, Wilayah diisolasi dari satu sama lain. Sumber daya di satu Wilayah tidak secara otomatis direplikasi ke Wilayah lain. Saat Anda menyimpan data di Wilayah tertentu, data Anda tidak direplikasi di luar Wilayah tersebut.Merupakan tanggung jawab Anda untuk mereplikasi data lintas Wilayah, jika bisnis Anda memerlukannya.Wilayah AWS yang diperkenalkan sebelum 20 Maret 2019diaktifkansecara default. Wilayah yang diperkenalkan setelah 20 Maret 2019—seperti Asia Pasifik (Hong Kong) dan Timur Tengah (Bahrain)—dinonaktifkansecara default. Anda harus mengaktifkan Wilayah ini sebelum Anda dapat menggunakannya. Anda dapat menggunakan AWS Management Console untuk mengaktifkan atau menonaktifkan Wilayah.Beberapa Wilayah memiliki akses terbatas. Akun Amazon AWS (Tiongkok) hanya menyediakan akses ke Wilayah Beijing dan Ningxi

## Avaibility Zone
Setiap Wilayah AWS memiliki banyak lokasi terisolasi yang dikenal sebagaiAvailability Zone.Setiap Availability Zone menyediakan kemampuan untuk mengoperasikan aplikasi dan basis data yang tersedia dengan sangat baik, toleran terhadap kesalahan, dan dapat diskalakan daripada yang mungkin dilakukan dengan satu pusat data. Setiap Availability Zone dapat mencakup beberapa pusat data (biasanya tiga), dan pada skala penuh, dapat mencakup ratusan ribu server. Availability Zone merupakan partisi Infrastruktur Global AWS yang terisolasi penuh. Availability Zone memiliki infrastruktur daya tersendiri, dan secara fisik berjarak sangat jauh dari Availability Zone lainnya tetapi semua Availability Zone berjarak 100 km satu sama lain. 

## Pusat Data AWS
- Pusat data AWS dirancang demi keamanan
- Pusat data adalah tempat data berada dan pemrosesan data terjadi
- Setiap data memiliki daya, jaringan, dan konektivitas berlebih, dan ditempatkan di pasilitas yang terpisah
- Pusat data biasanya memiliki 50.000 sampai 80.000 server fisik

## Points of Presence
Amazon CloudFrontadalah jaringan penyampaian konten(CDN) yang digunakan untuk mendistribusikan konten ke pengguna akhir untuk mengurangi latensi. Amazon Route 53 adalah layanan Domain Name System (DNS). Permintaan ke salah satu layanan ini akan dialihkan ke edge locationterdekat secara otomatis untuk menurunkan latensi.Points of PresenceAWS terletakdi sebagianbesarkotabesardi (total 69 kota) di 30 negaradi seluruhdunia. Denganterus mengukur konektivitas internet, kinerja, dan komputasi untuk menemukan cara terbaik untuk merutekan permintaan, Points of Presence memberikanpengalamanpenggunayang lebihbaikhampirsecarareal-time. TitikkehadiraninidigunakanolehbanyaklayananAWS, termasuklayananAmazon CloudFront, Amazon Route 53, AWS Shield, danAWS Web Application Firewall (AWS WAF).

## Fitur Infrastructure AWS 
AWS Global Infrastructure memiliki beberapa fitur berharga:
- Pertama, elastisdan dapat diskalakan. Ini berarti sumber daya dapat menyesuaikan dengan peningkatan atau penurunan kebutuhan kapasitas secara dinamis. Ini juga dapat dengan cepat menyesuaikan untuk mengakomodasi pertumbuhan.
- Kedua, infrastruktur initoleran terhadap kesalahan, yang berarti memiliki redundansi komponen bawaan yang memungkinkannya melanjutkan operasi meskipun komponen gagal.
- Terakhir, diperlukan sedikit atau tanpa intervensi manusia, sekaligus memberikan ketersediaan tinggidengan sedikit waktu henti.

### Poin Penting 
- Infrastruktur Global AWS terdiri dari Wilayah dan Availability Zone.
- Pilihan Wilayah Anda biasanya berdasarkan pada persyaratan kepatuhan atau untuk mengurangi latensi.
- Setiap Availability Zone terpisah secara fisik dari Availability Zone lainnya dan memiliki daya, jaringan, dan konektivitas berlebih.
- Edge location dan cache edge Regional meningkatkan kinerja dengan melakukan cache konten lebih dekat ke pengguna.

# Ikhtisar Layanan AWS dan Kategori Layanan
Seperti yang dibahas sebelumnya, Infrastruktur Global AWS dapat dibagi menjadi tiga elemen: Wilayah, Availability Zone, dan Points of Presence, yang disertai edge location. Infrastruktur ini menyediakan platform untuk serangkaian layanan yang luas, seperti jaringan, penyimpanan, layanan komputasi, dan basis data—serta layanan ini dikirimkan sebagai utilitas sesuai permintaan yang tersedia dalam hitungan detik, dengan harga sesuai pemakaian
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/19f281c7-9a76-48be-89e8-2a664e3d9e17)

AWS menawarkan serangkaian layanan berbasis cloud. Ada 23 kategori produk atau layanan yang berbeda, dan masing-masing kategori terdiri dari satu atau beberapa layanan. Kursus ini tidak akan mencoba untuk memperkenalkan Anda ke setiap layanan. Sebaliknya, fokus dari kursus ini adalah pada layanan yang paling banyak digunakan dan menawarkan pengenalan terbaik ke AWS Cloud.

## Kategori Layanan Penyimpanan
Layanan penyimpanan AWS mencakup layanan yang tercantum di sini, dan lainnya.
- Amazon Simple Storage Service (Amazon S3) adalah layanan penyimpanan objek yang menawarkan skalabilitas, ketersediaan data, keamanan, dan kinerja. Gunakan layanan ini untuk menyimpan dan melindungi sejumlah data untuk situs web, aplikasi seluler, pencadangan dan pemulihan, arsip, aplikasi perusahaan, perangkat Internet of Things (IoT), dan analitik big data.
- Amazon Elastic Block Store (Amazon EBS)adalah penyimpanan blok berkinerja tinggi, yang dirancang untuk digunakan dengan Amazon EC2 untuk beban kerja intensif throughput dan transaksi. Layanan ini digunakan untuk beragam beban kerja, seperti basis data relasional dan non-relasional, aplikasi perusahaan, aplikasi kontainer, mesin analitik big data, sistem file, dan alur kerja media.
- Amazon Elastic File System (Amazon EFS)menyediakan Sistem File Jaringan (NFS) elastis, dapat diskalakan, dan terkelola sepenuhnya untuk digunakan dengan layanan AWS Cloud dan sumber daya on-premise. Amazon EFS dibuat untuk menskalakan sesuai permintaan hingga petabyte, tumbuh dan menyusut secara otomatis ketika Anda menambahkan dan menghapus file. Layanan ini mengurangi kebutuhan untuk menyediakan dan mengelola kapasitas guna mengakomodasi pertumbuhan.
- Amazon Simple Storage Services Glacieradalah kelas penyimpanan cloud Amazon S3 yang aman, tahan lama, dan berbiaya sangat rendah untuk pengarsipan data dan pencadangan jangka panjang. Dirancang untuk memberikan daya tahan sebesar 99,999999999%, dan untuk menyediakan kemampuan keamanan dan kepatuhan menyeluruh untuk memenuhi persyaratan hukum yang paling ketat.

## Kategori Layanan Komputasi 
- Amazon Elastic Compute cloud (Amazon EC2) menyediakan kapasitas komputasi yang aman dan fleksibel sebagai mesin virtual di cloud.
- Amazon EC2 Auto Scaling memungkinkan Anda menambah atau menghapus EC2 instance secara otomatis sesuai dengan kondisi yang Anda tetapkan.
- Amazon Elastic Container Service (Amazon ECS) adalah layanan orkestrasi kontainer berkinerja tinggi dan sangat mudah diskalakan yang mendukung kontainer Docker.
- Amazon Elastic Container Registry (Amazon ECR) merupakan registri kontainer Docker yang dikelola sepenuhnya yang memudahkan developer menyimpan, mengelola, dan men-deploy gambar kontainer Docker.
- AWS Elastic Beanstalk adalah layanan untuk men-deploy dan menskalakan aplikasi dan layanan web di server yang sudah dikenal, seperti Apache dan Microsoft Internet Information Services (IIS).
- AWS Lambda memungkinkan Anda menjalankan kode tanpa menyediakan atau mengelola server. Anda hanya membayar untuk waktu komputasi yang Anda gunakan. Tidak ada biaya ketika kode Anda tidak berjalan.
- Amazon Elastic Kubernetes Service (Amazon EKS) memudahkan untuk men-deploy, mengelola, dan menskalakan aplikasi dalam kontainer yang menggunakan Kubernetes di AWS.
- AWS Fargate adalah mesin komputasi untuk Amazon ECS yang memungkinkan Anda menjalankan kontainer tanpa harus mengelola server atau kluster.

## Kategori Layanan Basis Data
- Amazon Relational Database Service (Amazon RDS)memudahkan penyiapan, pengoperasian, dan penskalaan basis data relasional di cloud.
- Amazon Auroraadalah basis data relasional yang kompatibel dengan MySQL dan PostgreSQL
- Amazon Redshift memungkinkan Anda menjalankan pertanyaan analitik terhadap data berjumlah petabyte yang disimpan secara lokal di Amazon Redshift, dan langsung terhadap data berjumlah exabyte yang disimpan di Amazon S3.
- Amazon DynamoDB adalah basis data nilai kunci dan dokumen yang memberikan kinerja milidetik satu digit pada skala apa pun.

## Kategori Layanan Jaringan dan Penyampaian Konten 
- Amazon Virtual Private Cloud (Amazon VPC) memungkinkan Anda menyediakan bagian yang terisolasi secara logis dari AWS Cloud
- Elastic Load Balancing secara otomatis mendistribusikan lalu lintas aplikasi yang masuk di beberapa target, seperti Amazon EC2 instance, kontainer, alamat IP, dan fungsi Lambda.
- Amazon CloudFront adalah layanan jaringan penyampaian konten (CDN) cepat yang memberikan data, video, aplikasi, dan antarmuka pemrograman aplikasi (API) dengan aman kepada pelanggan secara global dengan latensi rendah dan kecepatan transfer tinggi.
- AWS Transit Gateway adalah layanan yang memungkinkan pelanggan menghubungkan Amazon Virtual Private Cloud (VPC) dan jaringan on-premise mereka ke satu gateway.
- Amazon Route 53 adalah layanan web Domain Name System (DNS) cloud yang dapat diskalakan yang dirancang untuk memberikan cara yang dapat diandalkan untuk merutekan pengguna akhir ke aplikasi internet.
- AWS Direct Connect menyediakan cara untuk membuat koneksi jaringan pribadi khusus dari pusat data atau kantor Anda ke AWS, yang dapat mengurangi biaya jaringan dan meningkatkan throughput bandwidth
- AWS VPN menyediakan terowongan pribadi yang aman dari jaringan atau perangkat Anda ke jaringan global AWS.

## Kategori Layanan Keamanan, Identitas, dan Kepatuhan 
- AWS Identity and Access Management (IAM)memungkinkan Anda mengelola akses layanan dan sumber daya AWS secara aman
- AWS Organizations memungkinkan Anda membatasi layanan dan tindakan apa yang diizinkan di akun Anda
- Amazon Cognito memungkinkan Anda menambahkan fungsi daftar, masuk, dan kontrol akses pengguna ke aplikasi web dan seluler Anda
- AWS Artifact memberikan akses sesuai permintaan ke laporan keamanan dan kepatuhan AWS dan perjanjian online tertentu
- AWS Key Management Service (AWS KMS) memungkinkan Anda membuat dan mengelola kunci.
- WS Shield adalah layanan perlindungan Distributed Denial of Service (DDoS) terkelola yang melindungi aplikasi yang berjalan di AWS

## Kategori Layanan Management biaya AWS 
- Laporan Penggunaan dan Biaya AWS berisi kumpulan data biaya dan penggunaan AWS terlengkap yang tersedia, termasuk metadata tambahan tentang layanan, harga, dan reservasi AWS
- AWS Budgets memungkinkan Anda mengatur anggaran kustom yang akan memberi Anda peringatan saat biaya atau penggunaan Anda melebihi (atau diprakirakan akan melebihi) jumlah yang Anda anggarkan
- AWS Cost Explorer memiliki antarmuka yang mudah digunakan yang memungkinkan Anda memvisualisasikan, memahami, serta mengelola biaya dan penggunaan AWS Anda dari waktu ke waktu.

## Kategori Layanan Management dan Tata Kelola 
- AWS Management Console memberikan antarmuka pengguna berbasis web untuk mengakses akun AWS Anda.
- AWS Config menyediakan layanan yang membantu Anda melacak inventaris dan perubahan sumber daya.
- Amazon CloudWatch memungkinkan Anda memantau sumber daya dan aplikasi.
- AWS Auto Scaling menyediakan fitur yang memungkinkan Anda menskalakan beberapa sumber daya untuk memenuhi permintaan.
- AWS Command Line Interface menyediakan alat terpadu untuk mengelola layanan AWS.AWS Trusted Advisor membantu Anda mengoptimalkan kinerja dan keamanan.
- AWS Well-Architected Tool menyediakan bantuan dalam meninjau dan meningkatkan beban kerja Anda.
- AWS CloudTrail melacak aktivitas pengguna dan penggunaan API

## Knowledge Chapter2
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/79f86f35-fb92-4d18-8e86-c6e914419db2)


##Knowledge Chapter3
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/2a03fff4-8eef-482f-b7d3-14d9eb7cf008)



