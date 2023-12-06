# Modul 4 Jarkom IT25

### Anggota :

- ANDYANA MUHANDHATUL NABILA - 5027211029
- ANDREAS TIMOTIUS PARHORASAN SIHOMBING - 5027211019

Dalam mengerjakan praktikum modul 4 ini hal pertama yang saya lakukan adalah pembagian subneting nya berikut gambar saya ini untuk metode VLSM

[![Whats-App-Image-2023-12-06-at-16-33-33-ce64bf9d.jpg](https://i.postimg.cc/Y9dzsnZk/Whats-App-Image-2023-12-06-at-16-33-33-ce64bf9d.jpg)](https://postimg.cc/8JrvFHTn)

Kemudian setelah ditentukan pembagian subnetnya saya buat tabel yang berisi nama subnet dengan saya masukan kebutuhan jumlah IP dan menentukan netmasknya dengan tabel netmask dari hasil IP yang dibutuhkan tadi. 
Berikut adalah tabelnya : 

| Nama Subnet                                    | Rute                                               | Jumlah IP | Jumlah IP Unik | Netmask |
|-------------------------------------------------|-----------------------------------------------------|-----------|----------------|---------|
| A1                                              | Aura-Cloud0                                         | 2         | 2              | /30     |
| A2                                              | Aura-Denken                                         | 2         | 2              | /30     |
| A3                                              | Aura-Frieren                                        | 2         | 2              | /30     |
| A4                                              | Aura-Eisen                                          | 2         | 2              | /30     |
| A5                                              | Frieren-Switch3-LakeKorridor                       | 25        | 25             | /27     |
| A6                                              | Denken-Switch2-WiliRegion-Switch2-RoyalCapital     | 127       | 127            | /24     |
| A7                                              | Eisen-Switch0-Stark                                | 2         | 2              | /30     |
| A8                                              | Eisen-Lugner                                       | 2         | 2              | /30     |
| A9                                              | Eisen-Linie                                        | 2         | 2              | /30     |
| A10                                             | Eisen-Switch1-Richter-Switch1-Revolte              | 3         | 3              | /29     |
| A11                                             | Lugner-Switch10-TurkRegion                         | 1001      | 1001           | /22     |
| A12                                             | Lugner-Switch9-GrobeForest                         | 251       | 251            | /24     |
| A13                                             | Linie-Switch11-GranzChannel                        | 255       | 255            | /23     |
| A14                                             | Linie-Lawine                                       | 2         | 2              | /30     |
| A15                                             | Lawine-Switch7-BredtRegion-switch7-Heiter          | 31        | 31             | /26     |
| A16                                             | Heiter-Switch8-RiegelCanyon-Switch8-Sein          | 512       | 512            | /22     |
| A17                                             | Frieren-Flamme                                     | 2         | 2              | /30     |
| A18                                             | Flamme-fern                                        | 2         | 2              | /30     |
| A19                                             | Flamme-Switch5-RohrRoad                            | 1001      | 1001           | /22     |
| A20                                             | Flamme-Himmel                                      | 2         | 2              | /30     |
| A21                                             | Himmel-Switch6-SchwerMountains                     | 6         | 6              | /29     |
| A22                                             | Fern-Switch4-LaubHills-Switch4-AppetitRegion       | 1023      | 1023           | /21     |
| **Total**                                       |                                                   | **4257**  |                | **/19** |


Setelah diketahui hal-hal yang ada pada tabel diatas, lalu untuk metode vlsm dilakukan sorting dengan host terbanyak, lakukan gunakan perhitungan gunakan 2^n, yuntuk ip pertama adalah network id dan ip terakhir adalah broadcast id

| Subnet | Network ID      | Netmask              | Broadcast        |
|--------|-----------------|----------------------|------------------|
| A22    | 10.76.0.0       | 255.255.248.0        | 10.76.7.255      |
| A11    | 10.76.8.0       | 255.255.252.0        | 10.76.11.255     |
| A19    | 10.76.12.0      | 255.255.252.0        | 10.76.15.255     |
| A16    | 10.76.16.0      | 255.255.252.0        | 10.76.19.255     |
| A13    | 10.76.20.0      | 255.255.254.0        | 10.76.21.255     |
| A12    | 10.76.22.0      | 255.255.255.0        | 10.76.22.255     |
| A6     | 10.76.23.0      | 255.255.255.0        | 10.76.23.255     |
| A15    | 10.76.24.0      | 255.255.255.192      | 10.76.24.63      |
| A5     | 10.76.24.64     | 255.255.255.224      | 10.76.24.95      |
| A21    | 10.76.24.96     | 255.255.255.248      | 10.76.24.103     |
| A10    | 10.76.24.104    | 255.255.255.248      | 10.76.24.111     |
| A1     | 10.76.24.112    | 255.255.255.252      | 10.76.24.115     |
| A2     | 10.76.24.116    | 255.255.255.252      | 10.76.24.119     |
| A3     | 10.76.24.120    | 255.255.255.252      | 10.76.24.123     |
| A4     | 10.76.24.124    | 255.255.255.252      | 10.76.24.127     |
| A7     | 10.76.24.128    | 255.255.255.252      | 10.76.24.131     |
| A8     | 10.76.24.132    | 255.255.255.252      | 10.76.24.135     |
| A9     | 10.76.24.136    | 255.255.255.252      | 10.76.24.139     |
| A14    | 10.76.24.140    | 255.255.255.252      | 10.76.24.143     |
| A17    | 10.76.24.144    | 255.255.255.252      | 10.76.24.147     |
| A18    | 10.76.24.148    | 255.255.255.252      | 10.76.24.151     |
| A20    | 10.76.24.152    | 255.255.255.252      | 10.76.24.155     |


Kemudian saya mengset pemasangan IP pada GNS 3 menggunakan IP diatas yang telah didapatkan sebelumnya. Setelah topologi dibuat maka selanjutnya adalah melakukan routing dengan code dibawah ini : 

```
#Aura
route add -net 10.76.23.0 netmask 255.255.255.0 gw 10.76.24.118
route add -net 10.76.24.128 netmask 255.255.255.252 gw 10.76.24.126
route add -net 10.76.8.0 netmask 255.255.252.0 gw 10.76.24.126
route add -net 10.76.22.0 netmask 255.255.255.0 gw 10.76.24.126
route add -net 10.76.24.104 netmask 255.255.255.248 gw 10.76.24.126
route add -net 10.76.20.0 netmask 255.255.254.0 gw 10.76.24.126
route add -net 10.76.24.0 netmask 255.255.255.192 gw 10.76.24.126
route add -net 10.76.16.0 netmask 255.255.252.0 gw 10.76.24.126
route add -net 10.76.24.64 netmask 255.255.255.224 gw 10.76.24.122
route add -net 10.76.12.0 netmask 255.255.252.0 gw 10.76.24.122 
route add -net 10.76.0.0 netmask 255.255.248.0 gw 10.76.24.122 
<!-- -- >>>> route del -net 10.76.24.96 netmask 255.255.255.248 gw 10.76.24.122 -->

#Denken
route add -net 10.76.24.116 netmask 255.255.255.252 gw 10.76.24.117 

#Eisen
route add -net 10.76.24.124 netmask 255.255.255.252 gw 10.76.24.125 
route add -net 10.76.8.0 netmask 255.255.252.0 gw 10.76.24.134
route add -net 10.76.22.0 netmask 255.255.255.0 gw 10.76.24.134
route add -net 10.76.20.0 netmask 255.255.254.0 gw 10.76.24.138
route add -net 10.76.24.0 netmask 255.255.255.192 gw 10.76.24.138
route add -net 10.76.16.0 netmask 255.255.252.0 gw 10.76.24.138

#Lugner
route add -net 10.76.24.132 netmask 255.255.255.252 gw 10.76.24.133

#Linie
route add -net 10.76.24.136 netmask 255.255.255.252 gw 10.76.24.137
route add -net 10.76.24.0 netmask 255.255.255.192 gw 10.76.24.142
route add -net 10.76.16.0 netmask 255.255.252.0 gw 10.76.24.142

#Lawine
route add -net 10.76.24.140 netmask 255.255.255.252 gw 10.76.24.141 
route add -net 10.76.16.0 netmask 255.255.252.0 gw 10.76.24.2

#Heiter
route add -net 10.76.24.0 netmask 255.255.255.192 gw 10.76.24.1 

#Frieren
route add -net  10.76.24.120 netmask 255.255.255.252 gw 10.76.24.121
route add -net 10.76.12.0 netmask 255.255.252.0 gw 10.76.24.146 
route add -net 10.76.0.0 netmask 255.255.248.0 gw 10.76.24.146
<!-- -- >>>> route del -net 10.76.24.96 netmask 255.255.255.248 gw 10.76.24.146 -->

#Fern 
route add -net 10.76.24.148 netmask 255.255.255.252 gw 10.76.24.149 

#Flamme
route add -net 10.76.24.144 netmask 255.255.255.252 gw 10.76.24.145 
route add -net 10.76.0.0 netmask 255.255.248.0 gw 10.76.24.150
<!-- -- >>>> route del -net 10.76.24.96 netmask 255.255.255.248 gw 10.76.24.154 -->

#Himmel
route add -net 10.76.24.152 netmask 255.255.255.248 gw 10.76.24.153 

# IP
1. Denken - 10.76.24.118
2. RoyalCapital - 10.76.23.2
3. Wilie Region - 10.76.23.123
4. Eisen - 10.76.24.126
5. Server PT Stark - 10.76.24.130
6. Lugner - 10.76.24.134
7. PC-PTTurkRegion - 10.76.8.2
8. PC-PTGrobeForest - 10.76.22.2
9. PT-Richter - 10.76.24.106
10. PTRevolte - 10.76.24.107
11. Linie - 10.76.24.138
12. PTGranzChannel - 10.76.20.2
13. Lawine - 10.76.24.142
14. Heiter - 10.76.24.2
16. Riegel Canyon - 10.76.16.3
17. PTSein - 10.76.16.2
18. Frieren - 10.76.24.122
19. Flamme - 10.76.24.146
20. Fern - 10.76.24.150
21. PTLaubHills - 10.76.0.2
22. PTAppetitRegion - 10.76.0.3
23. PTRohrRoar - 10.76.12.2
24. Himmel - 10.76.24.154
25. PTSchwerMountain - 10.76.24.98
```



## CIDR

### Rute
Rute yang digunakan VLSM dan CIDR sedikit beda, gambar dibawah ini adalah rute yang kita pakai pada perhitungan cidr
![1](https://github.com/chocoricano/Jarkom-Modul-4-IT25-2023/assets/56831859/08223c3b-4dc7-4036-8a10-4c316f660355)


### Hitungan
perhitungan CIDR berbeda dengan VLSM, CIDR menggabungkan rute kejauh hingga semua menjadi satu kesataun

| i | Subnet | 1             | Netmask | 2             | Netmask | Netmask Akhir |
|---|--------|---------------|---------|---------------|---------|---------------|
| I |        |               |         |               |         |               |
|   | B1     | A1            | /29     | A2            | /30     | /28           |
|   | B2     | A4            | /21     | A5            | /30     | /20           |
|   | B3     | A13           | /26     | A14           | /22     | /21           |
|   | B4     | A15           | /23     | A12           | /30     | /22           |
| II|        |               |         |               |         |               |
|   | C1     | B1            | /28     | A3            | /22     | /21           |
|   | C2     | B2            | /20     | A6            | /30     | /19           |
|   | C3     | B3            | /21     | B4            | /22     | /20           |
|   | C4     | A18           | /22     | A19           | /24     | /21           |
| III|       |               |         |               |         |               |
|   | D1     | C1            | /21     | C2            | /19     | /18           |
|   | D2     | C3            | /20     | A11           | /30     | /19           |
|   | D3     | C4            | /21     | A17           | /30     | /20           |
| IV|        |               |         |               |         |               |
|   | E1     | D1            | /18     | A7            | /27     | /17           |
|   | E2     | D2            | /19     | A10           | /29     | /18           |
|   | E3     | D3            | /20     | A16           | /30     | /18           |
| V |        |               |         |               |         |               |
|   | F1     | E1            | /17     | A8            | /30     | /16           |
|   | F2     | E2            | /18     | E3            | /18     | /17           |
|   | F3     | A21           | /24     | A20           | /30     | /23           |
| VI|        |               |         |               |         |               |
|   | G1     | F1            | /16     | F3            | /23     | /15           |
|   | G2     | F2            | /18     | A9            | /30     | /16           |
| VII|       |               |         |               |         |               |
|   | H1     | G1            | /15     | G2            | /16     | /14           |

Maka akan menghasilkan network id, netmask, broadcast menjadi seperti ini

| Subnet | Network ID        | Netmask             | Broadcast          |
|--------|-------------------|---------------------|--------------------|
| A1     | 10.76.0.0         | 255.255.255.248     | 10.76.0.7          |
| A2     | 10.76.8.0         | 255.255.255.252     | 10.76.8.3          |
| A3     | 10.76.16.0        | 255.255.252.0       | 10.76.19.255       |
| A4     | 10.76.32.0        | 255.255.248.0       | 10.76.39.255       |
| A5     | 10.76.40.0        | 255.255.255.252     | 10.76.40.3         |
| A6     | 10.76.48.0        | 255.255.255.252     | 10.76.48.3         |
| A7     | 10.76.64.0        | 255.255.255.224     | 10.76.64.31        |
| A8     | 10.76.128.0       | 255.255.255.252     | 10.76.128.3        |
| A9     | 10.79.0.0         | 255.255.255.252     | 10.79.0.3          |
| A10    | 10.78.64.0        | 255.255.255.248     | 10.78.64.7         |
| A11    | 10.78.32.0        | 255.255.255.252     | 10.78.32.3         |
| A12    | 10.78.24.0        | 255.255.255.252     | 10.78.24.3         |
| A13    | 10.78.0.0         | 255.255.255.192     | 10.78.0.63         |
| A14    | 10.78.8.0         | 255.255.252.0       | 10.78.11.255       |
| A15    | 10.78.16.0        | 255.255.254.0       | 10.78.17.255       |
| A16    | 10.78.192.0       | 255.255.255.252     | 10.78.192.3        |
| A17    | 10.78.160.0       | 255.255.255.252     | 10.78.160.3        |
| A18    | 10.78.128.0       | 255.255.252.0       | 10.78.131.255      |
| A19    | 10.78.144.0       | 255.255.255.0       | 10.78.144.255      |
| A20    | 10.77.128.0       | 255.255.255.252     | 10.77.128.3        |
| A21    | 10.77.0.0         | 255.255.255.0       | 10.77.0.255        |


### Routing
Untuk Routing ada sedikit masalah pada cisco packet trackernya jadi tidak bisa dilakukan routing
