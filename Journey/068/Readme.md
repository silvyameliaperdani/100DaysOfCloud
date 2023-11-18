# Cloud Computing Part 4 [ Pemateri : Tiara Dwi Maulita Sari ]

## Introduction
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/7b121189-ee3d-41cb-89ac-c55dce26e090)

Pada pertemuan kali ini kita akan belajar mengenai VPC 
Topik yang akan dipelajari pada section kali ini adalah :
- Dasar-dasar Jaringan
- Amazon VPC
- Keamanan VPC
- Amazon Route 53
- Amazon CloudFront

Letsgooooo!!!

## Cloud Research
# Dasar-dasar Jaringan 

## Jaringan
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/72db8aaf-49a9-4cbe-bdd0-c6e7a66e099f)

Jaringan komputer mengacu pada perangkat komputasi yang saling terhubung serta dapat bertukar data dan berbagi sumber daya satu sama lain. Perangkat jaringan ini menggunakan sistem aturan, yang disebut sebagai protokol komunikasi, untuk mentransmisikan informasi melalui teknologi fisik atau nirkabel.

## Alamat IP 
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/c1330ca4-be84-4973-ba60-2a6cb2c2187c)

Setiap mesin client dalam jaringan memiliki alamat IP yang unik. Alamat IP adalah label numerik dalam format desimal. 

## Alamat IPv4 dan IPv6 

![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/58fdeace-8975-4d24-bc14-f21682db4fc2)

- Alamat IPv4 ada 32-bit **(Contoh nya : 192.168.22.1/24)**
- Alamat IPv6 ada 128-bit **(Alamat IPv6 terdiri dari delapan grup empat huruf dan angka yang dipisahkan oleh titik dua (:). Dalam contoh ini, alamat IPv6 adalah 2600:1f18:22ba:8c00:ba86:a05e:a5ba:00FF)**

## CIDR
Alamat CIDR dinyatakan sebagai berikut:
- Alamat IP (yang merupakan alamat pertama jaringan)
- Selanjutnya, karakter garis miring (/)
- Terakhir, nomor yang memberitahu Anda berapa banyak bit awalan perutean yang harus ditetapkan atau dialokasikan untuk pengidentifikasi jaringan
- Bit yang tidak tetap diperbolehkan untuk berubah. CIDR adalah cara untuk mengekspresikan grup alamat IP yang berturut-turut satu sama lain. Dalam contoh ini, alamat CIDR adalah 192.0.2.0/24. Angka terakhir (24) memberitahu Anda bahwa 24 bit pertama harus ditetapkan. 8 bit terakhir bersifat fleksibel, yang artinya 28(atau 256) alamat IP tersedia untuk jaringan, dengan rentang antara 192.0.2.0 hingga 192.0.2.255 Angka desimal keempat diperbolehkan untuk berubah dari 0 hingga 255.

  ## OSI ( Open Systems Interconnection)
  ![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/ee8d223f-b4a9-4b1b-8e39-a30cab2a2130)

Model Open Systems Interconnection (OSI) adalah kerangka kerja konseptual yang membagi fungsi komunikasi jaringan menjadi tujuh lapisan. Pengiriman data melalui jaringan sangat kompleks karena berbagai teknologi perangkat keras serta perangkat lunak harus bekerja secara kohesif melintasi batas-batas geografis dan politik. Model data OSI menyediakan bahasa universal untuk jaringan komputer, sehingga beragam teknologi dapat berkomunikasi menggunakan aturan komunikasi atau protokol standar. Setiap teknologi dalam lapisan khusus harus menyediakan kemampuan tertentu dan melakukan fungsi yang spesifik agar berguna dalam jaringan. Teknologi di lapisan yang lebih tinggi mendapatkan keuntungan dari abstraksi karena dapat menggunakan teknologi tingkat yang lebih rendah tanpa harus mengkhawatirkan detail implementasi yang mendasarinya

# Amazon VPC 
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/37d7f77f-5581-4e84-a9d2-fabc50361c22)

