JUDUL : DASAR PEMROGRAMAN ESP32 UNTUK
PEMROSESAN DATA INPUT/OUTPUT ANALOG
DAN DIGITAL

TUJUAN
1) Mahasiswa dapat memahami dan mengoperasikan GPIO pada ESP32.
2) Mahasiswa dapat memahami dan melakukan pengolahan data untuk
input/output analog dan digital.
3) Mahasiswa dapat melakukan optimalisasi pembacaan sensor analog
menggunakan metode regresi linear.
ALAT DAN BAHAN
1) ESP32
2) Breadboard
3) Kabel jumper
4) Potensiometer 10k Ohm (1)
5) Sensor Capacitive Soil Moisture
6) LED (5) dan Push Button (3)
7) Multimeter
8) Resistor 330,1K, 10K Ohm (@ 3)
   
TEORI SINGKAT
ESP-32 adalah mikrokontroler yang dikenalkan oleh Espressif System
merupakan penerus dari mikrokontroler ESP8266. Pada mikrokontroler ini sudah
tersedia modul WiFi dalam chip sehingga sangat mendukung untuk membuat
sistem aplikasi Internet of Things. Perbedaan antara ESP32 dengan ESP8266
adalah pada bagian prosesornya. ESP32 sudah Dual-Core 32 bit, jelas lebih cepat
ESP32 secara kinerja. Selain itu modul ini juga mempunyai bluetooth, satu fitur
yang tidak ada di ESP8266.
Gambar 5.1 merupakan susuan pin pada modul ESP32. Pada pin out tersebut
terdiri dari :
• 18 ADC (Analog Digital Converter)
• 2 DAC (Digital Analog Converter)
• 16 PWM (Pulse Width Modulation)
• 10 Sensor sentuh
• 2 jalur antarmuka UART
• pin antarmuka I2C, I2S, dan SPI
Gambar 5.1 Pinout ESP32

5.1 Pulse Wide Modulation (PWM)
Pin analog pada ESP32 (dan mikrokontroller lain pada umumnya) dapat
digunakan sebagai input dan output digital. Hanya saja pin analog memiliki fitur
untuk dapat mengubah sinyal analog yang masuk menjadi nilai digital yang
mudah diukur. Pin digital hanya dapat mengenali sinyal 0 volt sebagai nilai LOW
dan 3,3 volt sebagai nilai HIGH. Sedangkan pin analog dapat mengenali sinyal
pada rentang nilai voltase tersebut.

Pin analog terhubung dengan converter pada mikrokontroller yang dikenal
dengan istilah analog-to-digital converter (disingkat ADC atau A/D). Converter
ini mengubah nilai analog berbentuk sinyal voltase ke dalam bentuk digital/angka
supaya nilai analog ini dapat digunakan dengan lebih mudah dan aplikatif. ESP32
didukung perangkat keras yang mampu membaca input channel ADC hingga
resolusi 12 bit. Hal tersebut berarti bahwa ESP32 mampu mendapatkan
pembacaan analog mulai dari 0 hingga 4095, di mana 0 sesuai dengan 0V dan
4095 hingga 3.3V. Resolusi channel ADC tersebut dapat dikonversi juga menjadi
lebih kecil menggunakan kode dan rentang ADC pada program.

Analog output pada microkontroller dihasilkan oleh teknik yang dikenal
dengan istilah PWM atau Pulse Width Modulation. PWM memanipulasi keluaran
digital sedemikian rupa sehingga menghasilkan sinyal analog. Metode PWM
menggunakan pendekatan perubahan lebar pulsa untuk menghasilkan nilai
tegangan analog yang diinginkan. Pin yang difungsikan sebagai PWM analog
output akan mengeluarkan sinyal pulsa digital dengan frekuensi 5000 Hz yang
mana nilai tegangan analog diperoleh dengan mengubah duty cycle atau
perbandingan lamanya pulsa HIGH terhadap periode (T) dari sinyal digital
tersebut. Mikrokontroler melakukan pengaturan output digital ke HIGH dan LOW
bergantian dengan porsi waktu tertentu untuk setiap nilai keluarannya. Durasi
waktu untuk nilai HIGH disebut pulse width atau panjang pulsa. Hal tersebut
dapat dilihat pada Gambar 5.2.
Gambar 5.2. Duty cycle pada PWM
Sumber : www.arduino.cc

Kondisi HIGH adalah kondisi ketika sinyal berada di atas grafik (3,3V) dan
LOW adalah ketika sinyal berada di bawah (0V). Duty cycle adalah persentasi
panjang pulsa HIGH dalam satu periode sinyal. Ketika duty cycle 0% atau sinyal
LOW penuh, maka nilai analog yang dikeluarkan adalah 0V atau setara dengan
GND. Jika pulsa HIGH muncul selama setengah dari periode sinyal, maka duty
cycle yang dihasilkan adalah 50% yang berarti sinyal analog yang dihasilkan
sebesar setengah dari tegangan analog maksimal yaitu 1/2 dari 3,3 V atau sama
dengan 1,65 V. Ketika duty cycle 100% atau sinyal penuh maka sinyal yang
dikeluarkan adalah 3.3V.

5.2 Regresi Linear
Regresi analisis adalah teknik statistika untuk menginvestigasi dan
memodelkan hubungan antara variabel dari data statistik sebelumnya.
Pengaplikasian regresi cukup banyak dan terjadi hampir di banyak bidang seperti
bidang keteknikan, ilmu fisika dan kimia, ekonomi, manajemen, ilmu biologi dan
ilmu sosial. Bahkan analisis regresi mungkin lebih banyak digunakan dalam
teknik statistik.

Regresi dapat dibedakan menjadi tiga jenis, yaitu regresi linier, regresi multi
linier dan regresi tak linier. Di dalam model regresi linier terdapat dua jenis
variabel yaitu variabel bebas atau input tegangan (X) dan variabel tak bebas atau
output sensor (Y). Dalam bentuk yang paling sederhana, regresi linier
direpresentasikan pada persamaan (5.1).
𝑌 = 𝐴 + 𝐵𝑥 (5.1)
Di mana 𝐴 disebut sebagai sumbu awal dan 𝐵 adalah koefisien arah atau
koefisien beta.

LANGKAH PERCOBAAN
A. Instalasi Board ESP32 pada Arduino IDE

1. Buka Arduino IDE
2. Kemudian klik Menu File > Preferences
3. Pada kolom Additional ... yang ada dibawah, tambahkan link berikut
https://dl.espressif.com/dl/package_esp32_index.json
4. Klik menu Tools > Board: > Pilih Boards Manager ...
5. Pada kolom pencarian tulis ESP32 kemudian install dan tunggu sampai
selesai.
B. Mengakses GPIO dan PWM ESP32
a) GPIO
1. Buatlah rangkaian seperti pada Gambar di bawah ini.
2. Buka program example blink, kemudian modifikasi dan buat agar LED dapat
melakukan blink dengan interval 100ms, 1 detik, 2 detik dan 3 detik sekali.
Setelah itu, buatlah program agar LED dapat blink 1 detik sekali
menggunakan timer milis(). Dokumentasikan hasilnya.
3. Buatlah program seperti pada script di bawah ini untuk mengendalikan led
menggunakan push button. Kemudian upload program tersebut pada ESP32
dan dokumentasikan hasilnya.
