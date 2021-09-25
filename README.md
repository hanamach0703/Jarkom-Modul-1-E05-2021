# Jarkom-Modul-1-E05-2021

Anggota Kelompok:
1. Muhammad Rafki Mardi 05111940000054
2. Hana Machmudah       05111940000072
3. Ahmad Fadillah       05111940000155

## **No. 1**
### Sebutkan webserver yang digunakan pada "ichimarumaru.tech"!
### Jawaban No. 1
Pastikan `ichimarumaru.tech` sudah terbuka pada web browser pilihan. Pilih koneksi jaringan yang sedang digunakan pada `capture interface` dan kosongkan `capture filter`. Akan muncul seluruh hasil capture, pada `display filter` masukan filter berikut.
```
http.host=="ichimarumaru.tech"
```
<!-- foto 1-1 -->
![1-1](https://user-images.githubusercontent.com/74223938/134753872-ff2b7778-d920-45ea-96e5-7316541f19a8.png)

Filter diatas akan menampilkan seluruh paket yang menuju atau berasal dari `ichimarumaru.tech` seperti berikut.
<!-- foto 1-2 -->
![1-2](https://user-images.githubusercontent.com/74223938/134753882-eb3c430f-dca8-4eea-8cd3-f38632a4d874.png)

<!-- foto 1-3 -->
![1-3](https://user-images.githubusercontent.com/74223938/134753884-0c6e19ab-f3d3-4104-a9ca-229ce406f2eb.png)

Klick kanan pada salah satu paket, lalu pilih `Follow` kemudian pilih `TCP Stream` maka akan didapati bahwa webserver yang digunakan adalah `Nginx`
## **No. 2**
### Temukan paket dari web-web yang menggunakan basic authentication method!
### Jawaban No. 2
Pastikan `ichimarumaru.tech` sudah terbuka pada web browser pilihan. Ketika muncul situs yang meminta kredensial, lakukan login dengan kredensial bebas (ngasal).
<!-- foto 2-1 -->
![2-1](https://user-images.githubusercontent.com/74223938/134753888-9928f4c1-cd39-49b6-8daa-c956b0d97f68.png)

Pilih koneksi jaringan yang sedang digunakan pada `capture interface` dan kosongkan `capture filter`. Akan muncul seluruh hasil capture, pada `display filter` masukan filter berikut.
```
http.host=="basic.ichimarumaru.tech"
```
Pilih paket paling bawah, lalu buka atribut `Hypertext Trasnfer Protokol`. Akan terlihat website tersebut menggunakan `Authorization: Basic` serta `token` dan `string` kredensial yang kita masukan tadi.
<!-- foto 2-2 -->
![2-2](https://user-images.githubusercontent.com/74223938/134753890-cffd2c1e-b79b-4bb2-a4a3-ede6144d814c.png)

## **No. 3**
### Ikuti perintah di `basic.ichimarumaru.tech!` Username dan password bisa didapatkan dari file `.pcapng`!
### Jawaban No. 3
Pada `basic.ichimarumaru.tech` terlihat tulisan yang menyebutkan `only network practitioners can continue`. Buka file `1-5.pcapng`, lalu akan mucncul window wireshark baru yang berisi paket yang di-`capture`. Pada display filter, masukan string.
```
http.host contains "basic.ichimarumaru.tech"
```
<!-- foto 3-1 -->
![3-1](https://user-images.githubusercontent.com/74223938/134753893-964ee4cc-0fc4-4dbf-92a3-ba4d2edb1c30.png)

Akan muncul paket yang terkait dengan `basic.ichimarumaru.tech` yang mana bisa beragam hal (source, destination atau lainnya), lalu pilih `meme.png` dan buka atribut `Hypertext Transfer Protocol` buka sub-atribut `Authorization` dan tertampil `string` kredensial.
<!-- foto 3-2 -->
![3-2](https://user-images.githubusercontent.com/74223938/134753898-7e7c56c8-a1b0-4795-9068-88b8cd901989.png)

Masukan string tersebut ke kredensial `basic.ichimarumaru.tech`
<!-- foto 3-3 -->
![3-3](https://user-images.githubusercontent.com/74223938/134753902-9d7cdee5-c6b9-42c4-a0e7-5ca7a213aaf5.png)

Akan muncul pertanyaan dan diisi dengan sebenar - benarnya.
<!-- foto 3-4 -->
![3-4](https://user-images.githubusercontent.com/74223938/134753905-50e937e8-915b-4d6c-8a3d-bc2a914df8c4.png)

## **No. 4**
### Temukan paket `mysql` yang mengandung perintah query `select`!
### Jawaban No. 4
Masih di file yang sama, masukan `string` berikut ke display filter
```
frame contains "select"
```
<!-- foto 4-1 -->
![4-1](https://user-images.githubusercontent.com/74223938/134753907-cf415a12-3e2d-491b-a023-e39398892a83.png)

Akan muncul dua paket, tiap paket dibuka atribut `MySQL Protocol` dan sub-atribut `Request Command Query`. Terlihat dua `query` berikut.

<!-- foto 4-2 -->
![4-2](https://user-images.githubusercontent.com/74223938/134753911-c9848d64-6b93-4157-97ef-e58fbba9e93c.png)

<!-- foto 4-3 -->
![4-3](https://user-images.githubusercontent.com/74223938/134753912-3e019a5c-3667-4444-b407-f1d4ce78eb7c.png)

#### **No. 5**
### Login ke `portal.ichimarumaru.tech` kemudian ikuti perintahnya! Username dan password bisa didapat dari query insert pada table users dari file `.pcap`!
### Jawaban No. 5
Masih di file yang sama, masukan `string` berikut ke display filter
```
frame contains "INSERT"
```
Akan muncul satu paket,buka atribut `MySQL Protocol` dan sub-atribut `Request Command Query`. Terlihat `value` dari `INSERT` berikut.
<!-- foto 5-1 -->
![5-1](https://user-images.githubusercontent.com/74223938/134753916-c41d3b35-e478-4ca9-a403-78734ac410c3.png)

Masukan `string` tersebut ke `portal.ichimarumaru.tech` sesuai dengan atributnya (username:password[tanpa md5()]).
<!-- foto 5-2 -->
![5-2](https://user-images.githubusercontent.com/74223938/134753918-cfce76a4-7360-4380-8299-0878c8b16f17.png)

Akan muncul pertanyaan tertentu dan jawab dengan benar
<!-- foto 5-3 -->
![5-3](https://user-images.githubusercontent.com/74223938/134753923-561d8729-a0bf-4bf5-9864-462f144c4027.png)

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

Membuka file wireshark `8-10.pcap`
Melakukan filter `tcp-data.command == "RETR"` untuk menemukan paket yang menunjukkan pengmabilan file dari FTP, namun tidak ditemukan paket tersebut.

![8a](https://user-images.githubusercontent.com/66562311/134467422-4d5727b3-4705-47aa-9a61-aaa3c6d7fc09.png)

Melakukan filter `tcp-data.command` memnag tidak ditemukan paket dengan info `RETR`

![8b](https://user-images.githubusercontent.com/66562311/134467554-03baffef-1152-4fbe-b2c8-93db730fa04b.png)



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
### Selain itu terdapat `history.txt` yang kemungkinan berisi history bash server tersebut! Gunakan isi dari `history.txt` untuk menemukan password untuk membuka file rahasia yang ada di `secret.zip`!

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

Untuk nomor 11 kita dapat menuliskan 
```
src hst port 80
```
pada capture filter



## **No. 12**
### Filter sehingga wireshark hanya mengambil paket yang mengandung `port 21`!
### Jawaban No. 12

Untuk nomor 12 kita dapat menuliskan
```
hst port 21
```
pada capture filter



## **No. 13**
### Filter sehingga wireshark hanya menampilkan paket yang menuju `port 443`!
### Jawaban No. 13

Untuk nomor 12 kita dapat menuliskan
```
tcp.dstport == 443
```
pada display filter



## **No. 14**
### Filter sehingga wireshark hanya mengambil paket yang tujuannya ke `kemenag.go.id`!
### Jawaban No. 14

Pertama-tama kita buka website `kemenag.co.id`,
kemudian sebelum meng-capture kita tuliskan 
```
dst hst kemenag.co.id
```
pada capture filter 



## **No. 15**
### Filter sehingga wireshark hanya mengambil paket yang berasal dari `ip` kalian!
### Jawaban No. 15

Untuk nomor 15 kita hanya perlu menulis
```
src hst [ip]
```
pada capture filter menurut ip masing-masing


