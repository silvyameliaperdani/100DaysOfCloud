# Cloud Computing Part 5 [ Pemateri : Tiara Dwi Maulita Sari ]

## Introduction




## Cloud Research
# Komputasi 
## Tinjauan umum layanan Komputasi 
- Amazon Elastic Compute Cloud(Amazon EC2) menyediakan mesin virtual yang ukurannya dapat diubah.
- Amazon EC2 Auto Scalingmendukung ketersediaan aplikasi dengan memungkinkan Anda menentukan kondisi yang secara otomatis akan meluncurkan atau mengakhiri EC2 instance.
- Amazon Elastic Container Registry(Amazon ECR) digunakan untuk menyimpan dan mengambil image Docker.
- Amazon Elastic Container Service (Amazon ECS)adalah layanan orkestrasi kontainer yang mendukung Docker.
- VMware cloud on AWSmemungkinkan Anda menyediakan cloud hybrid tanpa perangkat keras kustom.
- AWS Elastic Beanstalkmenyediakan cara sederhana untuk menjalankan dan mengelola aplikasi web.
- AWS Lambda adalah solusi komputasi nirserver. Anda cukup membayar waktu komputasi yang digunakan.
- Amazon Elastic Kubernetes Service (Amazon EKS) memungkinkan Anda menjalankan Kubernetes terkelola di AWS.
- Amazon Lightsail menyediakan layanan sederhana untuk membangun aplikasi atau situs web.
- AWS Batchmenyediakan alat untuk menjalankan tugas batch pada skala apa pun.
- AWS Fargate menyediakan cara untuk menjalankan kontainer yang mengurangi kebutuhan Anda untuk mengelola server atau kluster.
- AWS Outposts menyediakan cara untuk menjalankan layanan AWS pilihan di pusat data on-premise Anda.
- AWS Serverless Application Repository menyediakan cara untuk menemukan, men-deploy, dan memublikasikan aplikasi nirserver

**Amazon EC2** menyediakan mesin virtual, dan Anda dapat menganggapnya sebagai infrastructure as a service (IaaS). Layanan IaaS memberikan fleksibilitas dan meninggalkan banyak tanggung jawab manajemen server untuk Anda.
**AWS Lambda** adalah platform komputasi tanpa administrasi. AWS Lambda memungkinkan Anda menjalankan kode tanpa menyediakan atau mengelola server. Anda cukup membayar waktu komputasi yang digunakan. Konsep teknologi nirserver ini relatif baru bagi banyak profesional IT.

## Amazon EC2
Amazon Elastic Compute Cloud (Amazon EC2) menyediakan mesin virtual agar Anda dapat meng-host jenis aplikasi yang sama yang mungkin dijalankan pada server on-premise tradisional. Layanan ini menyediakan kapasitas komputasi yang aman dan ukurannya dapat diubah di cloud. EC2 instance dapat mendukung berbagai beban kerja. Penggunaan umum untuk EC2 instance termasuk, namun tidak terbatas pada:
- Server aplikasi
- Server web
- Server basis data
- Server game
- Server email
- Server media
- Server katalog
- Server file
- Server komputasi
- Server proxy
Singkatan EC2 di Amazon EC2 adalah **Elastic Compute Cloud**:
- Elastic artinya Anda dapat dengan mudah menambah atau mengurangi jumlah server yang dijalankan untuk mendukung aplikasi secara otomatis.
- Compute mengacu pada alasan sebagian besar pengguna menjalankan server, yaitu untuk meng-host aplikasi yang berjalan atau memproses data—tindakan yang memerlukan sumber daya komputasi, termasuk daya pemrosesan (CPU) dan memori (RAM).
- Cloud mengacu pada fakta bahwa EC2 instance yang Anda jalankan di-host di cloud. Amazon EC2 menyediakan mesin virtual di cloud dan memberi Anda kontrol administratif penuh atas sistem operasi Windows atau Linux yang berjalan pada instans. Sebagian besar sistem operasi server didukung, termasuk: Windows 2008, 2012, 2016, dan 2019, Red Hat, SuSE, Ubuntu, dan Amazon Linux.