Amazon Virtual Private cloud (Amazon VPC) adalah layanan yang memungkinkan Anda menyediakan bagian yang terisolasi secara logis dari AWS cloud (disebut virtual private cloud, atau VPC), tempat Anda dapat meluncurkan sumber daya AWS anda

**VPC memberikan control atas sumber daya jaringan virtual anda, termasuk :**
 - IP Range
 - Subnet
 - Table Route
 - Gateway
 - NAT
 - Security Group

## VPC dan Subnet
Amazon VPC memungkinkan Anda menyediakan virtual private cloud (VPC). VPC adalah sebuah jaringan virtual yang terisolasi secara logis dari jaringan virtual lainnya di AWS Cloud.Sebuah VPC didedikasikan untuk akun Anda. VPC menjadi bagian dari satu Wilayah AWS dan dapat menjangkau beberapa Availability Zone.Setelah membuat VPC, Anda dapat membaginya menjadi satu subnet atau lebih. Subnet adalah rentang alamat IP dalam VPC.

## Pemberian Alamat IP 
Alamat IP memungkinkan sumber daya di VPC Anda berkomunikasi satu sama lain dan dengan sumber daya melalui internet. Ketika Anda membuat VPC, Anda menetapkan blok CIDR IPv4 (rentang alamat IPv4 privat) untuk VPC tersebut. Setelah membuat VPC, Anda tidak dapat mengubah rentang alamat, jadi penting untuk memilihnya dengan hati-hati.

## Alamat IP yang Dicadangkan 
Untuk setiap blok CIDR yang Anda tentukan, AWS mencadangkan lima alamat IP dalam blok tersebut, dan alamat ini tidak tersedia untuk digunakan. AWS mencadangkan alamat IP ini untuk:
- Alamat jaringan
- Perute lokal VPC (komunikasi internal)
- Resolusi Domain Name System (DNS)
- Penggunaan di masa mendatang
- Alamat siaran jaringan

## Jenis alamat IP Publik 
**Alamat IPv4 Publik :**
- Ditetapkan secara otomatis melalui pengaturan penetapan alamat IP public otomatis di tingkat subnet ( IP masih berubah-ubah )

**Alamat IP Elastis :**
- Berkaitan dengan akun AWS
- Dapat dialokasikan dan dipetakan ulang kapan saja
- Berbayar ( beli )

## Antarmuka Jaringan Elastis 
Antarmuka jaringan elastis adalah sebuah antarmuka jaringan virtual yang dapat Anda lampirkan atau lepaskan dari instans dalam VPC. Setiap instans dalam VPC Anda memiliki antarmuka jaringan default (antarmuka jaringan utama) yang ditetapkan alamat IPv4 pribadi dari rentang alamat IPv4 dari VPC Anda. Anda tidak dapat melepaskan antarmuka jaringan utama dari instans. Anda dapat membuat dan melampirkan antarmuka jaringan tambahan untuk setiap instans di VPC Anda. Jumlah antarmuka jaringan yang dapat Anda lampirkan bervariasi menurut tipe instans.

## Tabel rute dan rute 
Tabel ruteberisi sekumpulan aturan (disebutrute)yang mengarahkan lalu lintas jaringan dari subnet Anda. Setiap rute menentukan tujuandan target. Target adalah target yang dilalui lalu lintas tujuan.Secara default, setiap rute tabel yang Anda buat berisi rute lokal untuk komunikasi di VPC. Anda dapat menyesuaikan tabel rute dengan menambahkan rute.

