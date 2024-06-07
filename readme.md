# Praktikum-Jarkom-Modul-4

# Anggota

| Nama                            | NRP          |
| ------------------------------- | ------------ |
| Marcelinus Alvinanda Chrisantya | `5027221012` |
| Bintang Ryan Wardana            | `5027221022` |

# Topologi 

# Rute Subnet


# VLSM - GN3

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



