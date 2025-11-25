#  Laporan Hasil Scan Nmap – Metasploitable 2

Repository ini berisi dokumentasi hasil scanning Nmap pada host 192.168.100.10.

---

##  Screenshot Hasil Scan

###  Screenshot 1
<img src="gambar 1.png" width="800">

---

###  Screenshot 2
<img src="gambar 2.png" width="800">

---

###  Screenshot 3
<img src="gambar 3.png" width="800">

---


---

#  Command Nmap


---

#  Tabel Hasil Scan Port

| Port | Status | Deskripsi |
|------|--------|-----------|
| 21 | open | FTP – vsftpd 2.3.4<br>• ftp-anon: Anonymous login allowed (FTP code 230)<br>• FTP server status: Connected to 192.168.100.10 |
| 22 | open | SSH – OpenSSH 4.7p1 Debian 8ubuntu1 (protocol 2.0)<br>Fingerprint RSA & DSA terdeteksi |
| 23 | open | Telnet – Linux telnetd |
| 25 | open | SMTP – Postfix smtpd<br>• Mendukung PIPELINING, SIZE, VRFY, ETRN<br>• Cert CommonName: ubuntu804-base.localdomain |
| 53 | open | DNS – ISC Bind 9.4.2 |
| 80 | open | HTTP – Apache httpd 2.2.8 (Ubuntu) DAV/2<br>• Title: Metasploitable2 – Linux |
| 111 | open | rpcbind – RPC #100000 |
| 139 | open | SMB – Samba 3.0.20-Debian (WORKGROUP) |
| 445 | open | SMB – Samba 3.0.20-Debian<br>• Vuln NetBIOS<br>• SMB security mode: user-level<br>• Signing disabled |
| 512 | open | exec – BSD rexec |
| 513 | open | login – BSD rlogin |
| 514 | open | shell – BSD rsh |
| 1099 | open | Java RMI – GNU Classpath girmiregistry |
| 2049 | open | NFS – rpc.nfsd |
| 2121 | open | ProFTPD 1.3.1 |
| 3306 | open | MySQL 5.0.51a-3ubuntu5<br>• Default credentials: root (blank) |
| 3632 | open | distccd v1 (GNU) — sering dieksploitasi |
| 5432 | open | PostgreSQL 8.3.x |
| 5900 | open | VNC – protocol 3.3 |
| 6000 | open | X11 (access denied) |
| 6667 | open | UnrealIRCd – IRC (rentan terhadap backdoor) |
| 7001 | open | Apache JServ (Protocol v1.3) |
| 8009 | open | Apache Tomcat AJP13 |
| 8180 | open | Apache Tomcat/Coyote JSP Engine 1.1 |

---

#  Penjelasan Lengkap Hasil Scan Nmap

Di bawah ini adalah penjelasan lengkap untuk setiap port dan layanan yang ditemukan pada host **192.168.100.10** menggunakan Nmap.

---

##  Port 21 – FTP (vsftpd 2.3.4)
Layanan FTP berjalan menggunakan **vsftpd 2.3.4**.  
Ditemukan bahwa server mengizinkan **anonymous login**, yang merupakan risiko keamanan tinggi.  
Versi ini juga diketahui memiliki *backdoor vulnerability* yang memungkinkan penyerang mendapatkan akses sistem.

---

##  Port 22 – SSH (OpenSSH 4.7p1 Debian 8ubuntu1)
SSH aktif dengan versi yang cukup lama.  
Fingerprint RSA dan DSA terdeteksi, menunjukkan penggunaan algoritma lama yang kurang aman.  
Versi ini rentan terhadap beberapa CVE eksploitasi autentikasi.

---

##  Port 23 – Telnet
Telnet berjalan tanpa enkripsi sehingga semua data termasuk username dan password dapat disadap.  
Layanan ini sangat tidak aman dan tidak boleh digunakan pada sistem produksi.

---

##  Port 25 – SMTP (Postfix smtpd)
SMTP memungkinkan email relay.  
Server mendukung fitur seperti:
- VRFY → untuk enumerasi user
- ETRN → memungkinkan serangan mail relay

Terdapat sertifikat internal: `ubuntu804-base.localdomain`.

---

