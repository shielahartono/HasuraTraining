# Penjelasan Terkait Mekanisme Kerberos, apa itu Thin dan Thick Client



## Apa itu Kerberos ?

Kerberos adalah protokol autentikasi jaringan yang dirancang untuk menyediakan komunikasi yang aman di lingkungan yang tidak aman. Kerberos menggunakan enkripsi untuk memastikan bahwa identitas pengguna atau layanan diverifikasi dengan aman sebelum mengizinkan akses ke sumber daya jaringan.


Kerberos menggunakan berbagai jenis algoritma enkripsi untuk memastikan keamanan autentikasi dan komunikasi antara klien, server, dan KDC (Key Distribution Center). Jenis enkripsi yang digunakan bergantung pada implementasi dan versi Kerberos. Secara umum, berikut adalah jenis enkripsi yang digunakan dalam Kerberos:


  1. Enkripsi Simetris (Symmetric Encryption)

       A. Data Encryption Standard (DES)

       B. Triple DES (3 DES)

       C. Advanced Encryption Standard (AES)

  3. Enkripsi untuk Integritas Data

  4. Enkripsi Session Key



## Bagaimana cara kerja Kerberos ?

Berikut adalah ilustrasi proses 

  1. Autentikasi Awal (AS Exchange):

      Klien → KDC-AS: Permintaan autentikasi.
     
      KDC-AS → Klien: Mengirimkan TGT dan Session Key.

2. Permintaan Tiket Layanan (TGS Exchange):

      Klien → KDC-TGS: TGT + Permintaan akses ke layanan.
   
      KDC-TGS → Klien: Tiket layanan + Session Key.

   
3. Akses ke Layanan (Client/Server Exchange):
     Klien → Server: Tiket layanan.
   
     Server → Klien: Konfirmasi autentikasi dan layanan tersedia.


# Apa itu Thin Client ?

  Thin client adalah klien yang memiliki sedikit kemampuan pemrosesan atau penyimpanan lokal dan sangat bergantung pada server untuk menjalankan sebagian besar tugas.

Ciri-ciri Thin Client pada Kerberos:


1. Minimal Pemrosesan Lokal:
   
Thin client hanya berfungsi untuk mengirim permintaan autentikasi ke Key Distribution Center (KDC) dan menerima tiket tanpa banyak pemrosesan lokal.


2. Ketergantungan Tinggi pada Server:

Semua logika autentikasi dan pengelolaan sesi dilakukan di sisi server.

3. Keamanan Lebih Terkendali:
   
Karena klien tidak menyimpan banyak data sensitif, risiko kompromi data di perangkat lebih rendah.

4. Contoh Implementasi:

Perangkat atau aplikasi yang hanya bertugas mengarahkan permintaan autentikasi, seperti terminal akses jarak jauh yang bergantung sepenuhnya pada server.


## Kelebihan Thin Client:

  1.Biaya rendah untuk perangkat keras karena sedikit kebutuhan pemrosesan lokal.

  2.Keamanan lebih baik karena tidak banyak data sensitif disimpan di klien.


## Kekurangan Thin Client:
  
  1. Kinerja sangat tergantung pada konektivitas jaringan dan server.

  2. Tidak cocok untuk operasi yang membutuhkan pemrosesan lokal atau offline.


   



