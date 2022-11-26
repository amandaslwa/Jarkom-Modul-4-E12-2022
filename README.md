# Jarkom-Modul-4-E12-2022

Kelas Jaringan Komputer E - Kelompok E12
### Nama Anggota
- Amanda Salwa Salsabila        (5025201172)
- Michael Ariel Manihuruk       (5025201158)
- Azzura Mahendra Putra Malinus (5025201211)

## VLSM (Variable Length Subnet Masking)
<img width="599" alt="image" src="https://user-images.githubusercontent.com/90702710/204082245-eb807e55-3afe-4279-a2be-285dd341c4e7.png">

Menentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan melabel netmask berdasarkan jumlah IP yang dibutuhkan.

| Subnet | Alias | Jumlah IP | Netmask |
| --- | --- | --- | --- |
| A1	| Guideau - The Minister	| 1001	| /22 |
| A2	| The Minister - The Dauntless	| 2	| /30 |
| A3	| The Dauntless - Phanora - Johan	| 251	| /24 |
| A4	| The Minister - The Order	| 2	| /30 |
| A5	| The Order - Ashaf	| 51	| /26 |
| A6	| The Order - The Resonance	| 2	| /30 |
| A7	| The Resonance - The Instrument	| 2	| /30 |
| A8	| The Instrument - Matt Cugat	| 121	| /25 |
| A9	| The Instrument - The Firefist	| 2	| /30 |
| A10	| The Firefist - Keith - The Queen	| 212	| /24 |
| A11	| The Firefist - Oakleave	| 501	| /23 |
| A12	| The Resonance - The Magical	| 2	| /30 |
| A13	| The Magical - Haines - Corvekt	| 271	| /23
| A14	| The Instrument - The Profound	| 2	| /30 |
| A15	| The Profound - Spendrow	| 121	| /25 |
| A16	| The Profound - Helga	| 71	| /25 |
| A17	| The Resonance - The Beast	| 2	| /30 |
| A18	| The Queen - The Witch	| 2	| /30 |
| Total |		| 2618 |	/20 |

### Pohon IP

Subnet besar yang dibentuk memiliki NID 192.198.0.0 dengan netmask /20 sehingga pembagian IP berdasarkan NID dan netmask dihitung sesuai dengan pohon berikut.

<img width="852" alt="image" src="https://user-images.githubusercontent.com/90702710/204082554-8357cdc7-a672-4782-b8a8-cdb0f6e705ed.png">

Pada VLSM, IP diturunkan sesuai dengan length atasnya. Pembagian IPnya mengikuti tabel. Jika ada subnet yang bisa digunakan, maka subnet langsung digunakan. Hal ini dilakukan berulang sampai semua subnet digunakan.

### Pembagian IP

Pembagian IP tiap node disesuaikan dengan pembagian subnet berdasarkan pohon di atas pada topologi.

| Subnet | Node | IP | Subnet Mask | Length |
| --- | --- | --- | --- | --- |
| A1 | The Minister | 192.198.12.1 | 255.255.252.0 | /22 |
| A1 | Guideau | 192.198.12.2 | 255.255.252.0 | |
| A2 | The Minister | 192.198.0.5 | 255.255.255.252 | /30 |
| A2 | The Dauntless | 192.198.0.6 | 255.255.255.252 | |
| A3 | The Dauntless | 192.198.1.1 | 255.255.255.0 | /24 |
| A3 | Phanora | 192.198.1.2 | 255.255.255.0 | |
| A3 | Johan | 192.198.1.3 | 255.255.255.0 | |
| A4 | The Minister | 192.198.0.9 | 255.255.255.252 | /30 |
| A4 | The Order | 192.198.0.10 | 255.255.255.252 | |
| A5 | The Order | 192.198.0.65 | 255.255.255.192 | /26 |
| A5 | Ashaf | 192.198.0.66 | 255.255.255.192 | |
| A6 | The Order | 192.198.0.13 | 255.255.255.252 | /30 |
| A6 | The Resonance | 192.198.0.14 | 255.255.255.252 | |
| A7 | The Resonance | 192.198.0.17 | 255.255.255.252 | /30 |
| A7 | The Instrument | 192.198.0.18 | 255.255.255.252 | |
| A8 | The Instrument | 192.198.0.129 | 255.255.255.128 | /25 |
| A8 | Matt Cugat | 192.198.0.130 | 255.255.255.128 | |
| A9 | The Instrument | 192.198.0.21 | 255.255.255.252 | /30 |
| A9 | The Firefist | 192.198.0.22 | 255.255.255.252 | |
| A10 | The Firefist | 192.198.5.1 | 255.255.255.0 | /24 |
| A10 | The Queen | 192.198.5.2 | 255.255.255.0 | |
| A10 | Keith | 192.198.5.3 | 255.255.255.0 | |
| A11 | The Firefist | 192.198.6.1 | 255.255.254.0 | /23 |
| A11 | Oakleave | 192.198.6.2 | 255.255.254.0 | |
| A12 | The Resonance | 192.198.0.25 | 255.255.255.252 | /30 |
| A12 | The Magical | 192.198.0.26 | 255.255.255.252 | |
| A13 | The Magical | 192.198.2.1 | 255.255.254.0 | /23 |
| A13 | Haines | 192.198.2.2 | 255.255.254.0 | |
| A13 | Corvekt | 192.198.2.3 | 255.255.254.0 | |
| A14 | The Instrument | 192.198.0.29 | 255.255.255.252 | /30 |
| A14 | The Profound | 192.198.0.30 | 255.255.255.252 | |
| A15 | The Profound | 192.198.4.1 | 255.255.255.128 | /25 |
| A15 | Spendrow | 192.198.4.2 | 255.255.255.128 | |
| A16 | The Profound | 192.198.4.129 | 255.255.255.128 | /25 |
| A16 | Helga | 192.198.4.130 | 255.255.255.128 | |
| A17 | The Resonance | 192.198.0.33 | 255.255.255.252 | /30 |
| A17 | The Beast | 192.198.0.34 | 255.255.255.252 | |
| A18 | The Queen | 192.198.0.37 | 255.255.255.252 | /30 |
| A18 | The Witch | 192.198.0.38 | 255.255.255.252 | |

