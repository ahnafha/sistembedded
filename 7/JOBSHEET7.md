### JUDUL : TRANSMISI DATA MENGGUNAKAN HYPER TEXT TRANSFER PROTOCOL (HTTP)
### TUJUAN
1) Mahasiswa dapat memahami alur kerja, kegunaan dan manfaat protokol
HTTP.
2) Mahasiswa dapat memahami dan mengimplementasikan protokol HTTP
pada sistem IoT untuk monitoring dan kendali.
### ALAT DAN BAHAN
1) Komputer terpasang Node Red
2) Postman
### TEORI SINGKAT
Hypertext Transfer Protocol (HTTP) adalah sebuah protokol jaringan lapisan
aplikasi yang digunakan untuk sistem informasi terdistribusi, kolaboratif, dan
menggunakan hipermedia. Penggunaannya banyak pada pengambilan sumber
daya yang saling terhubung dengan tautan, yang disebut dengan dokumen
hiperteks, yang kemudian membentuk World Wide Web pada tahun 1990 oleh
fisikawan Inggris, Tim Berners-Lee. Hingga kini, ada dua versi mayor dari
protokol HTTP, yakni HTTP/1.0 yang menggunakan koneksi terpisah untuk
setiap dokumen, dan HTTP/1.1 yang dapat menggunakan koneksi yang sama
untuk melakukan transaksi. Dengan demikian, HTTP/1.1 bisa lebih cepat karena
memang tidak usah membuang waktu untuk pembuatan koneksi berulang-ulang.

Pengembangan standar HTTP telah dilaksanakan oleh Konsorsium World
Wide Web (World Wide Web Consortium/W3C) dan juga Internet Engineering
Task Force (IETF), yang berujung pada publikasi beberapa dokumen Request for
Comments (RFC), dan yang paling banyak dirujuk adalah RFC 2616 (yang
dipublikasikan pada bulan Juni 1999), yang mendefinisikan HTTP/1.1.

HTTP adalah sebuah protokol meminta/menjawab antara klien dan server.
Sebuah klien HTTP (seperti web browser atau robot dan lain sebagainya),
biasanya memulai permintaan dengan membuat hubungan ke port tertentu di
sebuah server Webhosting tertentu (biasanya port 80). Klien yang mengirimkan
permintaan HTTP juga dikenal dengan user agent. Server yang meresponsnya,
yang menyimpan sumber daya seperti berkas HTML dan gambar, dikenal juga
sebagai origin server. Di antara user agent dan juga origin server, bisa saja ada
penghubung, seperti halnya proxy, gateway, dan juga tunnel.

HTTP tidaklah terbatas untuk penggunaan dengan TCP/IP, meskipun HTTP
merupakan salah satu protokol aplikasi TCP/IP paling populer melalui Internet.
Memang HTTP dapat diimplementasikan di atas protokol yang lain di atas
Internet atau di atas jaringan lainnya. seperti disebutkan dalam “implemented on
top of any other protocol on the Internet, or on other networks.”, tapi HTTP
membutuhkan sebuah protokol lapisan transport yang dapat diandalkan. Protokol
lainnya yang menyediakan layanan dan jaminan seperti itu juga dapat digunakan.
### LANGKAH PERCOBAAN
A. Instalasi SQL Server (MySQL)

1.Buka Terminal Ubuntu.

