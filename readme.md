# Praktikum-Jarkom-Modul-4

# Anggota

| Nama                            | NRP          |
| ------------------------------- | ------------ |
| Marcelinus Alvinanda Chrisantya | `5027221012` |
| Bintang Ryan Wardana            | `5027221022` |

# Topologi 

# Rute Subnet


# VLSM - GN3
Teknik subnetting yang dikenal sebagai Variable Length Subnet Masking (VLSM) merupakan teknik yang digunakan untuk memaksimalkan pembagian alamat IP di dalam jaringan. Netmask besar disesuaikan dengan banyaknya komputer atau host yang membutuhkan alamat IP.
VLSM membagi jaringan besar menjadi subnet yang lebih kecil. Setiap subnet kemudian diberi netmask yang sesuai dengan jumlah host yang dibutuhkannya. Dengan demikian, netmask dengan jumlah host yang lebih besar akan memiliki bitmask yang lebih sedikit, sementara netmask dengan jumlah host yang lebih sedikit akan memiliki bitmask yang lebih besar.

Metode VLSM dilakukan menggunakan platform GNS3. Berikut adalah penjelasan lebih lanjutnya : 
## Tree
Berikut adalah tree untuk pembagian IP dimulai dari 10.78.0.0/20
![vlsmtree-it29](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/143849730/010c5484-f433-46b8-b9ba-bbdf45a2eae5)
## Pembagian IP
Berikut adalah pembagian IP yang diperoleh dari hasil pemecahan tree menjadi jaringan yang lebih kecil :
![image](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/143849730/20e9dfe3-8102-421e-9eeb-bb85d61c4241)
## Konfigurasi Network 
**JAWA**
```
auto lo
iface lo inet loopback

auto eth0
iface eth0 inet dhcp

#A3
auto eth1
iface eth1 inet static
address 10.78.21.197
netmask 255.255.255.252

#A2
auto eth2
iface eth2 inet static
address 10.78.21.193
netmask 255.255.255.252

#A1
auto eth3
iface eth3 inet static
address 10.78.21.189
netmask 255.255.255.252
```
**SULAWESI**
```
auto lo
iface lo inet loopback

#A1
auto eth0
iface eth0 inet static
address 10.78.21.190
netmask 255.255.255.252
gateway 10.78.21.189

#A6
auto eth1
iface eth1 inet static
address 10.78.21.161
netmask 255.255.255.248

#A4
auto eth2
iface eth2 inet static
address 10.78.20.1
netmask 255.255.255.128
```
**KALIMANTAN**
```
auto lo
iface lo inet loopback

#A2
auto eth0
iface eth0 inet static
address 10.78.21.194
netmask 255.255.255.252
gateway 10.78.21.193

#A9
auto eth1
iface eth1 inet static
address 10.78.21.201
netmask 255.255.255.252
```
**SUMATERA**
```
auto lo
iface lo inet loopback

#A3
auto eth0
iface eth0 inet static
address 10.78.21.198
netmask 255.255.255.252
gateway 10.78.21.197

#A16
auto eth1
iface eth1 inet static
address 10.78.21.205
netmask 255.255.255.252

#A18
auto eth2
iface eth2 inet static
address 10.78.21.65
netmask 255.255.255.224
```
**PC-Marisa**
```
#A4
auto eth0
iface eth0 inet static
address 10.78.20.2
netmask 255.255.255.128
gateway 10.78.20.1
```
**PC-Gorontalo**
```
#A4
auto eth0
iface eth0 inet static
address 10.78.20.3
netmask 255.255.255.128
gateway 10.78.20.1
```
**MALUKU-UTARA**
```
auto lo
iface lo inet loopback

#A4
auto eth0
iface eth0 inet static
address 10.78.20.4
netmask 255.255.255.128
gateway 10.78.20.1

#A5
auto eth1
iface eth1 inet static
address 10.78.0.1
netmask 255.255.248.0
```
**Tobelo**
```
#A5
auto eth0
iface eth0 inet static
address 10.78.0.2
netmask 255.255.248.0
gateway 10.78.0.1
```
**Morotai**
```
#A5
auto eth0
iface eth0 inet static
address 10.78.0.3
netmask 255.255.248.0
gateway 10.78.0.1
```
**Ternate**
```
#A5
auto eth0
iface eth0 inet static
address 10.78.0.4
netmask 255.255.248.0
gateway 10.78.0.1
```
**MAKASSAR**
```
auto lo
iface lo inet loopback

#A6
auto eth0
iface eth0 inet static
address 10.78.21.162
netmask 255.255.255.248
gateway 10.78.21.161

#A7
auto eth1
iface eth1 inet static
address 10.78.21.169
netmask 255.255.255.248
```
**Galesong**
```
#A7
auto eth0
iface eth0 inet static
address 10.78.21.170
netmask 255.255.255.248
gateway 10.78.21.169
```
**Topejawa**
```
#A7
auto eth0
iface eth0 inet static
address 10.78.21.171
netmask 255.255.255.248
gateway 10.78.21.169
```
**BELAWA**
```
auto lo
iface lo inet loopback

#A6
auto eth0
iface eth0 inet static
address 10.78.21.163
netmask 255.255.255.248
gateway 10.78.21.161

#A8
auto eth1
iface eth1 inet static
address 10.78.21.1
netmask 255.255.255.192
```
**Madini**
```
#A8
auto eth0
iface eth0 inet static
address 10.78.21.2
netmask 255.255.255.192
gateway 10.78.21.1
```
**Baru**
```
#A8
auto eth0
iface eth0 inet static
address 10.78.21.3
netmask 255.255.255.192
gateway 10.78.21.1
```
**KALIMANTAN-UTARA**
```
auto lo
iface lo inet loopback

#A9
auto eth0
iface eth0 inet static
address 10.78.21.202
netmask 255.255.255.252
gateway 10.78.21.201

#A10
auto eth1
iface eth1 inet static
address 10.78.18.1
netmask 255.255.255.0

#A11
auto eth2
iface eth2 inet static
address 10.78.21.181
netmask 255.255.255.252
```
**Selimau**
```
#A10
auto eth0
iface eth0 inet static
address 10.78.18.2
netmask 255.255.255.0
gateway 10.78.18.1
```
**KALIMANTAN-TIMUR**
```
auto lo
iface lo inet loopback

#A11
auto eth0
iface eth0 inet static
address 10.78.21.182
netmask 255.255.255.252
gateway 10.78.21.181


#A12
auto eth1
iface eth1 inet static
address 10.78.21.177
netmask 255.255.255.252

#A13
auto eth2
iface eth2 inet static
address 10.78.16.1
netmask 255.255.254.0
```
**Bangkirai**
```
#A13
auto eth0
iface eth0 inet static
address 10.78.16.2
netmask 255.255.254.0
gateway 10.78.16.1
```
**Lamaru**
```
#A13
auto eth0
iface eth0 inet static
address 10.78.16.3
netmask 255.255.254.0
gateway 10.78.16.1
```
**KALIMANTAN-SELATAN**
```
auto lo
iface lo inet loopback

#A12
auto eth0
iface eth0 inet static
address 10.78.21.178
netmask 255.255.255.252
gateway 10.78.21.178

#A14
auto eth1
iface eth1 inet static
address 10.78.21.97
netmask 255.255.255.224

#A15
auto eth2
iface eth2 inet static
address 10.78.8.1
netmask 255.255.248.0
```
**Angsana**
```
#A14
auto eth0
iface eth0 inet static
address 10.78.21.98
netmask  255.255.255.224
gateway 10.78.21.97
```
**Bajuin**
```
#A15
auto eth0
iface eth0 inet static
address 10.78.8.2
netmask 255.255.248.0
gateway 10.78.8.1
```
**Takisung**
```
#A15
auto eth0
iface eth0 inet static
address 10.78.8.3
netmask 255.255.248.0
gateway 10.78.8.1
```
**Batakan**
```
#A15
auto eth0
iface eth0 inet static
address 10.78.8.4
netmask 255.255.248.0
gateway 10.78.8.1
```
**LAMPUNG**
```
auto lo
iface lo inet loopback

#A16
auto eth0
iface eth0 inet static
address 10.78.21.206
netmask 255.255.255.252
gateway 10.78.21.205

#A17
auto eth1
iface eth1 inet static
address 10.78.19.1 
netmask 255.255.255.0
```
**Sebuku**
```
#A17
auto eth0
iface eth0 inet static
address 10.78.19.2 
netmask 255.255.255.0
gateway 10.78.19.1
```
**Sebesi**
```
#A17
auto eth0
iface eth0 inet static
address 10.78.19.3 
netmask 255.255.255.0
gateway 10.78.19.1
```
**Samosir**
```
#A18
auto eth0
iface eth0 inet static
address 10.78.21.66
netmask 255.255.255.224
gateway 10.78.21.65
```
**Sibandang**
```
#A18
auto eth0
iface eth0 inet static
address 10.78.21.67
netmask 255.255.255.224
gateway 10.78.21.65
```
**SUMATERA-UTARA**
```
auto lo
iface lo inet loopback

#A18
auto eth0
iface eth0 inet static
address 10.78.21.68
netmask 255.255.255.224
gateway 10.78.21.65

#19
auto eth1
iface eth1 inet static
address 10.78.21.185
netmask 255.255.255.252
```
**ACEH**
```
auto lo
iface lo inet loopback

#19
auto eth0
iface eth0 inet static
address 10.78.21.186
netmask 255.255.255.252
gateway 10.78.21.185

#20
auto eth1
iface eth1 inet static
address 10.78.20.129 
netmask 255.255.255.128

#21
auto eth2
iface eth2 inet static
address 10.78.21.129
netmask 255.255.255.224
```
**Starland**
```
auto eth0
iface eth0 inet static
address 10.78.20.132
netmask 255.255.255.128
gateway 10.78.20.129
```
**Enang-Enang**
```
auto eth0
iface eth0 inet static
address 10.78.20.131 
netmask 255.255.255.128
gateway 10.78.20.129
```
**Berawanng-Tampu**
```
auto eth0
iface eth0 inet static
address 10.78.20.130 
netmask 255.255.255.128
gateway 10.78.20.129
```
**Sabang**
```
auto eth0
iface eth0 inet static
address 10.78.21.130
netmask 255.255.255.224
gateway 10.78.21.129
```
**Lambaro**
```
auto eth0
iface eth0 inet static
address 10.78.21.131
netmask 255.255.255.224
gateway 10.78.21.129
```

