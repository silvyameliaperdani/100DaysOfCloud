
# Day1 - Virtualisasi dan Basic Linux (mentor : Diana Zuniarti)

## Introduction
untuk pemula di bidang cloud dan sysadmin, kita perlu memahami apa itu virtualisasi dan basic linux. pada journey pertama saya ini, kita akan membahas 
beberapa hal sebagai berikut :
 1. Pengenalan Virtualisasi 
 2. Hirarki File Linux
 3. Perintah Dasar di Linux

## Cloud Research

 1. Virtualisasi, teknologi yang menciptakan versi virtual dari sesuatu, baik itu server, ruang penyimpanan dll.

-  Virtual Machine adalah sebuah perangkat lunak atau sistem operasi virtual yang bisa digunakan pada sebuah perangkat keras bersama dengan OS asli pada perangkat fisik. Dengan virtual machine kita dapat menjalankan aplikasi / program pada perangkat fisik secara virtual seperti halnya kita menggunakan perangkat yang berbeda. Atau lebih singkat nya kita membuat komputer virtual diatas komputer fisik. 
 
 ![image](https://user-images.githubusercontent.com/121029600/210696499-d0971bcf-ae95-4ac3-b985-28674bcd43c0.png)
 
foto : diambil dari video Aguna Course - Virtual Machine Fundamental 
 
- Arsitektur Virtual Machine

![image](https://user-images.githubusercontent.com/121029600/210697466-a2f99d2b-7af1-42cc-ac26-c87ad3b276b1.png)

foto : diambil dari video Aguna Course - Virtual Machine Fundamental 

Contoh Hypervisor Bare-Mental Architecture: proxmox, vmware ESXi

Contoh Hypervisor Hosted Architecture : vmware, VirtualBox

2. Hirarki File Linux 
  Berikut struktur dari Direktori yang ada di Linux 
  
![image](https://user-images.githubusercontent.com/121029600/210698914-618b3e8b-b3bb-4c86-a9a4-75b87894ad0d.png)

/root : direktori paling tertinggi, atas direktori sistem pokok

/bin  : berisi file executable untuk digunakan oleh sistem 

/boot : berisi file untuk keperluan booting sistem operasi

/dev  : berisi file-file device

/etc  : tempat menyimpan konfigurasi

/home : untuk menyimpan file-file milik user

/lib  : berisi file library

/mnt  : digunakan untuk memount file temporary

/proc : berisi file-file yang mempunyai informasi tentang proses yang sedang dijalankan oleh sistem operasi

/sbin : sama saja dengan /bin, hanya saja yang disimpan adalah file-file binary

/tmp  : berisi file-file temporary yang digunakan selama sistem operasi berjalan

/usr  : direktori ini bisa digunakan oleh seluruh user untuk berbagai kepentingan, seperti 
sharing folder 

/var  : berisi file-file variable, seperti file mail,log dll.

3. Perintah - Perintah Dasar di Linux 
- cd = perintah untuk masuk ke direktori yang diinginkan
- cp = perintah untuk mengcopy file/direktori
- mv = perintah untuk memindahkan file dan juga bisa untuk rename file 
- touch = perintah untuk membuat file
- rm = perintah untuk menghapus file 
- mkdir = perintah untuk membuat direktori
- cp -r = perintah untuk mengcopy direktori beserta isinya 
- rmdir = perintah untuk menghapus direktori kosong 
- clear = perintah untuk menghapus tampilan yang ada di layar 
- history = perintah untuk melihat command apa saja yang telah kita jalankan 
- nano = perintah untuk mengedit file 
- ls  = melihat isi direktori 
- pwd = untuk menunjukkan posisi kita sekarang 
- echo ".." >> untuk menambahkan kalimat pada file 
- echo ".." > untuk mereplace isi file dan digantikan dengan kalimat yang ada di perintah  

## Social Proof


[Twitter](https://twitter.com/silvyameliaa_/status/1611179173036560385)
