# Cloud Computing Part 4 [ Pemateri : Tiara Dwi Maulita Sari ]

## Introduction
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
Jaringan komputer mengacu pada perangkat komputasi yang saling terhubung serta dapat bertukar data dan berbagi sumber daya satu sama lain. Perangkat jaringan ini menggunakan sistem aturan, yang disebut sebagai protokol komunikasi, untuk mentransmisikan informasi melalui teknologi fisik atau nirkabel.

## Alamat IP 
Setiap mesin client dalam jaringan memiliki alamat IP yang unik. Alamat IP adalah label numerik dalam format desimal. 

## Alamat IPv4 dan IPv6 
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