## Meluncurkan Amazon EC2 Instance
Pertama kali Anda meluncurkan Amazon EC2 instance, Anda mungkin akan menggunakan Wizard Peluncuran Instans AWS Management Console
>> Pilih AMI - Amazon Machine Image (AMI)memberikan informasi yang dibutuhkan untuk meluncurkan EC2 instance
>> Pilih Tipe Instance - Amazon EC2 menyediakan berbagai pilihan tipe instansyang dioptimalkan untuk kasus penggunaan berbeda. Tipe instans terdiri atas berbagai kombinasi CPU, memori, penyimpanan, dan kapasitas jaringan
>> Penanaman dan ukuran jenis EC2 Instance - Penanaman tipe instance (contoh : t3.micro) T adalah nama family nya, 3 adalah generasinya, micro adalah ukurannya
**Beberapa tipe instans lebih detail**:
  - Instans T3 menyediakaninstans tujuan umum berkinerja burstable yang memberikan garis dasar kinerja CPU dengan kemampuan untuk melonjak di atas garis dasar. Kasus penggunaan untuk tipe instans ini mencakup situs web dan aplikasi web, lingkungan pengembangan, server pembangun, repositori kode, layanan mikro, lingkungan pengujian dan tahapan, dan aplikasi lini bisnis.
  - InstansC5 dioptimalkan untuk beban kerja dengan komputasi intensif, dan memberikan kinerja tinggi hemat biaya dengan harga rendah per rasio komputasi. Kasus penggunaannya meliputi pemodelan ilmiah, pemrosesan batch, penayangan iklan, game multipemain yang dapat diskalakan, dan pengodean video.
  - Instans R5 dioptimalkan untuk aplikasi intensif memori. Kasus penggunaan mencakup basis data kinerja tinggi, penambangan dan analisis data, basis data dalam memori, cache dalam memori dengan skala web terdistribusi, aplikasi yang menjalankan pemrosesan real-time untuk big data tidak terstruktur, klaster Apache Hadoop atau Apache Spark, dan aplikasi perusahaan lainnya.
  
>> Tentukan Pengaturan jaringan
Ketika Anda meluncurkan sebuah instans dalam VPC default, AWS akan memberinya alamatIP publik secara default. Ketika Anda meluncurkan instans ke VPC nondefault, subnet memiliki atribut yang menentukan apakah instans yang diluncurkan ke subnet itu menerima alamat IP publik dari kumpulan alamat IPv4 publik. Secara default, AWS tidak akan menetapkan alamat IP publik ke instans yang diluncurkan di subnet nondefault.

>> Lampiran IAM role ( Opsional )
Anda sebaiknya jangan pernah menyimpan kredensial AWS pada EC2 instance. Itu sangat tidak aman. Sebagai gantinya, lampirkan IAM role ke EC2 instance. IAM role kemudian memberikan izin untuk membuat permintaan antarmuka pemrograman aplikasi (API) untuk aplikasi yang berjalan pada EC2 instance. Profil instans adalah kontainer untuk IAM role.Jika Anda menggunakan AWS Management Console untuk membuat peran bagi Amazon EC2, konsol tersebut secara otomatis membuat profil instans dan memberikan nama yang sama dengan peran. Ketika Anda kemudian menggunakan konsol Amazon EC2 untuk meluncurkan instans dengan IAM role, Anda dapat memilih peran untuk dikaitkan dengan instans. Di konsol tersebut, daftar yang ditampilkan sebenarnya adalah daftar nama profil instans

>>  Skrip Data pengguna (Opsional)
Ketika Anda membuat EC2 instance, Anda memiliki pilihan untuk mengirimkan data penggunake instans. Data pengguna dapat mengautomasi penyelesaian instalasi dan konfigurasi pada peluncuran instans. skrip data pengguna dapat melakukan patch dan memperbarui sistem operasi instans, mengambil dan menginstal kunci lisensi perangkat lunak, atau menginstal perangkat lunak tambahan. Ketika EC2 instance dibuat, skrip data pengguna akan berjalan dengan hak istimewa root selama fase akhir proses booting. Pada instans Linux, itu dijalankan oleh layanan cloud-init. Pada instans Windows, itu dijalankan oleh utilitas EC2Config atau EC2Launch. Secara default, data pengguna hanya berjalan saat pertama kali instans dimulai.

>> Tentukan Penyimpanan
 Saat meluncurkan EC2 instance, Anda dapat mengonfigurasi opsi penyimpanan. Misalnya, Anda dapat mengonfigurasi ukuran volume root tempat sistem operasi tamu diinstal .Untuk setiap volume yang akan dimiliki instans Anda, Anda dapat menentukan ukuran disk, jenis volume, dan apakah penyimpanan akan dipertahankan jika instans diakhiri. Anda juga harus menentukan apakah enkripsi perlu digunakan.

