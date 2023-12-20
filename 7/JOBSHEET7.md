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
