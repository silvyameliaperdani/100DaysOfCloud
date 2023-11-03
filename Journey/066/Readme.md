# Cloud Computing Part 3 [ Pemateri : Tiara Dwi Maulita Sari ]

## Introduction
Pada Journey kali ini kita akan belajar tentang :
- Model Tanggung Jawab bersama AWS
- AWS Identity and Access Management ( IAM )
- Mengamankan akun AWS
- Mengamankan data di AWS
- Berupaya Memastikan Kepatuhan

## Cloud Research
# Model Tanggung Jawab bersama AWS 
AWS mengoperasikan, mengelola, dan mengontrol komponen dari lapisan virtualisasi perangkat lunak ke keamanan fisik fasilitas di mana layanan AWS beroperasi.AWS bertanggung jawabmelindungi infrastruktur yang menjalankan semua layanan yang ditawarkan di AWS Cloud. Infrastruktur ini terdiri atas perangkat keras, perangkat lunak, jaringan, dan fasilitas yang menjalankan layanan AWS Cloud.Pelanggan bertanggung jawab atas enkripsi data saat istirahat dan data dalam transit. Pelanggan juga harus memastikan bahwa jaringan dikonfigurasi untuk keamanan dan kredensial keamanan dan login dikelola dengan aman. Selain itu, pelanggan bertanggung jawab atas konfigurasi grup keamanan dan konfigurasi sistem operasi yang berjalan pada instans komputasi yang mereka luncurkan (termasuk pembaruan dan patch keamanan).

AWS bertanggung jawab atas infrastruktur fisik yang menyediakan sumber daya Anda, termasuk:
- Keamanan fisik pusat data dengan akses berbasis kebutuhan terkontrol; terletak di fasilitas yang tidak mencolok, dengan penjagaan keamanan 24/7; autentikasi dua faktor; logging dan peninjauan akses; pengawasan video; dan degaussing dan penghancuran disk.
- Infrastruktur perangkat keras,seperti server, perangkat penyimpanan, dan peralatan lain yang diandalkan AWS.
- Infrastruktur perangkat lunak,yang menyediakan sistem operasi, aplikasi layanan, dan perangkat lunak virtualisasi.
- Infrastruktur jaringan, sepertirouter, switch, load balancer, firewall, dan kabel. AWS juga terus memantau jaringan di batas-batas eksternal, mengamankan jalur akses, dan menyediakan infrastruktur redundan dengan deteksi gangguan

Walaupun infrastruktur cloud dijamin dan dikelola oleh AWS, pelanggan bertanggung jawab untuk keamanan semua yang mereka masukkan ke dalamcloud. Pelanggan bertanggung jawabatas apa yang dilaksanakan dengan menggunakan layanan AWS dan untuk aplikasi yang terhubung ke AWS. Langkah keamanan spesifik yang harus Anda ambil tergantung layanan yang Anda gunakan dan kerumitan sistem Anda.Tanggung jawab pelanggan termasuk memilih dan mengamankan sistem operasi instans, mengamankan aplikasi yang diluncurkan pada sumber daya AWS, konfigurasi grup keamanan, konfigurasi firewall, konfigurasi jaringan, dan manajemen akun aman.

# AWS Identity and Access Management ( IAM )
AWS Identity and Access Management (IAM)memungkinkan Anda mengontrol akses ke komputasi, penyimpanan, basis data, dan layanan aplikasi di AWS Cloud. IAM dapat digunakan untuk menangani autentikasi, dan untuk menentukan dan menegakkan kebijakan otorisasi sehingga Anda dapat menentukan pengguna yang dapat mengakses layanan. IAM adalah alat yang secara terpusat mengelola akses untuk meluncurkan, mengonfigurasi, mengelola, dan mengakhiri sumber daya di akun AWS Anda. Ini memberikan kontrol detail atas akses ke sumber daya, termasuk kemampuan untuk menentukan dengan tepat panggilan API mana yang diizinkan untuk dilakukan pengguna ke setiap layanan. Baik Anda menggunakan AWS Management Console, AWS CLI, maupun kit pengembangan perangkat lunak (SDK) AWS, setiap panggilan ke layanan AWS adalah panggilan API. Dengan IAM, Anda dapat mengelola sumber daya yangdapat diakses oleh siapa, dan bagaimanasumber daya ini dapat diakses.

## IAM MFA 
Layanan dan sumber daya AWS dapat diakses dengan menggunakan AWS Management Console, AWS CLI, atau melalui SDK dan API. Untuk keamanan yang meningkat, sebaiknya aktifkan MFA.Dengan MFA, pengguna dan sistem harus memberikan token MFA—selain kredensial masuk biasa—sebelum mereka dapat mengakses layanan dan sumber daya AWS