# Jaringan VPC 
## Gateway Internet 
 Gateway Internet adalah komponen VPC yang dapat diskalakan, redundan, dan tersedia dengan sangat baik yang memungkinkan komunikasi antara instans di VPC dan internet Anda. Gateway internet memiliki dua tujuan: untuk memberikan target dalam tabel rute VPC Anda untuk lalu lintas yang dapat dirutekan internet, dan untuk melakukan penerjemahan alamat jaringan untuk instans yang telah ditetapkan alamat IPv4 publik

 ## NAT 
 Gateway Network Address Translation (NAT)  memungkinkan instans dalam subnet privat untuk terhubung ke internet atau layanan AWS lainnya. Untuk membuat gateway NAT, Anda harus menentukan subnet publik di mana gateway NAT seharusnya berada. Anda juga harus menentukan alamat IP Elastis untuk mengaitkannya dengan gateway NAT saat Anda membuatnya. Setelah Anda membuat gateway NAT, Anda harus memperbarui tabel rute yang terkait dengan satu atau lebih subnet privat Anda untuk mengarahkan lalu lintas yang terikat internet ke gateway NAT. Dengan demikian, instans di subnet privat Anda dapat berkomunikasi dengan internet.

 ## Berbagi VPC
 Berbagi VPC memungkinkan pelanggan berbagi subnet dengan akun AWS lainnya dalam organisasi yang sama di AWS Organizations.
 Berbagi VPC menawarkan beberapa manfaat:
 - Pemisahan tugas –Struktur VPC yang dikendalikan secara terpusat, perutean, alokasi alamat IP
 - Kepemilikan –Pemilik aplikasi terus memiliki sumber daya, akun, dan grup keamanan
 - Grup keamanan –peserta berbagi VPC dapat mereferensikan ID grup keamanan satu sama lain
 - Efisiensi –Kepadatan yang lebih tinggi di subnet, penggunaan VPN dan AWS Direct Connect
 - Tanpa batas langsung –Batas langusng dapat dihindari—misalnya, 50 antarmuka virtual per koneksi AWS Direct Connect melalui arsitektur jaringan yang disederhanakan.
 - Pengoptimalan biaya -Biaya dapat dioptimalkan melalui penggunaan kembali gateway NAT, endpoint antarmuka VPC, dan lalu lintas antar-Availability Zone.

## Peering VPC 
Koneksi peering VPC adalah koneksi jaringan antara dua VPC yang memungkinkan Anda mengarahkan lalu lintas antara kedua VPC menggunakan alamat IPv4 atau alamat IPv6 pribadi. Instans pada VPC manapun dapat berkomunikasi satu sama lain seolah-olah mereka ada di jaringan yang sama.

**Peering VPC memiliki beberapa batasan:**
- Rentang alamat IP tidak dapat tumpang tindih
- Peering transitif tidak didukung. Misalnya, Anda memiliki tiga VPC: A, B, dan C. VPC A terhubung ke VPC B, dan VPC A terhubung ke VPC C. Namun, VPC B tidakterhubung ke VPC C secara implisit. Untuk menghubungkan VPC B ke VPC C, Anda harus secara eksplisit menetapkan konektivitas tersebut.
- Anda hanya dapat memiliki satu sumber daya peering antara dua VPC yang sama.

## VPN AWS Site to Site 
Secara default, instans yang Anda luncurkan ke VPC tidak dapat berkomunikasi dengan jaringan jarak jauh. Untuk menghubungkan VPC Anda ke jaringan jarak jauh Anda (yaitu, membuat jaringan pribadi virtual atau koneksi VPN), lakukan :
- Buat perangkat gateway virtual baru (disebut gateway virtual private network (VPN)) dan lampirkan ke VPC Anda.
- Tentukan konfigurasi perangkat VPN atau customer gateway. Customer gateway bukan perangkat tetapi sumber daya AWS yang menyediakan informasi untuk AWS tentang perangkat VPN Anda.
- Membuat tabel rute kustom untuk mengarahkan lalu lintas yang terikat pusat data perusahaan ke gateway VPN. Anda juga harus memperbarui aturan grup keamanan. (Anda akan belajar tentang grup keamanan di bagian berikutnya.)
- Membangun koneksi AWS Site-to-Site VPN (Site-to-Site VPN) untuk menghubungkan dua sistem tersebut.
- Konfigurasikan perutean untuk melewati lalu lintas melalui koneksi.