##  Port 53 – DNS (ISC Bind 9.4.2)
DNS server menggunakan Bind 9.4.2.  
Versi ini memiliki banyak kelemahan historis seperti:
- DNS cache poisoning
- Remote DoS vulnerability

---

##  Port 80 – HTTP (Apache 2.2.8)
Layanan web menggunakan Apache 2.2.8.  
Teridentifikasi halaman default Metasploitable2.  
Versi Apache ini sangat rentan terhadap:
- Remote code execution
- Directory traversal
- WebDAV exploit

---

##  Port 111 – RPCBind
Digunakan untuk pemetaan RPC service.  
Sering menjadi pintu serangan exploit terhadap NFS dan RServices.

---

##  Port 139 dan 445 – SMB (Samba 3.0.20)
SMB berjalan menggunakan Samba 3.0.20 dengan banyak kelemahan:

- NetBIOS vulnerability
- SMB signing disabled
- Null session dapat aktif
- Rentan terhadap *remote code execution*

---

##  Port 512 / 513 / 514 – RServices (rexec, rlogin, rsh)
Ketiga layanan ini sangat berbahaya karena:

- Tidak menggunakan enkripsi  
- Menggunakan autentikasi berbasis host  
- Mudah dieksploitasi untuk mendapatkan akses root

---

##  Port 1099 – Java RMI
Java RMI Registry memungkinkan eksekusi jarak jauh jika tidak dilindungi.  
Rentan terhadap exploit **Remote Code Execution (RCE)**.

---

##  Port 2049 – NFS (rpc.nfsd)
NFS berbagi file system antar host.  
Jika tidak dikonfigurasi dengan baik, penyerang dapat:
- Melakukan mount direktori tanpa autentikasi
- Mengambil file sensitif

---

##  Port 2121 – ProFTPD 1.3.1
ProFTPD versi ini memiliki beberapa celah RCE dan backdoor.  
Sering menjadi target eksploitasi.

---

##  Port 3306 – MySQL 5.0.51a
MySQL menggunakan kredensial default:
- username: **root**
- password: **(kosong)**

Ini sangat berbahaya karena memberi akses penuh database kepada siapa pun.

---

##  Port 3632 – distccd v1 (GNU)
distccd sering dieksploitasi menggunakan serangan RCE.  
Tool ini berjalan tanpa autentikasi sehingga mudah diambil alih.

---

##  Port 5432 – PostgreSQL 8.3.x
PostgreSQL versi lama yang rentan terhadap brute-force dan privilege escalation.

---

##  Port 5900 – VNC (protocol 3.3)
VNC tidak mengenkripsi traffic sehingga dapat disadap.  
Brute-force terhadap password juga mudah dilakukan.

---

##  Port 6000 – X11
X11 sangat berbahaya jika terbuka ke publik.  
Penyerang dapat:
- Mengambil screenshot
- Melihat aktivitas GUI
- Melakukan keylogging

---

##  Port 6667 – UnrealIRCd (backdoor)
Versi UnrealIRCd yang ditemukan memiliki **backdoor bawaan** yang memungkinkan penyerang mengeksekusi perintah jarak jauh (RCE).  
Ini salah satu layanan paling kritis di Metasploitable2.

---

##  Port 7001 – Apache JServ
Digunakan untuk protokol Java lama.  
Rentan terhadap directory traversal dan file disclosure.

---

##  Port 8009 – Apache Tomcat AJP13
AJP13 sering menjadi target eksploit karena konfigurasi default Tomcat yang tidak aman.  
Dapat digunakan untuk:
- File inclusion
- Upload webshell
- Remote code execution

---

##  Port 8180 – Apache Tomcat/Coyote JSP Engine 1.1
Tomcat versi ini memiliki celah seperti:
- Weak admin password
- Upload webshell melalui Tomcat Manager

---

#  Ringkasan Tingkat Kerentanan
Host ini (Metasploitable2) secara keseluruhan sangat rentan karena:

- Banyak layanan lama dan tidak di-update  
- Password default dan layanan tanpa autentikasi  
- Banyak port kritis terbuka  
- Ada layanan yang (secara sengaja) memiliki backdoor  


Di buat oleh : MOCH.FEBRIANTO
