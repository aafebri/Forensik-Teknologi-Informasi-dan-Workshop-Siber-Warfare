# Rangkuman Lengkap Network Protocol

## Pengertian Network Protocol

*Network Protocol* adalah seperangkat aturan yang mengatur bagaimana data dikirim, diterima, dan diproses di dalam jaringan komputer. Protokol ini memastikan perangkat keras dan lunak dari produsen yang berbeda bisa berkomunikasi satu sama lain dengan standar yang sama.

## Model Lapisan Jaringan (Network Layers)

Untuk memahami cara kerja protokol, penting untuk memahami model lapisan (layer) jaringan. Dua model yang paling umum adalah *TCP/IP Model* dan *OSI Model*.

### 1. TCP/IP Model

Model TCP/IP (Transmission Control Protocol/Internet Protocol) adalah model standar yang digunakan saat ini. Model ini terdiri dari 4 lapisan:

* *Application Layer:* Lapisan teratas yang berinteraksi langsung dengan aplikasi pengguna.
    * *Contoh Protokol:* HTTP, FTP, SMTP, DNS, dan Telnet.
* *Transport Layer:* Bertanggung jawab untuk pengiriman data dari satu proses ke proses lain.
    * *Protokol Utama:* TCP (Transmission Control Protocol) untuk pengiriman yang andal, dan UDP (User Datagram Protocol) untuk pengiriman yang cepat.
* *Internet Layer:* Mengurus pengalamatan (IP Addressing) dan routing paket data.
    * *Protokol Utama:* IP (Internet Protocol).
* *Network Access Layer:* Lapisan terbawah yang menangani media fisik dan komunikasi data di dalam jaringan lokal.
    * *Contoh Protokol:* Ethernet (kabel) dan Wi-Fi (nirkabel).

Berikut adalah gambaran visual dari TCP/IP Model:

![TCP/IP Model](https://i.imgur.com/uR29w2M.png)

### 2. OSI Model

Model OSI (Open Systems Interconnection) adalah model konseptual yang lebih rinci, terdiri dari 7 lapisan. Meskipun tidak banyak digunakan dalam implementasi praktis seperti TCP/IP, model ini sangat penting untuk pendidikan dan pemahaman arsitektur jaringan.

* *Lapisan 7: Application*
* *Lapisan 6: Presentation*
* *Lapisan 5: Session*
* *Lapisan 4: Transport*
* *Lapisan 3: Network*
* *Lapisan 2: Data Link*
* *Lapisan 1: Physical*

Berikut adalah perbandingan visual antara OSI Model dan TCP/IP Model:

![OSI vs TCP/IP Model](https://i.imgur.com/gK1q2yY.png)

### Perbedaan TCP dan UDP

TCP dan UDP adalah dua protokol utama di lapisan Transport. Memahami perbedaannya sangat penting:

| Karakteristik    | TCP (Transmission Control Protocol)            | UDP (User Datagram Protocol)                       |
| ---------------- | ---------------------------------------------- | -------------------------------------------------- |
| *Keandalan* | *Reliable* (ada konfirmasi pengiriman)       | *Unreliable* (tanpa konfirmasi)                    |
| *Kecepatan* | Lebih lambat (overhead tinggi)                 | Lebih cepat (overhead rendah)                      |
| *Penggunaan* | Transfer file, email, browsing web (HTTP/S)    | Streaming video, game online, panggilan VoIP        |

Ini adalah rangkuman yang ringkas namun lengkap untuk tugas Anda. Selamat mengerjakan!  