## AWS Direct Connect 
AWS Direct Connect memungkinkan Anda membuat koneksi jaringan pribadi khusus antarjaringan dan salah satu lokasi DX Anda. Koneksi pribadi ini dapat mengurangi biaya jaringan, meningkatkan throughput bandwidth, dan memberikan pengalaman jaringan yang lebih konsisten dibandingkan dengan koneksi berbasis Internet.

## Endpoint VPC
Endpoint VPC adalah perangkat virtual. Komponen tersebut berskala horizontal, redundan, dan memiliki ketersediaan tinggi yang memungkinkan komunikasi antar instans di Amazon VPC dan layanan tanpa menimbulkan risiko ketersediaan atau batasan bandwidth pada lalu lintas jaringan. 

## AWS Transit Gateway 
Meskipun Anda dapat menggunakan peering VPC untuk menghubungkan pasangan VPC, mengelola konektivitas point-to-point di banyak VPC tanpa kemampuan untuk mengelola kebijakan konektivitas secara terpusat bisa jadi mahal dan sulit secara operasional. Untuk konektivitas on-premise, Anda harus melampirkan VPN ke setiap VPC individu. Pembangunan solusi ini dapat memakan waktu dan sulit dikelola ketika jumlah VPC tumbuh menjadi ratusan.Untuk mengatasi masalah ini, Anda dapat menggunakan AWS Transit Gateway untuk menyederhanakan model jaringan Anda. Dengan AWS Transit Gateway, Anda hanya perlu membuat dan mengelola satu koneksi dari gateway pusat ke setiap VPC, pusat data on-premise, atau kantor jarak jauh di seluruh jaringan Anda.

# Keamanan VPC 

## Security Group 
Grup keamanan mengontrol lalu lintas yang diizinkan untuk mencapai dan meninggalkan sumber daya yang terkait dengannya. Misalnya, setelah Anda mengaitkan grup keamanan dengan instans EC2, grup ini mengontrol lalu lintas masuk dan keluar untuk instans tersebut. Anda dapat mengaitkan grup keamanan hanya dengan sumber daya di VPC tempat ia dibuat. Grup keamanan memiliki aturanyang mengontrol lalu lintas masuk dan keluar.

##  ACL Jaringan 
 ACL memungkinkan atau menolak lalu lintas masuk atau keluar tertentu di tingkat subnet. Anda dapat menggunakan ACL jaringan default untuk VPC Anda, atau Anda dapat membuat ACL jaringan khusus untuk VPC Anda dengan aturan yang mirip dengan aturan untuk grup keamanan Anda untuk menambahkan lapisan keamanan tambahan ke VPC Anda. ACL jaringan memiliki aturan masuk dan keluar yang terpisah, dan setiap aturan dapat mengizinkan atau menolak lalu lintas. Secara otomatis, VPC Anda dilengkapi dengan ACL jaringan default yang dapat diubah. Secara default, VPC mengizinkan semua lalu lintas IPv4 masuk dan keluar dan, jika berlaku, lalu lintas IPv6. Tabel menunjukkan ACL jaringan default.

 ## Security Group Vs ACL Jaringan 
-  Grup keamanan bertindak pada tingkat instans, tetapi ACL jaringan bertindak pada tingkat subnet.
-  Grup keamanan hanya mendukung aturan izinkan, namun ACL jaringan mendukung aturan izinkan dan tolak.
-  Grup keamanan bersifat stateful, tetapi ACL jaringan adalah stateless.
-  Untuk grup keamanan, semua aturan dievaluasi sebelum keputusan dibuat untuk mengizinkan lalu lintas. Untuk ACL jaringan , aturan dievaluasi dalam urutan nomor sebelum keputusan dibuat untuk mengizinkan lalu lintas.

 # Amazon Route 53
 Amazon Route 53 adalah layanan web Sistem Nama Domain (DNS) dengan ketersediaan tinggi dan dapat diskalakan. Route 53 menghubungkan permintaan pengguna ke aplikasi internet yang berjalan di AWS atau on-premise. Amazon Route 53 juga menawarkan Registrasi Nama Domain—Anda dapat membeli dan mengelola nama domain (seperti example.com), dan Amazon Route 53 akan mengonfigurasi pengaturan DNS secara otomatis untuk domain Anda.

 Amazon Route 53 memungkinkan Anda meningkatkan ketersediaan aplikasi Anda yang berjalan di AWS dengan:
 - Mengonfigurasi skenario cadangan dan failover untuk aplikasi Anda sendiri.
 - Memungkinkan arsitektur multi-Wilayah yang sangat tersedia di AWS.
 - Membuat pemeriksaan kesehatan untuk memantau kesehatan dan kinerja aplikasi, server web, dan sumber daya lainnya. Setiap pemeriksaan kesehatan yang Anda buat dapat memantau salah satu hal berikut—kesehatan sumber daya tertentu, seperti server web; status pemeriksaan kesehatan lainnya; dan status alarm Amazon CloudWatch.

