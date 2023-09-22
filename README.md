# Jarkom-Modul-1-D24-2023
Laporan Praktikum Kelas Jaringan Komputer 2024
Kelompok D24.

<ul>
  <li>Daffa Saskara - 5025211249</li>
  <li>Arundaya Pratama Nurhasan - 5025221205</li>
</ul>

## No1
### Penyelesaian
![no1-jarkom1](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/120204570/940c4311-cb7d-4fc3-b5be-d173b72f7ba4)
<br>
Dari packet yang ter-capture kita menemukan bahwa perintah yang dilakukan oleh user adalah STOR (mengunggah file). Setelah membuka packet tersebut, dengan cara klik kanan 2 kali, kita dapat menemukan sequence dan acknowledge number (raw) dan jika kita melakukan klik kanan kemudian ```follow``` -> ```TCP Stream``` kita dapat melihat Response yang didapat kemudian dengan cara yang sama kita dapat melihat sequence dan acknowledge number (raw)-nya

### Kendala
Tidak ada

## No2
### Penyelesaian
![2pcap](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/88588446/bb78f24a-c544-4acf-9eaf-1b5b41bdf4ee)
<br>
Menggunakan filter ```http contains 10.21.78.111``` klik kanan, dan ```follow``` -> ```TCP Stream```
Dan akan muncul informasi Server menggunakan ```gunicorn``` seperti pada di gambar.
<br>
<br>
<img src="assets/2wsl.jpg" width="700" >

### Kendala
Tidak ada.

## No3
### Penyelesaian
![no3pcap](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/88588446/1aaf8b5e-ec70-4b63-b9f7-65197417adae)
<br>
<br>
Pertama di display filter masukan syntax ```ip.addr == 239.255.255.250 and udp.port == 3702```. Syntax ini digunakan untuk mencari IP dengan address  ```239.255.255.250``` yang berada pada port ```3702```. Hasilnya menunjukan sebanyak 21 pada IP dan Port tersebut dengan Protocol ```UDP```
<br>
<br>
![no3wsl](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/88588446/7b5bf085-00b1-4c20-b13c-3b3e978184e5)
<br>
<br>
### Kendala
Tidak ada.

## No4
### Penyelesaian
![no4pcapwsl](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/88588446/5b4b543b-5aed-4df3-b8e6-025e301dc9ab)
<br>
<br>
Pertama lihat package no ```130``` dengan ```frame.number == 130```, lalu lihat pada bagian kiri bawah pada User Datagram Protocol lalu liat ```Checksum``` tertuliskan ```0x18e5```.
### Kendala
Tidak ada.

## No5
### Penyelesaian
![no5-jarkom1(1)](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/120204570/2eec6301-7aa5-4afa-90f5-7146264abdfc)
<br>
Dengan melihat packet yang ada kita melihat ada info yang mencurigakan dengan tulisan ‘Pass’ setelah kita klik kanan kemudian ```follow``` -> ```TCP Stream``` kita menemukan password dari file zip berupa enkripsi dalam base64.
<br>
<br>
![no5-jarkom1(2)](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/120204570/8c4f2dec-de63-476b-8843-3f25eafde368)
<br>
Setelah kita lakukan deskripsi dan memasukka password tersebut ke file zip yang tersedia maka kita akan mendapat perintah selanjutnya  yaitu membuka ```nc 10.21.78.111 11111```
<br>
<br>
![no5-jarkom1(3)](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/120204570/423fc2c4-3b37-4435-aec6-ab3c0d53e1a4)
<br>
Kemudia akan muncul pertanyaan-pertanyaan selanjutnya yang bisa kita isi untuk mendapatkan flagnya
<br>
<br>
### Kendala
Tidak ada

## No6
### Penyelesaian
![6pcap](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/88588446/125af98f-c258-4d7c-9ade-d0b55c8fd9ec)
<br>
<br>
Pertama adalah cari nomor ```7812``` dengan ```frame.number == 7812``` sesuai dengan soal. Lalu, IP Source didecrypt berdasarkan angka ```(A=1)```, maka hasilnya adalah ```JDRNJA```
<br>
<br>
![6decrypt](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/88588446/82a6d6ae-d8ee-4dac-a818-89b677009074)
<br>
<br>
### Kendala
Memahami soal, teka-teki terlalu dipaksakan.

## No7
### Penyelesaian
![no7-jarkom1](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/120204570/44ac0bf8-a672-4e10-998a-0b035d06a3d6)
<br>
Menggunakan filter “ip.dst == 184.87.193.88”, dan ditampilkan 6 pckg.
<br>
### Kendala
Tidak ada
## No8
### Penyelesaian
![no8pcapwsl](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/88588446/4d85b834-a552-4194-8dbe-9298d2431980)
<br>
pada display filter masukan syntax ```tcp.dstport == 80 || udp.dstport == 80```, maka akan menunjukan bahwa Syntax berhasil
```tcp``` dan ```udp``` menandakan jenis protokol yang digunakan. tanda ```||``` menandakan ```atau```. sehingga kueri akan menampilkan seluruh jenis protokol yang menuju ```port 80```

### Kendala
Tidak ada.

## No9
### Penyelesaian
![no9wsl](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/88588446/14a4a7a9-f636-4b2f-a9d7-4cbf023ccda8)
<br>
```ip.src == 10.51.40.1 && ip.dst != 10.39.55.34```
Pada Display Filter, untuk menyelesaikan soal tersebut digunakan syntax di atas. Namun, pada source dan destination IP tersebut tidak ditemukan alamat yang dicari

### Kendala
tidak ada.

## No10
### Penyelesaian
![no10pcapwsl](https://github.com/daffasas/Jarkom-Modul-1-D24-2023/assets/88588446/6800f811-cda9-47bc-a740-b32def9428a3)
filter ```TELNET``` dan klik kanan lalu ```follow``` -> ```TCP stream```. di sinii ada di frame number ```285```
### Kendala
Tidak ada.
