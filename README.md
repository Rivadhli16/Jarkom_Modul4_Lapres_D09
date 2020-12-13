# Jarkom_Modul4_Lapres_D09

### 05111840000058 Rafif Ridho
### 05111840000128 Muhammad Rivadhli Purnomo

## TOPOLOGI CPT
![img](/img/1.jpg)

### Kelompok kami mengerjakan teknik VLSM pada CPT, sedangkan teknik CIDR pada UML.

## VLSM (Variable Length Subnet Masking) - CPT

Pembagian Tiap Subnet

![img](/img/1-2.jpg)

Perhitungan total ip

![img](/img/1-3.jpg)

Pohon VLSM

![img](/img/1-4.png)

Pembagian NID

![img](/img/1-5.jpg)

Routing

![img](/img/1-6.jpg)

## CIDR (Classles Inter-Domain Routing)

### Pembagian Subnet 

Class A

![img](/img/2-1.png)

Class B

![img](/img/2-2.png)

Class C

![img](/img/2-3.png)

Class D

![img](/img/2-4.png)

Class E

![img](/img/2-5.png)

Class F

![img](/img/2-6.png)

Class G

![img](/img/2-7.png)

Dari Subnetting di atas didapatkan Tree sebagai berikut

![img](/img/2-8.png)

Membuat topo.sh mengikuti topologi yang sudah diberikan

![img](/img/2-9.png)

Jalankan topo.sh, lalu kemudian isi /etc/network/interfaces seperti berikut

1. Surabaya
```
auto lo
iface lo inet loopback

#cloud
auto eth0
iface eth0 inet static
address 10.151.72.46
netmask 255.255.255.252
gateway 10.151.72.45
 
#sampang
auto eth1
iface eth1 inet static
address 192.168.64.1
netmask 255.255.252.0
 
#pasuruan
auto eth2
iface eth2 inet static
address 192.168.192.1
netmask 255.255.255.252
 
#batu
auto eth3
iface eth3 inet static
address 192.168.32.1
netmask 255.255.255.252
 
#mojokerto
auto eth4
iface eth4 inet static
address 10.151.79.81
netmask 255.255.255.252
```
2. Mojokerto

```
auto lo
iface lo inet loopback

#surabaya
auto eth0
iface eth0 inet static
address 10.151.79.82
netmask 255.255.255.252
gateway 10.151.79.81
```

3. Pasuruan 
```
auto lo
iface lo inet loopback

#surabaya
auto eth0
iface eth0 inet static
address 192.168.192.2
netmask 255.255.255.252
gateway 192.168.192.1
 
#probolinggo
auto eth1
iface eth1 inet static
address 192.168.144.1
netmask 255.255.255.252
 
#sidoarjo
auto eth2
iface eth2 inet static
address 192.168.160.1
netmask 255.255.252.0
```

4. Probolinggo

```
auto lo
iface lo inet loopback
 
#pasuruan
auto eth0
iface eth0 inet static
address 192.168.144.2
netmask 255.255.255.252
gateway 192.168.144.1
 
#bondowoso
auto eth1
iface eth1 inet static
address 192.168.136.1
netmask 255.255.255.128
 
#jember&banyuwangi
auto eth2
iface eth2 inet static
address 192.168.128.1
netmask 255.255.248.0
```

5. Bondowoso

```
auto lo
iface lo inet loopback
 
#probolinggo
auto eth0
iface eth0 inet static
address 192.168.136.2
netmask 255.255.255.128
gateway 192.168.136.1
```

6. Jember

```
auto lo
iface lo inet loopback
 
#probolinggo
auto eth0
iface eth0 inet static
address 192.168.128.2
netmask 255.255.248.0
gateway 192.168.128.1
```

7. Banyuwangi

```
auto lo
iface lo inet loopback
 
#probolinggo
auto eth0
iface eth0 inet static
address 192.168.128.3
netmask 255.255.248.0
gateway 192.168.128.1
```

8. Sidoarjo

```
auto lo
iface lo inet loopback
 
#pasuruan
auto eth0
iface eth0 inet static
address 192.168.160.2
netmask 255.255.252.0
gateway 192.168.160.1
```

9. Sampang 

```
auto lo
iface lo inet loopback
 
#surabaya
auto eth0
iface eth0 inet static
address 192.168.64.2
netmask 255.255.252.0
gateway 192.168.64.1
```

10. Batu