# Mengamankan Akun AWS
AWS merekomendasikan agar Anda menggunakan IAM untuk membuat pengguna tambahan dan menetapkan izin kepada pengguna ini, mengikuti prinsip hak istimewa terkecil. Misalnya, jika Anda memerlukan izin tingkat administrator, Anda dapat membuat pengguna IAM, memberikan akses penuh kepada pengguna tersebut, lalu menggunakan kredensial tersebut untuk berinteraksi dengan akun. Nantinya, jika Anda perlu mencabut atau mengubah izin Anda, Anda dapat menghapus atau mengubah kebijakan apa pun yang terkait dengan pengguna IAM tersebut.Selain itu, jika Anda memiliki beberapa pengguna yang memerlukan akses ke akun, Anda dapat membuat kredensial unik untuk setiap pengguna dan menentukan pengguna mana yang akan memiliki akses ke sumber daya mana. Misalnya, Anda dapat membuat pengguna IAM dengan akses hanya-baca ke sumber daya di akun AWS Anda dan mendistribusikan kredensialnya kepada pengguna yang memerlukan akses baca. Anda harus menghindari berbagi kredensial yang sama dengan beberapa pengguna.

Langkah lain yang disarankan untuk mengamankan akun AWS baru adalah untuk memerlukan otentikasi multifaktor (MFA) untuk login pengguna pengguna root dan untuk semua login pengguna IAM lainnya. Anda juga dapat menggunakan MFA untuk mengontrol akses program.

# Mengamankan Data di AWS 
Enkripsi data adalah alat penting untuk digunakan ketika tujuan Anda adalah untuk melindungi data digital. Enkripsi data mengambil data yang dapat dibaca dan mengodekannya sehingga tidak dapat dibaca oleh siapa pun yang tidak memiliki akses ke kunci rahasia yang dapat digunakan untuk memecahkan kode itu. Jadi, bahkan jika penyerang mendapatkan akses ke data Anda, mereka tidak bisa melakukan apa pun.Data saat istirahat mengacu pada data yang tersimpan secara fisik pada disk atau pita. AWS Certificate Manageradalah layanan yang memungkinkan Anda menyediakan, mengelola, dan men-deploy sertifikat SSL atau TLS untuk digunakan bersama dengan layanan AWS dan sumber daya terhubung internal Anda. Sertifikat SSL/TLS digunakan untuk mengamankan komunikasi jaringan dan membuat identitas situs web melalui internet serta sumber daya pada jaringan pribadi. Dengan AWS Certificate Manager, Anda dapat meminta sertifikat dan kemudian men-deploy-nya pada sumber daya AWS (seperti distribusi load balancers atau CloudFront).  AWS Certificate Manager juga menangani perpanjangan sertifikat.

# Bekerja untuk Memastikan Kepatuhan 
AWS Config adalah layanan yang memungkinkan Anda mengakses, mengaudit, dan mengevaluasi konfigurasi sumber daya AWS Anda. AWS Config terus memantau dan mencatat konfigurasi sumber daya AWS Anda dan memungkinkan Anda mengautomasi evaluasi konfigurasi tercatat terhadap konfigurasi yang diinginkan. Dengan Aws Config, Anda dapat meninjau perubahan dalam konfigurasi dan hubungan antara sumber daya AWS, meninjau riwayat konfigurasi sumber daya detail, dan menentukan kepatuhan Anda secara keseluruhan terhadap konfigurasi yang ditentukan dalam pedoman internal Anda. Ini memungkinkan Anda menyederhanakan audit kepatuhan, analisis keamanan, manajemen perubahan, dan pemecahan masalah operasional.Seperti yang Anda lihat di tangkapan layar AWS Config Dashboard yang ditampilkan di sini, AWS Config membuat cantuman inventaris semua sumber daya yang ada di akun, dan kemudian memeriksa kepatuhan aturan konfigurasi dan kepatuhan sumber daya. Sumber daya yang ditengarai tidak patuh akan ditandai, yang memperingatkan Anda terkait masalah konfigurasi yang harus ditangani dalam akun.AWS Config adalah layanan Wilayah. Untuk melacak sumber daya di seluruh Wilayah, aktifkan di setiap Wilayah yang Anda gunakan. AWS Config menawarkan fitur agregator yang dapat menunjukkan pandangan agregat sumber daya di beberapa Wilayah dan bahkan beberapa akun



