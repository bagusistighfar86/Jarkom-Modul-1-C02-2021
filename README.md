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
http.host == "ichimarumaru.tech"

# 2
## Soal
Temukan paket dari web-web yang menggunakan basic authentication method!
## Jawaban
http.authbasic

# 3
## Soal
Ikuti perintah di basic.ichimarumaru.tech! Username dan password bisa didapatkan dari file .pcapng!
## Jawaban
frame contains basic


# 4
## Soal
Temukan paket mysql yang mengandung perintah query select!
## Jawaban
mysql.query matches select

# 5
## Soal
Login ke portal.ichimarumaru.tech kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file .pcap!
## Jawaban
mysql.query matches insert

# 6
## Soal
Cari username dan password ketika melakukan login ke FTP Server!
## Jawaban
ftp && frame contains user

# 7
## Soal
Ada 500 file zip yang disimpan ke FTP Server dengan nama 0.zip, 1.zip, 2.zip, ..., 499.zip. Simpan dan Buka file pdf tersebut. (Hint = nama pdf-nya "Real.pdf")
## Jawaban
frame contains “Real.pdf

# 8
## Soal
Cari paket yang menunjukan pengambilan file dari FTP tersebut!
## Jawaban
ftp-data.command == RETR

# 9
## Soal
Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama "secret.zip". Simpan dan buka file tersebut!
## Jawaban
ftp-data.command contains "secret.zip"

# 10
## Soal
Selain itu terdapat "history.txt" yang kemungkinan berisi history bash server tersebut! Gunakan isi dari "history.txt" untuk menemukan password untuk membuka file rahasia yang ada di "secret.zip"!
## Jawaban
ftp-data.command contains "history.txt"
ftp-data.command contains "bukanapaapa.txt"

# 11
## Soal
Filter sehingga wireshark hanya mengambil paket yang berasal dari port 80! 
## Jawaban
src port 80

# 12
## Soal
Filter sehingga wireshark hanya mengambil paket yang mengandung port 21!
## Jawaban
port 21

# 13
## Soal
Filter sehingga wireshark hanya menampilkan paket yang menuju port 443!
## Jawaban
dst port 443

# 14
## Soal
Filter sehingga wireshark hanya mengambil paket yang tujuannya ke kemenag.go.id!
## Jawaban
dst host kemenag.go.id

# 15
## Soal
Filter sehingga wireshark hanya mengambil paket yang berasal dari ip kalian!
## Jawaban
ip src 192.168.1.8