```
auto lo
iface lo inet loopback
 
#surabaya
auto eth0
iface eth0 inet static
address 192.168.32.2
netmask 255.255.255.252
gateway 192.168.32.1
 
#kediri
auto eth1
iface eth1 inet static
address 192.168.8.1
netmask 255.255.255.252
 
#nganjuk
auto eth2
iface eth2 inet static
address 192.168.20.1
netmask 255.255.252.0
 
#jombang
auto eth3
iface eth3 inet static
address 192.168.18.1
netmask 255.255.254.0
```

11. Nganjuk

```
auto lo
iface lo inet loopback
 
#batu
auto eth0
iface eth0 inet static
address 192.168.20.2
netmask 255.255.252.0
gateway 192.168.20.1
```

12. Jombang

```
auto lo
iface lo inet loopback
 
#batu
auto eth0
iface eth0 inet static
address 192.168.18.2
netmask 255.255.254.0
gateway 192.168.18.1
```

13. Madiun

```
auto lo
iface lo inet loopback
 
#bojonegoro
auto eth0
iface eth0 inet static
address 192.168.16.1
netmask 255.255.255.240
 
#batu
auto eth1
iface eth1 inet static
address 192.168.18.3
netmask 255.255.254.0
gateway 192.168.18.1
```

14. Kediri

```
auto lo
iface lo inet loopback
 
#batu
auto eth0
iface eth0 inet static
address 192.168.8.2
netmask 255.255.255.252
gateway 192.168.8.1
 
#lumajang
auto eth1
iface eth1 inet static
address 192.168.4.1
netmask 255.255.255.0
 
#malang
auto eth2
iface eth2 inet static
address 10.151.79.85
netmask 255.255.255.252
```

15. Lumajang

```
auto lo
iface lo inet loopback
 
#kediri
auto eth0
iface eth0 inet static
address 192.168.4.2
netmask 255.255.255.0
gateway 192.168.4.1
```

16. Blitar

```
auto lo
iface lo inet loopback
 
#tulungagung
auto eth0
iface eth0 inet static
address 192.168.0.1
netmask 255.255.252.0
 
#kediri
auto eth1
iface eth1 inet static
address 192.168.4.3
netmask 255.255.255.0
gateway 192.168.4.1
```

17.  Tulungagung

```
auto lo
iface lo inet loopback
 
#blitar
auto eth0
iface eth0 inet static
address 192.168.0.2
netmask 255.255.252.0
gateway 192.168.0.1
```

18. Bojonegoro

```
auto lo
iface lo inet loopback
 
#madiun
auto eth0
iface eth0 inet static
address 192.168.16.2
netmask 255.255.255.240
gateway 192.168.16.1
```

19. Malang

```
#kediri
auto eth0
iface eth0 inet static
address 10.151.79.86
netmask 255.255.255.252
gateway 10.151.79.85
```
Lalu routing di Surabaya, Pasuruan, Batu, dan Kediri

1. Surabaya

```
#pasuruan D2/18
route add -net 192.168.128.0 netmask 255.255.192.0 gw 192.168.192.2

#batu D1/19
route add -net 192.168.0.0 netmask 255.255.224.0 gw 192.168.32.2

#malang
route add -net 10.151.79.84 netmask 255.255.255.252 gw 192.168.32.2
```

2. Pasuruan

```
#probilinggo
route add -net 192.168.128.0 netmask 255.255.240.0 gw 192.168.144.2
```

3. Batu

```
#kediri
route add -net 192.168.0.0 netmask 255.255.248.0 gw 192.168.8.2

#malangikutkediri
route add -net 10.151.79.84 netmask 255.255.255.252 gw 192.168.8.2

#madiun
route add -net 192.168.16.0 netmask 255.255.252.0 gw 192.168.18.3
```

4. Kediri

```
#blitar
route add -net 192.168.0.0 netmask 255.255.248.0 gw 192.168.4.3
```

Setelah itu uncomment net.ipv4.ip_forward = 1 di `nano /etc/sysctl.conf` lalu ketikkan  `sysctl -p` dan enter pada semua router

![img](/img/2-10.png)

Lalu iptables di Surabaya

![img](/img/2-11.png)

Lalu testing dengan ping ke cloud, akan tetapi pada uml kami sepertinya masih ada kesalahan dan tidak bisa ping ke cloud dari uml yg tidak terhubung ke surabaya langsung
