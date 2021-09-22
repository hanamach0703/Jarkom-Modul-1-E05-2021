# Jarkom-Modul-1-E05-2021

Anggota Kelompok:
1. Muhammad Rafki Mardi 05111940000054
2. Hana Machmudah       05111940000072
3. Ahmad Fadillah       05111940000155

## **No. 1**
### Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!
### Jawaban No. 1


## **No. 2**
### Temukan paket dari web-web yang menggunakan basic authentication method!
### Jawaban No. 2


## **No. 3**
### Ikuti perintah di `basic.ichimarumaru.tech!` Username dan password bisa didapatkan dari file `.pcapng`!
### Jawaban No. 3
 
 
## **No. 4**
### Temukan paket `mysql` yang mengandung perintah query `select`!
### Jawaban No. 4


#### **No. 5**
### Login ke `portal.ichimarumaru.tech` kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file `.pcap`!
### Jawaban No. 5


## **No. 6**
### Cari username dan password ketika melakukan login ke FTP Server!

### Jawaban No. 6
Membuka file wireshark `6-7.pcap`
Mencari Username dengan menggunakan filter `tcp contains "USER"`, sehingga didapatkan File transfer Protocol (FTP) USER `secretuser`
![Screenshot (93)](https://user-images.githubusercontent.com/66562311/134371827-e1d8a804-3caf-4bf9-ba19-1d5a6248975e.png)

Mencari PAssword menggunakan filter `tcp contains "PASS"`, sehingga didapatkan File Transfer Protocol (FTP) PASS adalah `aku.pengen.pw.aja`
![Screenshot (94)](https://user-images.githubusercontent.com/66562311/134371951-24498df5-c82f-4923-abf4-fce12b7e86cb.png)


## **No. 7** 
### Ada 500 file zip yang disimpan ke FTP Server dengan nama `0.zip, 1.zip, 2.zip, ..., 499.zip`. Simpan dan Buka file pdf tersebut. `(Hint = nama pdf-nya "Real.pdf")`

### Jawaban No. 7
Membuka file wireshark `6-7.pcap`
Menggunakan filter `frame contains "Real.pdf"`

![7a](https://user-images.githubusercontent.com/66562311/134380887-31eff4dc-4d05-4419-ab58-962b9fcf76ea.png)

Kemudian klik kanan pilih `follow` kemudian pilih `TCP Stream`

![7b](https://user-images.githubusercontent.com/66562311/134378824-030ae48c-2424-42f0-b6a9-110f66d43f01.png)

Pilih show data `Raw`

![7c](https://user-images.githubusercontent.com/66562311/134379007-8dfe3b0d-acb8-4a75-90be-066ce691414b.png)

Menyimpan file dengan format `pdf`.

![7d](https://user-images.githubusercontent.com/66562311/134379126-bdee097b-c037-43d8-9c7c-e241a1111de2.png)

Membuka file yang telah di save.

![7e](https://user-images.githubusercontent.com/66562311/134380934-dcef1aaa-73f2-42ed-a7c2-ba69a9e01677.png)


## **No. 8**
### Cari paket yang menunjukan pengambilan file dari FTP tersebut!

### Jawaban No. 8

Mmbuka file wireshark `8-10.pcap`


## **No. 9**
### Dari paket-paket yang menuju FTP terdapat inidkasi penyimpanan beberapa file. Salah satunya adalah sebuah file berisi data rahasia dengan nama `secret.zip`. Simpan dan buka file tersebut!

### Jawaban No. 9
Membuka file wireshark `8-10.pcap`
Menggunakan filter `ftp-data` kemudian ctrl+F `secret` untuk mendapatkan paket berisi data rahasia

![9a](https://user-images.githubusercontent.com/66562311/134384478-1fbb3983-9297-4fdf-a39d-09506c7d469a.png)

Klik Kanan pilih`follow` kemudian pilih `TCP Stream`

![9b](https://user-images.githubusercontent.com/66562311/134384633-659180f8-9f79-41bc-85a0-87bac0f70f23.png)

Menyimpan file dengan show data `Raw` simpan file dalam bentuk `zip` sesuai dengan ekstansi file dalam soal.

![9c](https://user-images.githubusercontent.com/66562311/134384936-a90c02ad-617d-4628-9aa1-c487cc6f1a07.png)

Membuka file yang telah disimpan `secret.zip` dengan melakukan ekstarksi file terlebih dahulu. Hingga didapatkan file seperti ini. Terdapat password untuk membuka file `secret.zip`

![9d](https://user-images.githubusercontent.com/66562311/134385099-7796e5c5-49e7-47a2-af63-1856b942b6e2.png)


## **No. 10**
### **Selain itu terdapat `history.txt` yang kemungkinan berisi history bash server tersebut!
Gunakan isi dari `history.txt` untuk menemukan password untuk membuka file rahasia yang ada di `secret.zip`!**

### Jawaban No. 10
Pada soal No. 10 menggunakan tetap file wireshark `8-10.pcap`
Untuk mendapatkan isi dari `history.txt`. Perlu memfilter menggunakan `ftp-data` kemudian ctrl+F `history`

![10a](https://user-images.githubusercontent.com/66562311/134389079-fd60a4be-d01e-4483-9fda-4f9f35f92c15.png)

klik kanan pilih `follow` kemudian pilih `TCP Stream` akan didapatkan isi data sebagai berikut:

![10b](https://user-images.githubusercontent.com/66562311/134389395-a2486ea8-22af-46c8-b1c3-e07366d68a6b.png)

Dalam data didapat nama file `bukanapaapa.txt`. Mencoba mencari paket mengandung `bukanapaapa`

![10c](https://user-images.githubusercontent.com/66562311/134389702-50f54541-c43e-46b3-94e1-ca7ebb8d4b4b.png)

Buka isi dari paket yang mengandung `bukanapaapa.txt` dengan mengklik kanan kemudian pilih `follow` selanjutnya pilih `TCP Stream`. Didapatkan data yang merupakan password dari file yang `secret.zip` dalam soal No. 9.

![10d](https://user-images.githubusercontent.com/66562311/134390017-f6552001-8c99-4143-88c9-b2c7b8ea3e3a.png)

Memasukkan password pada file `secret.zip`.

![10e](https://user-images.githubusercontent.com/66562311/134390304-1b286678-f4bb-47af-a277-9a6959227925.png)

Didapatkan Isi dari file `secret.zip`.

![10f](https://user-images.githubusercontent.com/66562311/134390438-0a0ba735-aad4-4dc1-a2c2-8d2e901d0b4a.png)


## **No. 11**
### Filter sehingga wireshark hanya mengambil paket yang berasal dari `port 80`!
### Jawaban No. 11


## **No. 12**
### Filter sehingga wireshark hanya mengambil paket yang mengandung `port 21`!
### Jawaban No. 12


## **No. 13**
### Filter sehingga wireshark hanya menampilkan paket yang menuju `port 443`!
### Jawaban No. 13


## **No. 14**
### Filter sehingga wireshark hanya mengambil paket yang tujuannya ke `kemenag.go.id`!
### Jawaban No. 14


## **No. 15**
### Filter sehingga wireshark hanya mengambil paket yang berasal dari `ip` kalian!
### Jawaban No. 15