2.Kemudian install mysql-server menggunakan perintah berikut.
   
   ![7A(2)Kemudian install mysql-server menggunakan perintah berikut](https://github.com/ahnafha/sistembedded/assets/154432108/a3c4483a-c9f7-4e80-b30f-c8303c5ff048)

3.Tunggu proses instalasi sampai selesai. Kemudian gunakan perintah berikut
untuk memastikan mysql telah terpasang dan aktif berjalan.

![7A(3)Tunggu proses instalasi sampai selesai  Kemudian gunakan perintah berikut](https://github.com/ahnafha/sistembedded/assets/154432108/4579611d-0a60-421f-83c0-c72459976729)

4.Langkah selanjutnya adalah melakukan instalasi keamanan untuk database
yang akan digunakan (set username dan password, dll).

![7A(4)Langkah selanjutnya adalah melakukan instalasi keamanan untuk database](https://github.com/ahnafha/sistembedded/assets/154432108/000a21d5-57ba-427a-afdc-4257e267798d)

5.Kemudian setelah selesai instalasi, lakukan pengaturan username dan
password untuk user root di localhost seperti pada Gambar 6.1.
![7A(5)lakukan pengaturan username ](https://github.com/ahnafha/sistembedded/assets/154432108/290548d4-eb0a-4af6-b502-81ab1bf4040e)

6.Setelah itu ketik perintah exit untuk keluar dari mysql shell. Kemudian login
menggunakan user root dan password yang telah dibuat sebelumnya.

![7A(6)Setelah itu ketik perintah exit untuk keluar dari mysql shell  Kemudian login](https://github.com/ahnafha/sistembedded/assets/154432108/5f8ea2dc-08a0-4ee9-b2dd-e163d41b07b6)

7.Buat database menggunakan perintah berikut.

![7A(7)](https://github.com/ahnafha/sistembedded/assets/154432108/dc8a985d-e234-463e-baf0-01f847baa171)


8.Lakukan pemeriksaan pada daftar database untuk memastikan bahwa
database yang telah dibuat sudah berhasil terbentuk menggunakan perintah
pada baris pertama. Kemudian pilih data database yang telah kita buat seperti
pada script perintah barus kedua berikut.
![7A(8)Lakukan pemeriksaan pada daftar database](https://github.com/ahnafha/sistembedded/assets/154432108/7b253bac-0178-4016-8e79-b81183cf814a)

9.Buat tabel menggunakan perintah seperti pada Gambar 6.2. (nama dan row
tabel menyesuaikan project masing-masing).

![7A(9)Buat tabel menggunakan perintah seperti pada Gambar 6 2  (nama dan row](https://github.com/ahnafha/sistembedded/assets/154432108/fd3943d6-9f5a-4fd3-b2c1-b352a05e0945)

Basic Flow Transmisi Data Menggunakan Protokol HTTP
1. Install Postman pada Komputer Windows, kemudian lakukan pendaftaran
akun.
2. Buatlah flow program seperti pada Gambar 6.3. Gunakan HTTP In node dan
Debug Node.
Gambar 6.3. Basic flow transmisi data menggunakan protokol HTTP
3. Konfigurasi Input Dummy node seperti Gambar 6.4.
Gambar 6.4. Konfigurasi pada Input Dummy Node
4. Deploy flow program, kemudian masuk ke Postman. Konfigurasi Postman
seperti pada Gambar 6.5A untuk mengirim data String dengan format
encoded utf-8 dan Gambar 6.5B untuk mengirim data dalam format JSON.
Klik Send untuk mengirim data. (Isian pada Body sama, Header berbeda).
5. Langkah selanjutnya, dokumentasikan hasil keluaran dari flow program.

![7B(1-5)](https://github.com/ahnafha/sistembedded/assets/154432108/e5077734-5c45-485c-bc6a-99a30c86b4ad)

6. Setelah itu, buatlah flow program seperti Gambar 6.6 untuk melakukan
parsing data JSON.
Gambar 6.6. Flow program untuk parsing data JSON
7. Kemudian konfigurasi Function/Validation node seperti pada Gambar 6.7.
Ubah obj.variabel_datamu pada setiap node, sesuai dengan project masingmasing.
Gambar 6.7. Konfigurasi pada Validation node
8. Deploy program dan dokumentasikan hasil keluarannya.

![7B(6-8)](https://github.com/ahnafha/sistembedded/assets/154432108/a2fdf79c-d8f3-405e-a92e-1c660f3db9ed)

10. Buatlah flow program seperti pada Gambar 6.8 untuk simulasi transmisi data
pada protokol HTTP dengan respons (acknowledgement/ack).
Gambar 6.8. Flow program transmisi data pada protokol HTTP dengan respons
11. Konfigurasi Validation node seperti Gambar 6.9.
Gambar 6.9. Konfigurasi pada Validation node
12. Kemudian, konfigurasi Router Node seperti Gambar 6.10.
Gambar 6.10. Konfigurasi pada Router node
13. Setelah itu, konfigurasi HTTP Response (Resp Ok dan Resp Bad) node
seperti Gambar 6.11.
Gambar 6.11. Konfigurasi pada HTTP Response node
14. Kemudian kirimkan data JSON menggunakan Postman seperti pada pada
Gambar 6.12 dan Gambar 6.13. Shape bertanda merah merupakan response
dari server ketika data berhasil terkirim dan gagal terkirim.
Gambar 6.12. Konfigurasi pada Postman dan response data berhasil terkirim
Gambar 6.13. Konfigurasi pada Postman dan response data gagal terkirim
15. Setelah itu,dokumentasikan hasilnya.
    
status=1 (data berhasil terkirim)
![7B(9-14)status=1](https://github.com/ahnafha/sistembedded/assets/154432108/63cef779-f28e-4d06-aede-70844305d06c)
status=0 (data gagal terkirim)
![7B(9-14)status=0](https://github.com/ahnafha/sistembedded/assets/154432108/2c75f845-6db6-4f5a-998f-f1810e763e44)
