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