## Routing
Routing yang dilakukan hanya pada Sulawesi dikarenakan routing pada Kalimantan dan Sumatera tidak berhasil. Alhasil, node hanya dapat melakukan ping antar sesama node di area(A1-A21) yang sama. Sementara pada Sulawesi, node yang berbeda area berhasil melakukan ping satu sama lain, bukan hanya pada area yang sama saja. Akan tetapi, node dari Sulawesi tidak bisa melakukan ping terhadap node di Kalimantan dan Sumatera.<br>
**JAWA**
```
route add -net 10.78.20.0 netmask 255.255.255.128 gw 10.78.21.190
route add -net 10.78.0.0 netmask 255.255.248.0 gw 10.78.21.190
route add -net 10.78.21.160 netmask 255.255.255.248 gw 10.78.21.190
route add -net 10.78.21.168 netmask 255.255.255.248 gw 10.78.21.190
route add -net 10.78.21.0 netmask 255.255.255.192 gw 10.78.21.190

#KALIMANTAN
route add -net 10.78.21.200 netmask 255.255.255.252 gw 10.78.21.194
route add -net 10.78.18.0 netmask 255.255.255.0 gw 10.78.21.194
route add -net 10.78.21.180 netmask 255.255.255.252 gw 10.78.21.194
route add -net 10.78.21.176 netmask 255.255.255.252 gw 10.78.21.194
route add -net 10.78.16.0 netmask 255.255.254.0 gw 10.78.21.194
route add -net 10.78.21.96 netmask 255.255.255.224 gw 10.78.21.194
route add -net 10.78.8.0 netmask 255.255.248.0 gw 10.78.21.194

#SUMATERA
route add -net 10.78.21.204 netmask 255.255.255.252 gw 10.78.21.198
route add -net 10.78.19.0 netmask 255.255.255.0 gw 10.78.21.198
route add -net 10.78.21.64 netmask 255.255.255.224 gw 10.78.21.198
route add -net 10.78.21.184 netmask 255.255.255.252 gw 10.78.21.198
route add -net 10.78.20.128 netmask 255.255.255.128 gw 10.78.21.198
route add -net 10.78.21.128 netmask 255.255.255.224 gw 10.78.21.198
```
**SULAWESI**
```
#Maluku-Utara
route add -net 10.78.0.0 netmask 255.255.248.0 gw 10.78.20.4

#Makassar
route add -net 10.78.21.168 netmask 255.255.255.248 gw 10.78.21.162

#Belawa
route add -net 10.78.21.0 netmask 255.255.255.192 gw 10.78.21.163
```
**MALUKU-UTARA**
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.173.21.190
```
**BELAWA**
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.173.21.190
```
**MAKASSAR**
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.173.21.190
```


# CIDR - CPT

Untuk metode CIDR atau Classless Inter-Domain Routing akan direpresentasikan dengan tools Cisco Packet Tracker.

## Penggabungan Subnet

### Step 1.
![b](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/58eaa1ad-2262-481e-96af-36dc01432d40)

### Step 2. 
![c](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/d05a4934-a744-46de-85c4-3a979cea881f)

### Step 3.
![d](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/94a0453b-7cc8-41db-b400-ffbc9ed199a7)

### Step 4.
![e](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/68e4f1de-bf51-424b-8824-8fd1d34a5d3d)

### Step 5.
![f](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/a66cfabe-521b-42f8-93ce-e4ebe1638f39)

### Step 6.
![g](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/2a7a0e07-aace-41ff-afe7-9bbb067d4c55)

# Step 7.
![h](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/04472312-b207-4373-a61d-c234b431eac1)

### Tree CIDR
![Decision tree(2)](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/dd350f94-4da1-4ea2-bffd-fac2a8ff14a5)

### Pembagian IP
![image](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/9b5ab558-6911-431e-b605-59caddb8c937)

### Konfigurasi CPT

Konfigurasi subnet dapat dilakukan dengan membuka menu router yang akan dikonfigurasi, untuk contoh berikut adalah konfigurasi router `Jawa` dan `Sulawesi`
   ![image](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/1cbc8a24-f903-4a13-9635-05302584a23f)
   
1. Buka menu router dan pindah pada tab konfig, kemudian masuk pada interface yang digunakan pada subnet tersebut, case ini adalah eth1/1. Kemudian isi IP Address dan subnet mask yang sesuai, untuk `Jawa` karena adalah host pertama dalam subnet, maka ip addressnya adalah network id (NID) dengan bit ke 4nya ditambahkan 1 yaitu `10.78.28.1`. Dan subnet masknya disesuaikan dengan subnetnya, karena subnet antara `Jawa` dan `Sulawesi` adalah /30, maka subnet masknya adalah `255.255.255.252`. Seperti berikut contoh pengisiannya:
  ![image](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/0c9365b7-383b-44a8-a34b-17fc256f7a8b)

2. Kemudian lakukan hal yang sama di `Sulawesi`, bedanya di interface yang digunakan yaitu eth0/0. Untuk IP Addressnya tambahkan 1 pada nilai bit 4 dari IP Address `Jawa`, yaitu `10.78.28.2`
   ![image](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/a1ca6610-09c9-4053-8118-c944133fe7dd)

Terakhir lakukan hal tersebut pada router di setiap subnet.

### Routing CPT

1. Buka menu router, kemudian masuk pada tab konfig dan pilih routing->static. Di sini akan dilakukan routing pada `Jawa` dan `Kalimantan-Utara`. Seperti di bawah:
  ![image](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/ce2bb3db-021a-4154-b9f3-78cc3aaba791)

2. Kemudian isi network id (NID) dan mask subnet yang dituju. Untuk Next Hop akan diisi dengan router terdekat yang akan digunakan sebagai 'jembatan' lalu lintas antara router `Jawa` dan `Kalimantan-Utara` atau antara subnet A2 dengan A9, oleh karena itu kolom next hop akan diisi dengan ip address dari Kalimantan pada interface yang tehubung pada subnet A2, yaitu `10.78.42.2`.
   ![image](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/9d0fabaa-d308-4355-a703-02cd51450d51)
   Kalau sudah tekan tombol Add.

3. Tidak lupa lakukan konfigurasi static routing di router `Kalimantan` yang menjadi jembatan tadi. Isi kolom-kolomnya sebagai berikut:
  ![image](https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/6599d731-a044-409c-84de-ea729757151f)
   Untuk NID dan Subnet masknya, digunakan 0.0.0.0 untuk menunjukkan bahwa rute ini berlaku untuk semua jaringan. Dalam hal ini, network ID 0.0.0.0 adalah cara untuk mengatakan "semua jaringan". Dan Mask menunjukkan bahwa      tidak ada bit dari alamat IP tujuan yang perlu dicocokkan. Mask 0.0.0.0 berarti semua bit dari alamat IP tujuan diabaikan untuk pencocokan rute.

#### Hasil Routing
https://github.com/J0see1/Jarkom-Modul-4-IT29/assets/134209563/06a348d9-cc96-416f-8f4f-551b746dff87



