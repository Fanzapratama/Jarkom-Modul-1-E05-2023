# Lapres-jarkom
1. User melakukan berbagai aktivitas dengan menggunakan protokol FTP. nc 10.21.78.111 12345
   Solving: Masuk ke dalam netcat dan perhatikan soal yang diinginkan! Selanjutnya, analisis dilakukan melalui file packet capture yang diberikan.
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-22%20132011.png)

Karena clue yang diberikan oleh soal adalah aktivitas yang terjadi pada protokol FTP, saya menggunakan keyword "FTP" untuk melakukan filter pada Wireshark. Setelah itu, saya mencari paket yang diduga merupakan aktivitas berikut:
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-22%20144709.png)

Setelah itu, saya mencari sequence number (raw) dan menemukan bahwa itu salah. Setelah itu, saya melanjutkan pencarian saya dan menemukan paket berikut:

![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-21%20184047.png)
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-21%20185033.png)
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-21%20184807.png)
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-21%20184818.png)

FLAG:	Jarkom2023{y0u_r_g00d_4t_4dr3ssing_BxKoMxD44474065}

2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer! nc 10.21.78.111 13579
   Solving : Masuk ke dalam capture packet dan, mengingat bahwa soal memerlukan informasi tentang server, lanjutkan dengan menganalisis protokol HTTP dari file pcap. Ini karena server biasanya menggunakan protokol HTTP.

![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-22%20132539.png)

Saya menggunakan keyword "HTTP" untuk melakukan filter pada Wireshark. Awalnya, saya merasa bingung dan menjawab "HTTP," tetapi setelah memeriksa dan menganalisis lebih lanjut, akhirnya saya menemukan informasi yang diperlukan dalam bagian "follow HTTP Stream."

![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/2.1.png)
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/2.2.png)

FLAG: Jarkom2023{9unic0rn_1s_8B0YW3w304dxCxp_c00l}

3.	Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut: nc 10.21.78.111 13590
   Solving: Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702? Saya menggunakan keyword "(ip.src == 239.255.255.250 || ip.dst == 239.255.255.250) && 
   (udp.port == 3702 || tcp.port == 3702) " untuk melakukan filter pada Wireshark. Sehingga berhasil menemukan hasil ini.

![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-21%20171312.png)

Setelah menggunakan filter, kami dapat menemukan 21 paket yang menggunakan protokol UDP.


4. Berapa nilai checksum yang didapat dari header pada paket nomor 130? nc 10.21.78.111 13591
   Solving: Untuk mengambil nilai checksum dari paket nomor 130, langkah pertama adalah menemukan paket nomor 130 dalam daftar, kemudian periksa bagian checksum pada paket tersebut, seperti paket berikut:

![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-22%20125111.png)

![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-21%20172730.png)

![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/4.png)














6. ncat 10.21.78.111 6666
   Seorang anak bernama Udin Berteman dengan SlameT yang merupakan seorang penggemar film detektif. sebagai teman yang baik, Ia selalu mengajak slamet untuk bermain valoranT bersama. suatu malam, terjadi sebuah hal yang tak     terdUga. ketika udin mereka membuka game    tersebut, laptop udin menunjukkan sebuah field text dan Sebuah kode Invalid bertuliskan "server SOURCE ADDRESS 7812 is invalid". ketika ditelusuri di google, hasil pencarian         hanya menampilkan a1 e5 u21. jiwa detektif slamet pun bergejolak. bantulah udin dan    slamet untuk menemukan solusi kode error tersebut.
   Seorang anak laki-laki bernama Udin berteman dengan Slamet, pria yang menyukai film detektif. Sebagai teman baik, ia selalu mengajak Slamet bermain Valorant bersamanya. Suatu malam, sesuatu yang tidak terduga terjadi. Saat Udin  membuka game tersebut, laptop Udin      menampilkan kolom teks tidak valid dan  kode  bertuliskan "ALAMAT SUMBER SERVER 7812 tidak valid". Saat searching di Google, hasil pencarian hanya menampilkan a1 e5 u21. Jiwa Detektif Slamet bergetar. Bantu Udin dan Slamet menemukan solusi atas kode kesalahan          tersebut.
   dari hint yang terdapat bisa ditarik solusi ➔ 104.18.14.101 → 0-18 → 10 4 18 14 10 1 → J D R N J A
   seperti pada gambar berikut:
   ![soal1](https://github.com/stevanza/LapresJarkom/blob/main/WhatsApp%20Image%202023-09-22%20at%2009.24.21.jpeg)
   ![soal1](https://github.com/stevanza/LapresJarkom/blob/main/WhatsApp%20Image%202023-09-22%20at%2009.22.34.jpeg)

   Flag :  Jarkom2023{h3h3_ctf_d1k1t_a0GO675X225VW7IQZ7kx}

7. nc 10.21.78.111 6565
   Berapa jumlah packet yang menuju IP 184.87.193.88?
   ![soal1](https://github.com/stevanza/LapresJarkom/blob/main/WhatsApp%20Image%202023-09-22%20at%2009.26.49.jpeg)
   ![soal](https://github.com/stevanza/LapresJarkom/blob/main/WhatsApp%20Image%202023-09-22%20at%2009.27.00.jpeg)

   Flag: Jarkom2023{c94ERFV5EG9Rgy2Oa0_4n0th3r_f1lt3ring}

8. nc 10.21.78.111 7171
   Berikan kueri filter sehingga wireshark hanya mengambil semua protokol paket yang menuju port 80! (Jika terdapat lebih dari 1 port, maka urutkan sesuai dengan abjad)!
   ![soal](https://github.com/stevanza/LapresJarkom/blob/main/WhatsApp%20Image%202023-09-22%20at%2009.29.33.jpeg)

   Flag: Jarkom2023{qu3ryyyyying_998893_AzNwFxEhDuO_15_fun}

9.nc 10.21.78.111 7272
   Berikan kueri filter sehingga wireshark hanya mengambil paket yang berasal dari alamat 10.51.40.1 tetapi tidak menuju ke alamat 10.39.55.34!
   ![soal](https://github.com/stevanza/LapresJarkom/blob/main/WhatsApp%20Image%202023-09-22%20at%2009.38.08.jpeg)

   Flag: Jarkom2023{y3s_its_RkOkNkNlNmO_qu3ry1ng}

10. nc 10.21.78.111 7373
    Sebutkan kredensial yang benar ketika user mencoba login menggunakan Telnet!
    ![soal](https://github.com/stevanza/LapresJarkom/blob/main/WhatsApp%20Image%202023-09-22%20at%2009.44.52.jpeg)
    ![soal1](https://github.com/stevanza/LapresJarkom/blob/main/WhatsApp%20Image%202023-09-22%20at%2009.44.39.jpeg)

