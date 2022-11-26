# Jarkom-Modul-4-D09-2022

## Anggota Kelompok D09
| No | Nama | NRP |
| ------ | ------ | ----- |
| 1 | Monica Narda Davita | 5025201009 |
| 2 | Alya Shofarizqi Inayah | 5025201113 |
| 3 | Meisya Salsabila Indrijo Putri | 5025201114 |

## Prefix IP
192.189.X.X

## CIDR GNS3
### Topologi GNS3
![topologiCIDR](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/TopologiGNS3.jpeg?raw=true)

### Topologi Cluster GNS3
![topologiA](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/ClusterA.png?raw=true)
![topologiB](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/ClusterB.png?raw=true)
![topologiC](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/ClusterC.png?raw=true)
![topologiD](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/ClusterD.png?raw=true)
![topologiE](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/ClusterE.png?raw=true)
![topologiF](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/ClusterF.png?raw=true)
![topologiG](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/ClusterG.png?raw=true)
![topologiH](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/ClusterH.png?raw=true)

Dari pengelompokan subnet tersebut didapatkan subnet terbesar memiliki 16 bit, sehingga pohon pembagian IP dapat dibuat menjadi sebagai berikut:

### Pohon IP CIDR
![pohonIPCIDR](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/CIDRTree.png?raw=true)

Setelah didapatkan IP pada setiap subnet paling bawah, maka dicari netmask dan broadcast pada setiap subnet tersebut. Hasilnya sebagai berikut:

### Tabel Netmask dan Broadcast ID
![NetmaskBroadcastCIDR](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/NetIDBroadcastCIDR.jpeg?raw=true)

### CIDR Routing - Setting Network Configuration
![NetworkConfigurationCIDR](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/NetworkConfCIDR.jpeg?raw=true)

**Konfigurasi: The Resonance**
```
auto eth0
iface eth0 inet dhcp

auto eth1
iface eth1 inet static
      address 192.189.32.1
      netmask 255.255.255.252

auto eth2
iface eth2 inet static
      address 192.189.146.1
      netmask 255.255.255.252

auto eth3
iface eth3 inet static
      address 192.189.160.1
      netmask 255.255.255.252

auto eth4
iface eth4 inet static
      address 192.189.64.1
      netmask 255.255.255.252
```

**Konfigurasi: The Order**
```
auto eth0
iface eth0 inet static
      address 192.189.32.2
      netmask 255.255.255.252
      gateway 192.189.32.1

auto eth1
iface eth1 inet static
      address 192.189.8.1
      netmask 255.255.255.252

auto eth2
iface eth2 inet static
      address 192.189.16.1
      netmask 255.255.255.192
```

**Konfigurasi: The Minister**
```
auto eth0
iface eth0 inet static
      address 192.189.8.2
      netmask 255.255.255.252
      gateway 192.189.8.1

auto eth1
iface eth1 inet static
      address 192.189.4.1
      netmask 255.255.252.0

auto eth2
iface eth2 inet static
      address 192.189.2.1
      netmask 255.255.255.252
```

**Konfigurasi: The Dauntless**
```
auto eth0
iface eth0 inet static
      address 192.189.2.2
      netmask 255.255.255.252
      gateway 192.189.2.1

auto eth1
iface eth1 inet static
      address 192.189.0.1
      netmask 255.255.255.0
```

**Konfigurasi: The Instrument**
```
auto eth0
iface eth0 inet static
      address 192.189.146.2
      netmask 255.255.255.252
      getaway 192.189.146.1

auto eth1
iface eth1 inet static
      address 192.189.136.1
      netmask 255.255.255.128

auto eth2
iface eth2 inet static
      address 192.189.136.1
      netmask 255.255.255.252

auto eth3
iface eth3 inet static
      address 192.189.145.1
      netmask 255.255.255.252
```

