# Jarkom-Modul-1-C02-2021

|         Nama        |       NRP      |
|        :----:       |     :----:     |
| Muhammad Bagus I    | 05111940000049 |
| Christoffer Ivano   | 05111940000091 |
| Bayu Adjie Sidharta | 05111940000172 |

# 1
## Soal
Sebutkan webserver yang digunakan pada "ichimarumaru.tech"! 
## Jawaban
Filter = `http.host == "ichimarumaru.tech"`
## Cara
Pilih salah satu yang didapat lalu follow TCP Stream untuk melihat servernya.

[![1.png](https://i.postimg.cc/PJxmkcGn/1.png)](https://postimg.cc/wyCtXwTw)


# 2
## Soal
Temukan paket dari web-web yang menggunakan basic authentication method!
## Jawaban
Filter = `http.authbasic`
## Cara
Masukkan filter dan paket sudah langsung tampil.

[![2.png](https://i.postimg.cc/QxvcR00v/2.png)](https://postimg.cc/8jBFvB8b)


# 3
## Soal
Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!
## Jawaban
frame contains basic

[![3a.png](https://i.postimg.cc/CKgkKdyN/3a.png)](https://postimg.cc/tsBYSq4Z)

[![3b.png](https://i.postimg.cc/PJP87wZt/3b.png)](https://postimg.cc/n9fzjM05)


# 4
## Soal
Temukan paket mysql yang mengandung perintah query select!
## Jawaban
mysql.query matches select

[![4.png](https://i.postimg.cc/63SrLXbb/4.png)](https://postimg.cc/2bQLrPDn)


# 5
## Soal
Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!
## Jawaban
mysql.query matches insert

[![5a.png](https://i.postimg.cc/fWtjWVkG/5a.png)](https://postimg.cc/8sGrtPR4)

[![5b.png](https://i.postimg.cc/G2kLzPX0/5b.png)](https://postimg.cc/ZB5z5Nkj)


# 6
## Soal
Cari username dan password ketika melakukan login ke FTP Server!
## Jawaban
ftp && frame contains user

[![6a.png](https://i.postimg.cc/Fz7PNp88/6a.png)](https://postimg.cc/N2v8x6gk)

[![6b.png](https://i.postimg.cc/hv62jxqj/6b.png)](https://postimg.cc/30jXfkN5)


# 7
## Soal
Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")
## Jawaban
filter = `frame contains “Real.pdf`
## Cara
Pilih salah satu paket lalu follow TCP Stream ubah show data menjadi Raw dan simpan Real.pdf.

[![7.png](https://i.postimg.cc/zfz64CDZ/7.png)](https://postimg.cc/gx7gZ66N)


# 8
## Soal
Cari paket yang menunjukan pengambilan file dari FTP tersebut!
## Jawaban
ftp-data.command == RETR

[![8.png](https://i.postimg.cc/C5qQbJ7D/8.png)](https://postimg.cc/RJvdB7jV)


# 9
## Soal
Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!
## Jawaban
filter = `ftp-data.command contains "secret.zip"`
## Cara
Pilih salah satu paket lalu follow TCP Stream ubah show data menjadi Raw dan simpan secret.zip. Setelah dibuka terdapat file wanted.pdf yang membutuhkan password.

[![9.png](https://i.postimg.cc/3NmtkNrF/9.png)](https://postimg.cc/fSWcFw9V)


# 10
## Soal
Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!
## Jawaban
filter = `ftp-data.command contains "history.txt"`
## Cara
Pilih paket dan follow TCP Stream dan akan muncul text yang menunjukkan bukanapaapa.txt
[![10a.png](https://i.postimg.cc/hj7rYvmR/10a.png)](https://postimg.cc/G8dG8czX)

## Jawaban
ftp-data.command contains "bukanapaapa.txt"
## Cara
Pilih paket dan follow TCP Stream, ubah show data menjadi raw lalu save menjadi bukanapaapa.txt. Buka file tersebut maka akan muncul password untuk file wanted.pdf pada secret.zip.

[![10b.png](https://i.postimg.cc/90dBWk1x/10b.png)](https://postimg.cc/ctJ3hXpY)

## Cara
Masukkan password yang didapat dari bukanapaapa.txt lalu file wanted.pdf akan terbuka seperti berikut.
[![10b.png](https://i.postimg.cc/90dBWk1x/10b.png)](https://postimg.cc/ctJ3hXpY)


# 11
## Soal
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80! 
## Jawaban
Ketik `src port 80` pada capture filter, lalu wireshark berjalan. Kemudian wireshark mendeteksi paket yang berasal dari port 80.


[![11.png](https://i.postimg.cc/RVs8r5HG/11.png)](https://postimg.cc/Cz8JD2Jf)


# 12
## Soal
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
## Jawaban
Ketik `port 21` pada capture filter, lalu wireshark berjalan. Kemudian wireshark mendeteksi paket yang mengandung port 21

[![12.png](https://i.postimg.cc/HW3v5DBH/12.png)](https://postimg.cc/F1dx56Mn)


# 13
## Soal
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
## Jawaban
Ketik `dst port 443` pada capture filter, lalu wireshark berjalan. Kemudian wireshark mendeteksi paket yang menuju port 443

[![13.png](https://i.postimg.cc/kGhyHCpb/13.png)](https://postimg.cc/p5z89wxW)


# 14
## Soal
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!
## Jawaban
Ketik `dst host kemenag.go.id` pada capture filter, lalu wireshark berjalan.
Tampilan awal wireshark tidak mendeteksi apapun karena memang belum dibuka websitenya. Setelah dibuka website kemenag.go.id maka wireshark dapat mengambil paket yang tujuannya ke kemenag.go.id

[![14.png](https://i.postimg.cc/KYrD2BWF/14.png)](https://postimg.cc/sBxhPQy0)


# 15
## Soal
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
## Jawaban
Pertama - tama Cek IP kita melalui Run as Administrator Command Prompt. Lalu Ketikkan "ipncofig". Setelah itu akan muncul IP kita. IP kita ditandai dengan IPv4 Address yakni dengan IP 192.168.1.7.

[![1632432194734.jpg](https://i.postimg.cc/ht8dzg11/1632432194734.jpg)](https://postimg.cc/dh11pbXh)


Lalu kita ambil paket yang hanya berasal dari IP kita yakni dengan cara mengetik
`ip src 192.168.1.7` sebagai capture filter

[![1632432890702.jpg](https://i.postimg.cc/1tYQvnsc/1632432890702.jpg)](https://postimg.cc/2bvM65qV)


# Kendala & Error
1. Kendala Wifi Indihome & Telkomsel yang lagi lemot membuat praktikum terhambat
2. 




