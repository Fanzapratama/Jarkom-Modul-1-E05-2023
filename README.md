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
2. Sebutkan web server yang digunakan pada portal praktikum Jaringan Komputer! nc 10.21.78.111 13579
   Solving : Masuk ke dalam capture packet dan, mengingat bahwa soal memerlukan informasi tentang server, lanjutkan dengan menganalisis protokol HTTP dari file pcap. Ini karena server biasanya menggunakan protokol HTTP.
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-22%20132539.png)
Saya menggunakan keyword "HTTP" untuk melakukan filter pada Wireshark. Awalnya, saya merasa bingung dan menjawab "HTTP," tetapi setelah memeriksa dan menganalisis lebih lanjut, akhirnya saya menemukan informasi yang diperlukan dalam bagian "follow HTTP Stream."
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/2.1.png)
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/2.2.png)