**Konfigurasi: The Profound**
```
auto eth0
iface eth0 inet static
      address 192.189.145.2
      netmask 255.255.255.252
      gateway 192.189.145.1

auto eth1
iface eth1 inet static
      address 192.189.144.1
      netmask 255.255.255.128

auto eth2
iface eth2 inet static
      address 192.189.144.129
      netmask 255.255.255.128
```

**Konfigurasi: The Firefist**
```
auto eth0
iface eth0 inet static
      address 192.189.136.2
      netmask 255.255.255.252
      gateway 192.189.136.1

auto eth1
iface eth1 inet static
      address 198.189.128.1
      netmask 255.255.255.0

auto eth2
iface eth2 inet static
      address 192.189.131.1
      netmask 255.255.254.0
```

**Konfigurasi: The Queen**
```
auto eth0
iface eth0 inet static
      address 198.189.128.2
      netmask 255.255.255.0
      gateway 198.189.128.1

auto eth1
iface eth1 inet static
      address 192.189.129.1
      netmask 255.255.255.252
```

### CIDR Routing - Setting Host Configuration
![ClientServerCIDR](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/ClientServerCIDR.jpeg?raw=true)

**Konfigurasi: Guideau (1000 Host)**
```
auto eth0
iface eth0 inet static
      address 192.189.4.2
      netmask 255.255.252.0
      gateway 192.189.4.1
```

**Konfigurasi: Phanora (150 Host)**
```
auto eth0
iface eth0 inet static
      address 192.189.0.2
      netmask 255.255.255.0
      gateway 192.189.0.1
```

**Konfigurasi: Johan (100 Host)**
```
auto eth0
iface eth0 inet static
      address 192.189.0.153
      netmask 255.255.255.0
      gateway 192.189.0.1
```

**Konfigurasi: Ashaf (50 Host)**
```
auto eth0
iface eth0 inet static
      address 192.189.16.2
      netmask 255.255.255.192
      gateway 192.189.16.1
```

**Konfigurasi: Matt Cugatt (120 Host)**
```
auto eth0
iface eth0 inet static
      address 192.189.136.2
      netmask 255.255.255.128
      gateway 192.189.136.1
```

**Konfigurasi: Keith (210 Host)**
```
auto eth0
iface eth0 inet static
      address 192.189.128.2
      netmask 255.255.255.0
      gateway 192.189.128.1
```

**Konfigurasi: Oakleave (500 Host)**
```
auto eth0
iface eth0 inet static
      address 192.189.131.2
      netmask 255.255.254.0
      gateway 192.189.131.1
```

**Konfigurasi: The Witch (Server)**
```
auto eth0
iface eth0 inet static
      address 192.189.129.2
      netmask 255.255.255.252
      gateway 192.189.129.2
```

**Konfigurasi: The Beast (Server)**
```
auto eth0
iface eth0 inet static
      address 192.189.64.2
      netmask 255.255.255.252
      gateway 192.189.64.1
```

**Konfigurasi: Haines (70 Host)**
```
auto eth0
iface eth0 inet static
      address 192.189.192.202
      netmask 255.255.254.0
      gateway 192.189.192.1
```
**Konfigurasi: Corvekt (200 Host)**\
```bash
auto eth0
iface eth0 inet static
      address 192.189.192.2
      netmask 255.255.254.0
      gateway 192.189.192.1
```

**Konfigurasi: Spendrow (120 Host)**
```
auto eth0
iface eth0 inet static
      address 192.189.144.2
      netmask 255.255.255.128
      gateway 192.189.144.1
```

**Konfigurasi: Helga (70 Host)**
```
auto eth0
iface eth0 inet static
      address 192.189.144.130
      netmask 255.255.255.128
      gateway 192.189.144.129
```