## Amazon CloudFront 
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/54ea09e1-cda1-4651-89a7-7e3ec48fb218)

Sebuah jaringan penyampaian konten (CDN) adalah sistem server pembuatan cache yang didistribusikan secara global. CDN menyimpan salinan file yang biasa diminta dalam cache (konten statis, seperti Hypertext Markup Language, atau HTML; Cascading Style Sheet, atau CSS; JavaScript; dan file gambar) yang di-host di server asal aplikasi. CDN memberikan salinan lokal dari konten yang diminta dari edge cache atau Point of Presence yang menyediakan pengiriman tercepat untuk pemohon. **Amazon CloudFront** adalah layanan jaringan pengiriman konten (CDN) yang dibuat untuk performa tinggi, keamanan, dan kenyamanan developer. 

Amazon CloudFront memberikan manfaat sebagai berikut:
- Cepat dan global-Amazon CloudFront diskalakan secara masif dan didistribusikan secara global. 
- Keamanan di edge–Amazon CloudFront menyediakan perlindungan tingkat jaringan dan tingkat aplikasi. 
- Dapat diprogram sepenuhnya–Fitur Amazon CloudFront dapat dikustomisasi untuk persyaratan aplikasi tertentu.
- Terintegrasi secara mendalam dengan AWS–Amazon CloudFront terintegrasi dengan AWS, dengan lokasi fisik yang terhubung langsung ke Infrastruktur Global AWS, serta layanan AWS lain
- Hemat biaya–Amazon CloudFront hemat biaya karena tidak memiliki komitmen minimum dan biaya Anda hanya untuk apa yang Anda pakai.

**Harga Amazon CloudFront**
Biaya Amazon CloudFront ditagih berdasarkan penggunaan layanan aktual di empat area:
- Transfer data keluar –Anda dikenakan biaya untuk volume data yang ditransfer keluar dari edge location Amazon CloudFront, diukur dalam GB, ke internet atau ke asal Anda (server asal AWS maupun server asal lainnya). Penggunaan transfer data Anda dijumlahkan secara terpisah untuk wilayah geografis tertentu, kemudian biayanya dihitung berdasarkan tingkat harga untuk setiap area.
- Permintaan HTTP(S) –Anda akan dikenakan biaya untuk jumlah permintaan HTTP(S) yang dibuat ke Amazon CloudFront untuk konten Anda.
- Permintaan pembatalan validasi –Anda dikenakan biaya per jalur dalam permintaan pembatalan validasi Anda. Jalur yang terdaftar dalam permintaan pembatalan validasi Anda merepresentasikan URL (atau beberapa URL jika jalur tersebut mengandung karakter pengganti) objek yang ingin Anda batalkan validasinya dari cache CloudFront. 
- Secure Sockets Layer (SSL) kustom IP khusus –Anda membayar 600 USD per bulan untuk setiap sertifikat SSL kustom yang terkait dengan satu atau lebih distribusi CloudFront yang menggunakan versi IP Khusus dari dukungan sertifikat SSL kustom. Biaya bulanan ini di-prorata berdasarkan jam.

# Hasil Knowledge
![image](https://github.com/silvyameliaperdani/100DaysOfCloud/assets/121029600/5df3e810-7ca8-4ccb-9dc1-977f55d1e1dd)




