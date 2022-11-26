# Jarkom-Modul-3-E12-2022

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
| A2	| The Minister - The Daundless	| 2	| /30 |
| A3	| The Daundless - Phanora - Johan	| 251	| /24 |
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
| A2 | The Daundless | 192.198.0.6 | 255.255.255.252 | |
| A3 | The Daundless | 192.198.1.1 | 255.255.255.0 | /24 |
| A3 | Phanora | 192.198.1.2 | 255.255.255.0 | |
| A3 | Johan | 192.198.1.3 | 255.255.255.0 | |
| A4 | The Minister | 192.198.0.9 | 255.255.255.252 | /30 |
| A4 | The Order | 192.198.0.10 | 255.255.255.252 | |
| A5 | The Order | 192.198.0.65 | 255.255.255.192 | /26 |
| A5 | Ashaf | 192.198.0.66 | 255.255.255.192 | |
| A6 | The Order | 192.198.0.13 | 255.255.255.252 | /30 |
| A6 | The Resonance | 192.198.0.14 | 255.255.255.252 | |
| A7 | The Resonance | 192.198.0.17 | 255.255.255.252 | /30 |
| A7 | TheInstrument | 192.198.0.18 | 255.255.255.252 | |