### Assignment

Contoh pada The Resonance, IP dan Subnet Mask ditambahkan sesuai dengan pembagian yang telah dilakukan, dengan IP ditambah 1 dari subnetnya. Hal ini diassign untuk semua router, client dan server.

<img width="352" alt="image" src="https://user-images.githubusercontent.com/90702710/204084042-b1ae7427-6a8d-4bfb-b15f-bab88d0aa84a.png">

Pada server & client ditambahkan juga gateway yang mengarah ke router terdekat.

<img width="352" alt="image" src="https://user-images.githubusercontent.com/90702710/204084067-b58c53b4-e7b5-44ce-b3ec-55157159f6ac.png">

### Menambah Ethernet

Karena default hanya memiliki 2 port ethernet, maka port dapat ditambah pada tab physical sesuai dengan jumlah yang dibutuhkan. Misal pada The Instrument, dibutuhkan 2 port tambahan karena total cabang yang terkoneksi ada 4.

<img width="352" alt="image" src="https://user-images.githubusercontent.com/90702710/204084122-46805685-01d3-4d23-9552-100870a06913.png">

### Routing

Berikut adalah konfigurasi yang telah diset pada masing-masing router.
- The Resonance
<img width="247" alt="image" src="https://user-images.githubusercontent.com/90702710/204092928-40d1a6b0-c385-4de9-8601-02bdb4d5add4.png">

<img width="247" alt="image" src="https://user-images.githubusercontent.com/90702710/204092946-29034362-c61a-4e76-974d-6746004a16d6.png">

<img width="248" alt="image" src="https://user-images.githubusercontent.com/90702710/204093064-2a8435f0-2057-4f9e-85e4-2c03a5405cf6.png">

<img width="248" alt="image" src="https://user-images.githubusercontent.com/90702710/204093073-308f0ecf-4b3c-4867-a83c-723e0312f0ff.png">

<img width="247" alt="image" src="https://user-images.githubusercontent.com/90702710/204093606-29798699-a68a-4dea-af56-8a6b0940e472.png">

- The Order
<img width="248" alt="image" src="https://user-images.githubusercontent.com/90702710/204093118-5360f67b-a348-4142-b397-c78e58b7874e.png">

<img width="248" alt="image" src="https://user-images.githubusercontent.com/90702710/204093130-631cc6ae-79ee-4d01-acac-8b7b390327ca.png">

- The Minister
<img width="247" alt="image" src="https://user-images.githubusercontent.com/90702710/204084410-c26b1e71-2a9f-4143-aae5-2980a6cd7704.png">

- The Dauntless
<img width="247" alt="image" src="https://user-images.githubusercontent.com/90702710/204084422-0229838c-6e91-4a64-bdfb-e1b7a2a1879d.png">

- The Instrument
<img width="248" alt="image" src="https://user-images.githubusercontent.com/90702710/204093151-770ea23e-785b-4dda-b42b-1fa96985b996.png">

