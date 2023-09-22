# Lapres-jarkom
1. User melakukan berbagai aktivitas dengan menggunakan protokol FTP. nc 10.21.78.111 12345
   Solving: Masuk ke dalam netcat dan perhatikan soal yang diinginkan! Selanjutnya, analisis dilakukan melalui file packet capture yang diberikan.
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-22%20132011.png)
Karena clue yang diberikan oleh soal adalah aktivitas yang terjadi pada protokol FTP, saya menggunakan keyword "FTP" untuk melakukan filter pada Wireshark. Setelah itu, saya mencari paket yang diduga merupakan aktivitas berikut:
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-22%20144709.png)
Setelah itu, saya mencari sequence number (raw) dan menemukan bahwa itu salah. Setelah itu, saya melanjutkan pencarian saya dan menemukan paket berikut:
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-21%20184047.png)
![soal](https://github.com/Fanzapratama/Lapres-jarkom/blob/main/Screenshot%202023-09-21%20185033.png)
![soal]()
