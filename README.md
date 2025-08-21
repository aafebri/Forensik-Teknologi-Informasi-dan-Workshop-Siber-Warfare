# 📡 Network Protocol - Dokumentasi Lengkap

Repositori ini berisi dokumentasi lengkap tentang **Network Protocol**, arsitektur komunikasi jaringan, serta penjelasan detail dari hardware, OS, proses komunikasi, OSI layer, TCP/IP, hingga penggunaan Wireshark untuk analisis jaringan.  

---

## 1. 🌐 Network Protocol
**Network Protocol** adalah seperangkat aturan yang mengatur bagaimana data dikirim, diterima, dan diproses di dalam jaringan komputer.  
Contoh: **TCP/IP, HTTP, FTP, DNS, DHCP, SMTP, POP3, IMAP**.  

Protokol ini memastikan perangkat yang berbeda bisa berkomunikasi dengan standar yang sama.
![OSI vs TCP/IP](data:image/png;base64,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)

---

## 2. ⚙️ Hardware, Kernel, OS, Apps, User, CPU, Process
- **Hardware** → Perangkat fisik (CPU, RAM, NIC, router, switch).
- **Kernel** → Bagian inti OS, menghubungkan hardware dengan software.
- **OS (Operating System)** → Sistem pengatur komputer (Linux, Windows, macOS).
- **Apps** → Aplikasi yang digunakan user (browser, WhatsApp, game, dll).
- **User** → Orang yang menggunakan sistem.
- **CPU - Process** → CPU mengeksekusi instruksi aplikasi dalam bentuk proses.

![OSI vs TCP/IP](images/gambar2.png)
---

## 3. 🚀 Aplikasi, Proses, dan Komunikasi
- **Apps yang sedang dieksekusi** → Menjadi **process** di CPU.
- **Komunikasi antar process** → Bisa melalui **Inter-Process Communication (IPC)**.
- **Remote Procedure Call (RPC)** → Memungkinkan satu program memanggil fungsi di komputer lain.
- **Network TCP/IP** → Digunakan untuk komunikasi data antar komputer.
![OSI vs TCP/IP](images/gambar3.png)
---

## 4. 📑 ISO-OSI Model
Model **OSI (Open Systems Interconnection)** memiliki **7 layer**:

1. **Physical** → Transmisi bit (kabel, fiber, sinyal).
2. **Data Link** → Pengalamatan fisik (MAC Address, Ethernet).
3. **Network** → Routing & IP Address.
4. **Transport** → Segmentasi data (TCP/UDP).
5. **Session** → Mengatur koneksi antar aplikasi.
6. **Presentation** → Enkripsi, kompresi, format data.
7. **Application** → Layanan aplikasi (HTTP, FTP, DNS).
![OSI vs TCP/IP](images/gambar4.png)
---

## 5. 🌍 Internet & Alur Kerjanya
Alur sederhana Internet:
1. User membuka aplikasi (misalnya browser).
2. Aplikasi membuat permintaan ke server (HTTP/HTTPS).
3. DNS menerjemahkan domain → IP Address.
4. Data dikirim via TCP/IP melewati router, switch, kabel, dll.
5. Server merespon → data kembali ke user.
![OSI vs TCP/IP](images/gambar5.png)
---

## 6. 📦 Aturan TCP/IP
- **TCP (Transmission Control Protocol)** → Handshake, reliabilitas, segmentasi data.
- **IP (Internet Protocol)** → Pengalamatan & routing.
- Kombinasi ini membentuk **Internet Protocol Suite**.
![OSI vs TCP/IP](images/gambar6.png)
---

## 7. 👥 Client dan User dalam OSI Layer
- **Application** → HTTP, FTP, DNS.
- **Presentation** → SSL/TLS, enkripsi.
- **Session** → Socket, sesi komunikasi.
- **Transport** → TCP/UDP.
- **Network** → IP.
- **Data Link** → Ethernet, MAC.
- **Physical** → Kabel, wireless.
![OSI vs TCP/IP](images/gambar7.png)

---

## 8. 📡 Media Komunikasi & Pensinyalan
1. **Cable (UTP/STP)** → Murah, mudah dipasang.
2. **Fiber Optic** → Cepat, tahan interferensi.
3. **Radio Frequency (Wireless/Wi-Fi)** → Praktis, tapi rawan gangguan.
![OSI vs TCP/IP](images/gambar8.gif)
---

## 9. 🔍 Wireshark & Testing
**Wireshark** adalah tool untuk menganalisis paket data jaringan.  

### Cara kerja:
1. Menangkap paket (capture) dari interface jaringan.
2. Menampilkan detail tiap paket (src IP, dst IP, protokol, payload).
3. Memungkinkan filter untuk analisis spesifik (contoh: hanya DNS atau HTTP).

### Contoh Capture DNS:
- Gunakan file trace seperti `dns-imp-pacing.gz`.
- Buka di Wireshark → gunakan filter:
- Akan terlihat request & response DNS (domain → IP).
![OSI vs TCP/IP](images/gambar9.png)
---


## 10. 📊 Diagram OSI vs TCP/IP
![OSI vs TCP/IP](images/osi_vs_tcpip.png)

## 11. 🌍 Alur Kerja Internet (HTTP/HTTPS)
![Internet Flow](images/internet_flow.png)

## 📌 Kesimpulan
- **Network Protocol** = aturan komunikasi antar perangkat.  
- **OSI & TCP/IP** = model komunikasi data.  
- **Wireshark** = alat analisis paket.  
- **Media komunikasi** → kabel, fiber, radio.  
- Semua ini bekerja bersama agar Internet bisa berjalan sebagaimana mestinya.  

---

✍️ Dibuat Oleh : Marthen Frikaldo Antaribaba

Untuk dokumentasi belajar & riset..  