<img width="247" alt="image" src="https://user-images.githubusercontent.com/90702710/204093157-538575e3-3d9f-48e8-a417-d7a5d0ca86fd.png">

- The Profound
<img width="249" alt="image" src="https://user-images.githubusercontent.com/90702710/204084522-13a2054e-7ecc-474d-b864-bbb3ff14304f.png">

- The Firefist
<img width="248" alt="image" src="https://user-images.githubusercontent.com/90702710/204084537-87698878-4b44-4b59-b32c-bf8aa447662b.png">

- The Queen
<img width="248" alt="image" src="https://user-images.githubusercontent.com/90702710/204084549-8c9c38f6-a765-47f4-a620-68e0a16eee65.png">

- The Magical
<img width="248" alt="image" src="https://user-images.githubusercontent.com/90702710/204084565-1e81ff0d-50b6-4b88-874b-7ff34039799b.png">

### Testing

Untuk video testing pada CPT dapat dilihat pada drive: https://drive.google.com/file/d/1cPCdrfRzm2IEJ6wk8gXkMSUUpe1OKVcx/view?usp=share_link

## CIDR (Classless Inter-Domain Routing)
Menentukan jumlah alamat IP yang dibutuhkan oleh tiap subnet dan melabel netmask berdasarkan jumlah IP yang dibutuhkan.

![image](https://user-images.githubusercontent.com/82187488/204094033-3096b821-9c29-4dd1-8495-2b700808cbcb.png)

Menggabungkan dua subnet yang terjauh dari NAT. Pada kasus ini, terdapat empat gabungan subnet. Netmask dari subnet yang baru merupakan satu tingkat dari netmask terbesar dari dua subnet yang digabungkan. 

![image](https://user-images.githubusercontent.com/82187488/204094065-4e70e431-e4fb-40db-a025-fb7b90f8daaf.png)

Cara tersebut dilakukan hingga terbentuk satu subnet besar.

![image](https://user-images.githubusercontent.com/82187488/204094080-867fdad3-d45e-4013-9ddf-afd9d4769feb.png)

![image](https://user-images.githubusercontent.com/82187488/204094091-1e0ce2bb-8694-41b4-8247-1c9dc158ea4f.png)

![image](https://user-images.githubusercontent.com/82187488/204094107-b22589ad-b7a7-4e0d-ada4-1c1d95fd1f15.png)

![image](https://user-images.githubusercontent.com/82187488/204094126-40c47cfe-3ac8-413c-aa52-f74013c9e458.png)

![image](https://user-images.githubusercontent.com/82187488/204094140-5cda7253-76b4-43f4-b396-d08450512053.png)

![image](https://user-images.githubusercontent.com/82187488/204094154-7f8ec5a4-e110-4b7a-8ed1-6fc537411917.png)

![image](https://user-images.githubusercontent.com/82187488/204094172-27c5cf4f-9f72-4d83-a3f1-2c74edbbbb57.png)

Setelah itu, membuat pohon IP untuk membagi IP kepada subnet-subnet yang dibentuk di awal.

<img width="621" alt="image" src="https://user-images.githubusercontent.com/90702710/204095245-88ca69e6-2026-4a8b-8414-794aeeca3b7d.png">

Terdapat dua macam kasus dalam menentukan IP:

![image](https://user-images.githubusercontent.com/82187488/204094310-6fb7e828-d55f-4a1a-bc35-b550e856ae32.png)

Pada kasus tersebut, IP dari node di kiri merupakan total IP dari node di kanan ditambah satu.

![image](https://user-images.githubusercontent.com/82187488/204094323-b76d93fa-3c77-4598-9eb3-8becc288c6a7.png)

Pada kasus tersebut, IP dari node di kanan merupakan total dari IP dari node di kiri ditambah satu.

Jika tree sudah selesai dibuat, NID dari setiap subnet dapat ditentukan. Setelah itu, tabel IP dapat dibentuk.

![image](https://user-images.githubusercontent.com/82187488/204094420-e09d7a96-61ee-4da1-a916-177297f96cf2.png)

Setelah tabel IP dibuat, setiap node pada GNS3 diberikan IP sesuai dengan yang telah ditentukan di tabel IP.

Contoh konfigurasi pada sebuah subnet (A14) dengan mengikuti pembagian di tabel IP.

![image](https://user-images.githubusercontent.com/82187488/204094558-6b12c6d1-7bcf-4bb1-95fa-a72abb201d5d.png)

![image](https://user-images.githubusercontent.com/82187488/204094582-3cc54047-0e4b-411b-bb49-fc5591b23eb2.png)