### CIDR Routing - Routing
**The Resonance**
```
route add -net 192.189.4.0 netmask 255.255.252.0 gw 192.189.32.2        #A1 Guideau
route add -net 192.189.8.0 netmask 255.255.255.252 gw 192.189.32.2      #A4 The Order
route add -net 192.189.2.0 netmask 255.255.255.252 gw 192.189.32.2      #A2 The Dauntless
route add -net 192.189.0.0 netmask 255.255.255.0 gw 192.189.32.2        #A3 Phanora-Johan
route add -net 192.189.16.0 netmask 255.255.255.192 gw 192.189.32.2     #A5 Ashaf
route add -net 192.189.129.0 netmask 255.255.255.252 gw 192.189.146.2   #A9 The Queen
route add -net 192.189.131.0 netmask 255.255.254.0 gw 192.189.146.2     #A13 Oakleave
route add -net 192.189.128.0 netmask 255.255.255.0 gw 192.189.146.2     #A8 Keith
route add -net 192.189.144.128 netmask 255.255.255.128 gw 192.189.146.2 #A17 Helga
route add -net 192.189.144.0 netmask 255.255.255.128 gw 192.189.146.2   #A16 Spendrow
route add -net 192.189.145.0 netmask 255.255.255.252 gw 192.189.146.2   #A18 The Instrument
route add -net 192.189.136.0 netmask 255.255.255.128 gw 192.189.146.2   #A7 Matt Cugat
route add -net 192.189.192.0 netmask 255.255.254.0 gw 192.189.160.2     #A15 Corvekt
```

**The Order**
```
route add -net 192.189.4.0 netmask 255.255.252.0 gw 192.189.8.2         #A1 Guideai
route add -net 192.189.0.0 netmask 255.255.255.0 gw 192.189.8.2         #A3 Phanora-Johan
route add -net 192.189.2.0 netmask 255.255.255.252 gw 192.189.8.2       #A2 The Dauntless
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.189.32.1                  #default
```

**The Minister**
```
route add -net 192.189.0.0 netmask 255.255.255.0 gw 192.189.2.2         #A3 Johan-Phanora
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.189.8.1                   #default
```

**The Dauntless**
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.189.2.1                   #default
```

**The Magical**
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.189.160.1                 #default
```

**The Instrument**
```
route add -net 192.189.129.0 netmask 255.255.255.252 gw 192.189.136.2   #A9 The Queen
route add -net 192.189.131.0 netmask 255.255.254.0 gw 192.189.136.2     #A13 Oakleave
route add -net 192.189.128.0 netmask 255.255.255.0 gw 192.189.136.2     #A8 Keith
route add -net 192.189.144.128 netmask 255.255.255.128 gw 192.189.145.2 #A17 Helga
route add -net 192.189.144.0 netmask 255.255.255.128 gw 192.189.145.2   #A16 Spendrow
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.189.146.1                 #default
```

**The Profound**
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.189.145.1                 #default
```

**The Firefist**
```
route add -net 192.189.129.0 netmask 255.255.255.252 gw 192.189.128.2   #A9 The Queen
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.189.136.1                 #default
```

**The Queen**
```
route add -net 0.0.0.0 netmask 0.0.0.0 gw 192.189.128.1                 #default
```

### CIDR Routing - IP Tables The Resonance
Pada router The Resonance jalankan perintah berikut ini:
```
  iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE -s 192.189.0.0/15
```

### CIDR Routing - Setting resolv.conf
Pada semua node selain The Resonance (termasuk router-router lain), jalankan perintah berikut ini:
```
  echo nameserver 192.168.122.1 > /etc/resolv.conf
```

### CIDR Routing - Bukti Berhasil Ping
![Bukti1Ping](https://github.com/MonicaDavita/Jarkom-Modul-4-D09-2022/blob/main/AsetCIDR/Gui-Ph%20PING%20Success.jpeg?raw=true)
* Guideau to Phanora


## VLSM CPT
### Topologi CPT
<img width="960" alt="Screenshot_20221126_212023" src="https://user-images.githubusercontent.com/94627623/204093545-730b940b-ffbf-4357-ad48-a26621995d15.png">