**Pilihan penyimpanan Amazon EC2**
- Amazon Elastic Block Store ( Amazon EBS)
  Volume penyimpanan tingkat blok yang tahan lama, dapat menghentikan instance serta memulainya lagi, dan datanya akan tetap ada disana.
- Amazon EC2 Instance Store
    Penyimpanan Ephemeral disediakan pada disk yang melekat pada komputer host tempat ec2 isntance berjalan. Jika instance berhenti, data yang di simpan akan dihapus
- Pilihan lain untuk penyimpanan (bukan untuk volume root)
  - Pasang sistem file Amazon Elastic File System ( Amazon EFS)
  - Sambungkan ke Amazon Simple Storage Service ( Amazon S3)

  >> Tambahkan Tag
  Tag adalah label yang dapat Anda tetapkan ke sumber daya AWS. Setiap tag berisikuncidan nilai opsional, keduanya Anda yang tentukan. Tag memungkinkan Anda mengategorikan sumber daya AWS, seperti EC2 instance, dengan cara berbeda. Misalnya, Anda dapat memberi tag pada instans berdasarkan tujuan, pemilik, atau lingkungan.
  
  >> Pengaturan Grup Keamanan
  Suatu grup keamanan bertindak sebagai firewall virtual yang mengontrol lalu lintas untuk satu instans atau lebih. Ketika meluncurkan instans, Anda dapat menentukan satu grup keamanan atau lebih; jika tidak, grup keamanan default digunakan. Anda dapat menambahkan aturanke setiap grup keamanan. Aturan memungkinkan lalu lintas ke atau dari instans terkait. Anda dapat mengubah aturan untuk grup keamanan kapan saja, dan aturan baru akan diterapkan secara otomatis ke semua instans yang terkait dengan grup keamanan.
  
  >> Mengidentifikasi / Membuat pasangan kunci
  Amazon EC2 menggunakan kriptografi kunci–publik untuk mengenkripsi dan mendekripsi informasi login. Teknologi ini menggunakankunci publikuntuk mengenkripsi potongan data, lalu penerima menggunakan kunci pribadi untuk mendekripsi data. Kunci publik dan pribadi dikenal sebagai pasangan kunci. Kriptografi kunci publik memungkinkan Anda mengakses instans Anda secara aman dengan menggunakan kunci privat, bukan kata sandi.

**Sebagian besar pengaturan yang Anda tentukan selama peluncuran akan terlihat di panel Deskripsi. Informasi tentang instans tersedia termasuk informasi alamat IP dan alamat DNS, tipe instans, ID instans unik yang ditetapkan ke instans, ID AMI yang digunakan untuk meluncurkan instans, ID VPC, ID subnet, dan lainnya.
  **
## Luncurkan EC2 Instance dengan AWS Command Line 
- EC2 instance juga dapat dibuat secara terprogram
- Perintahnya mencakup informasi berikut:
   - aws –Menentukan pemanggilan utilitas baris perintah aws.
   - ec2 –Menentukan pemanggilan perintah layanan ec2.
   - run-instances –Adalah subperintah yang sedang dipanggil.
Perintah lainnya menentukan beberapa parameter, termasuk:
    - image-id -Parameter ini diikuti oleh ID AMI. Semua AMI memiliki ID AMI yang unik.
    - count -Anda dapat menentukan lebih dari satu.
    - instance-type –Anda dapat menentukan tipe instans untuk membuat (misalnya) instans c3.large
    - key-name –Dalam contoh, anggaplah bahwa MyKeyPairsudah ada.
    - security-groups -Dalam contoh ini, anggaplah bahwa MySecurityGroupsudah ada.
    - region -AMI berada di Wilayah AWS, sehingga Anda harus menentukan Wilayah tempat AWS CLI menemukan AMI dan meluncurkan EC2 instance.
  Perintah akan berhasil membuat EC2 instance jika:
    - Perintah terbentuk dengan benar
    - Sumber daya yang dibutuhkan perintah sudah ada
    - Anda memiliki izin yang cukup untuk menjalankan perintah
    - Anda memiliki kapasitas yang cukup di akun AWS
  Jika perintah berhasil, API merespons perintah dengan ID instans dan data lain yang relevan bagi aplikasi Anda untuk digunakan dalam permintaan API berikutnya.

