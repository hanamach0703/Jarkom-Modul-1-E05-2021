# Jarkom-Modul-1-E05-2021

Anggota Kelompok:
1. Muhammad Rafki Mardi 05111940000054
2. Hana Machmudah       05111940000072
3. Ahmad Fadillah       05111940000155

## **No. 1 Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!**
### Jawaban No. 1


## **No. 2 Temukan paket dari web-web yang menggunakan basic authentication method!**
### Jawaban No. 2


## **No. 3 Ikuti perintah di `basic.ichimarumaru.tech!` Username dan password bisa didapatkan dari file `.pcapng`!**
### Jawaban No. 3
 
 
## **No. 4  Temukan paket `mysql` yang mengandung perintah query `select`!**
### Jawaban No. 4


#### **No. 5  Login ke `portal.ichimarumaru.tech` kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file `.pcap`!**
### Jawaban No. 5


## **No. 6**
### ari username dan password ketika melakukan login ke FTP Server!
### Jawaban No. 6
Membuka file wireshark `6-7.pcap`
Mencari Username dengan menggunakan filter `tcp contains "USER"`, sehingga didapatkan File transfer Protocol (FTP) USER `secretuser`
![Screenshot (93)](https://user-images.githubusercontent.com/66562311/134371827-e1d8a804-3caf-4bf9-ba19-1d5a6248975e.png)

Mencari PAssword menggunakan filter `tcp contains "PASS"`, sehingga didapatkan File Transfer Protocol (FTP) PASS adalah `aku.pengen.pw.aja`
![Screenshot (94)](https://user-images.githubusercontent.com/66562311/134371951-24498df5-c82f-4923-abf4-fce12b7e86cb.png)


## **No. 7** 
### Ada 500 file zip yang disimpan ke FTP Server dengan nama `0.zip, 1.zip, 2.zip, ..., 499.zip`. Simpan dan Buka file pdf tersebut. `(Hint = nama pdf-nya "Real.pdf")`**
### Jawaban No. 7
Membuka file wireshark `6-7.pcap`
Mennggunakan filter `frame contains "Real.pdf"`
<img width="960" alt="7a" src="https://user-images.githubusercontent.com/66562311/134377132-7ae56c0c-1e83-430e-a4fa-5e3dd39308b5.PNG">

Kemudian klik kanan pilih `follow` kemudian pilih `TCP Stream`
![7b](https://user-images.githubusercontent.com/66562311/134378824-030ae48c-2424-42f0-b6a9-110f66d43f01.png)

Pilih show data `Raw`
![7c](https://user-images.githubusercontent.com/66562311/134379007-8dfe3b0d-acb8-4a75-90be-066ce691414b.png)

Menyimpan file dengan format `pdf`
![7d](https://user-images.githubusercontent.com/66562311/134379126-bdee097b-c037-43d8-9c7c-e241a1111de2.png)

Membuka file
<img width="450" height="350" allign=center alt="7e" src="https://user-images.githubusercontent.com/66562311/134379190-60825c49-5846-43d9-a17f-8b43ee738c33.PNG">


## **No. 8 Cari paket yang menunjukan pengambilan file dari FTP tersebut!**
### Jawaban No. 8


## **No. 9 Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama `secret.zip`. Simpan dan buka file tersebut!**
### Jawaban No. 9


## **No. 10 Selain itu terdapat `history.txt` yang kemungkinan berisi history bash server tersebut!
Gunakan isi dari `history.txt` untuk menemukan password untuk membuka file rahasia yang ada di `secret.zip`!**
### Jawaban No. 10


## **No. 11  Filter sehingga wireshark hanya mengambil paket yang berasal dari `port 80`!**
### Jawaban No. 11


## **No. 12  Filter sehingga wireshark hanya mengambil paket yang mengandung `port 21`!**
### Jawaban No. 12


## **No. 13  Filter sehingga wireshark hanya menampilkan paket yang menuju `port 443`!**
### Jawaban No. 13


## **No. 14 Filter sehingga wireshark hanya mengambil paket yang tujuannya ke `kemenag.go.id`!**
### Jawaban No. 14


## **No. 15 Filter sehingga wireshark hanya mengambil paket yang berasal dari `ip` kalian!**
### Jawaban No. 15

