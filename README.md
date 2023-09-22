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
3.	Dapin sedang belajar analisis jaringan. Bantulah Dapin untuk mengerjakan soal berikut: nc 10.21.78.111 13590
   Solving: Berapa banyak paket yang tercapture dengan IP source maupun destination address adalah 239.255.255.250 dengan port 3702? Saya menggunakan keyword "(ip.src == 239.255.255.250 || ip.dst == 239.255.255.250) && 
   (udp.port == 3702 || tcp.port == 3702) " untuk melakukan filter pada Wireshark. Sehingga berhasil menemukan hasil ini.
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-21%20171312.png)
Setelah menggunakan filter, kami dapat menemukan 21 paket yang menggunakan protokol UDP.
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-21%20171232.png)