## Siklus hidup Amazon EC2 Instance 
- Tertunda : Ketika sebuah instans pertama kali diluncurkan dari AMI, atau ketika Anda memulai instans yang dihentikan, instans masuk ke keadaan tertunda ketika instans di-boot dan di-deploy ke komputer host.
- Reboot : AWS merekomendasikan untuk me-reboot instans dengan menggunakan konsol Amazon EC2, AWS CLI, atau AWS SDK, bukan memanggil reboot dari sistem operasi (OS) tamu. Instans yang di-reboot menetap pada host fisik yang sama, mempertahankan nama DNS publik dan alamat IP publik yang sama, dan jika memiliki volume tempat penyimpanan instans, mempertahankan data pada volume tersebut.
- Dimatikan : Keadaan ini merupakan keadaan di antara berjalandan diakhiri. 
- Diakhiri : Instans yang diakhiri tetap terlihat di konsol Amazon EC2 untuk sementara waktu sebelum mesin virtual dihapus. Namun, Anda tidak dapat terhubung atau memulihkan instans yang diakhiri.
- Berhenti : Instans yang didukung oleh AmazonEBS dapat dihentikan. Instans memasuki status berhentisebelum mencapai keadaan berhentisepenuhnya.
- Dihentikan : Instans yang dihentikantidak akan dikenakan biaya yang sama dengan instans berjalan. Memulaiinstans yang dihentikan menempatkannya kembali ke keadaan tertunda, dan memindahkan instans ke mesin host baru.


### Pertimbangan untuk menggunakan alamat IP Elastis 
Suatu alamat IP publik adalah alamat IPv4 yang dapat dijangkau dari internet. Setiap instans yang menerima alamat IP publik juga diberikan nama host DNS eksternal. Contohnya, jika alamat IP publik yang ditetapkan ke instans adalah 203.0.113.25, nama host DNS eksternal mungkinec2-203-0-113-25.compute-1.amazonaws.com.Jika Anda menentukan bahwa alamat IP publik harus ditetapkan ke instans, alamat itu akan ditetapkan dari kumpulan alamat IPv4 publik AWS. Alamat IP publik tidak terkait dengan akun AWS Anda.

### Metadata EC2 Instance 
Metadata instans adalah data tentang instans Anda. Anda dapat melihatnya saat Anda terhubung ke instans. Untuk mengaksesnya di browser, buka URL berikut: http://169.254.169.254/latest/meta-data/. Data juga dapat dibaca secara terprogram, seperti dari jendela terminal yang memiliki utilitas cURL. Di jendela terminal, jalankan curl http://169.254.169.254/latest/meta-data/untuk mengambilnya. Alamat IP 169.254.169.254adalah alamat tautan lokal dan hanya valid dari instans tersebut.

## Amazon CloudWatch untuk pemantauan 
Anda dapat memantau instans dengan menggunakan Amazon CloudWatch, yang mengumpulkan dan memproses data mentah dari Amazon EC2 menjadi metrik yang mudah dibaca hampir secara real-time. Statistik ini dicatat selama 15 bulan, sehingga Anda dapat mengakses informasi historis dan mendapatkan perspektif lebih baik tentang kinerja aplikasi web atau layanan Anda.


# Mengoptimalkan Biaya Amazon EC2 
Amazon menawarkan model harga yang berbeda yang dapat dipilih ketika Anda ingin menjalankan EC2 instance. 
Penagihan per detik hanya tersedia untuk Instans Sesuai Permintaan, Instans Cadangan, dan Instans Spot yang menjalankan Amazon Linux atau Ubuntu.
- **Instans** Sesuai Permintaan memenuhi syarat untuk AWS Tingkat Gratis. Instans ini memiliki biaya di muka paling rendah dan fleksibilitas paling besar. Tidak ada komitmen di muka atau kontrak jangka panjang. 
- **Host Khusus** adalah server fisik dengan kapasitas instans yang khusus untuk Anda gunakan. Anda dapat menggunakan lisensi perangkat lunak per-soket, per-inti, atau per-VM yang ada, seperti untuk Microsoft Windows atau Microsoft SQL Server. 
- **Instans Khusus** adalah instans yang berjalan di virtual private cloud (VPC) dalam perangkat keras yang dikhususkan untuk satu pelanggan. Instans ini secara fisik diisolasi pada tingkat perangkat keras host dari instans milik akun AWS lainnya.
- **Instans Cadangan** memungkinkan Anda memesan kapasitas komputasi untuk jangka waktu 1 tahun atau 3 tahun dengan biaya operasional per jam yang lebih rendah. Harga penggunaan diskon selalu tetap selama Anda memiliki Instans Cadangan. Jika Anda mengharapkan penggunaan yang konsisten dan berat, instans ini dapat memberikan penghematan besar dibandingkan dengan Instans Sesuai Permintaan.
- **Instans Cadangan Terjadwal** memungkinkan Anda membeli pencadangan kapasitas yang berulang secara harian, mingguan, atau bulanan, dengan durasi tertentu, untuk jangka waktu 1 tahun. Anda membayar untuk waktu yang dijadwalkan ke instans, bahkan jika Anda tidak menggunakannya. 
- **Instans Spot** memungkinkan Anda menawar EC2 instance yang tidak terpakai, sehingga dapat menurunkan biaya Anda. Harga per jam untuk Instans Spot berfluktuasi tergantung pada penawaran dan permintaan. Instans Spot Anda berjalan setiap kali tawaran Anda melebihi harga pasar saat itu.

Setiap model harga Amazon EC2 memberikan serangkaian manfaat berbeda. Instans Sesuai Permintaan paling fleksibel, tanpa kontrak jangka panjang dan tarif rendah. Instans Spotmemberikan skala besar dengan harga diskon yang signifikan. Instans Cadanganadalah pilihan yang baik jika Anda memiliki kebutuhan komputasi terprediksi atau terus-menerus (misalnya, instans yang ingin terus Anda jalankan sebagian besar atau sepanjang waktu selama berbulan-bulan atau bertahun-tahun).HostKhusus adalah pilihan yang baik ketika Anda memiliki pembatasan lisensi untuk perangkat lunak yang ingin dijalankan di Amazon EC2, atau ketika Anda memiliki kepatuhan atau persyaratan peraturan tertentu yang menghalangi Anda menggunakan opsi deployment lainnya.


## 4 Pilar pengoptimalan Biaya 
- Ukuran Tepat
- Tingkatan Elastisitas
- Model Harga Optimal
- Optimalkan pilihan Penyimpanan


# Layanan Kontainer 
Kontainer merupakan metode virtualisasi sistem operasiyang memungkinkan Anda menjalankan aplikasi dan dependensinya dalam proses yang sumber dayanya terisolasi. Dengan kontainer, Anda mudah mengemas kode aplikasi, konfigurasi, dan dependensi menjadi unsur fundamental yang dapat menghasilkan konsistensi lingkungan, efisiensi operasional, produktivitas developer, dan kontrol versi

# Docker
Platform perangkat lunak yang mengemas perangkat lunak (seperti aplikasi) ke dalam kontainer. Docker diinstal pada setiap server yang akan meng-host kontainer, dan akan menyediakan perintah sederhana yang dapat Anda gunakan untuk membangun, memulai, atau menghentikan kontainer.Dengan menggunakan Docker, Anda dapat dengan cepat men-deploy dan menskalakan aplikasi ke lingkungan apa pun.

# Amazon Elastic Container Service 
Amazon Elastic Container Service (Amazon ECS) adalah layanan manajemen kontainer berkinerja tinggi dan sangat mudah diskalakan yang mendukung kontainer Docker. Amazon ECS memudahkan Anda menjalankan aplikasi di kluster Amazon EC2 instance yang terkelola.

## Apa itu Kubernetes 
Kubernetesadalah perangkat lunak sumber terbuka untuk orkestrasi kontainer. Kubernetes dapat bekerja dengan banyak teknologi kontainerisasi, termasuk Docker. Karena ini adalah proyek sumber terbuka yang populer, komunitas besar developer dan perusahaan membangun ekstensi, integrasi, dan plugin yang menjaga perangkat lunak tetap relevan, dan menambahkan fitur baru dan yang banyak diminta secara berkala.Kubernetes memungkinkan Anda men-deploy dan mengelola aplikasi kontainerdalam skala besar. Dengan Kubernetes, Anda dapat menjalankan semua jenis aplikasi kontainer menggunakan peralatan yang sama di pusat data on-premise dan cloud.

# Amazon Elastic Kubernetes Service 

