# Laporan Resmi Modul 4 Jaringan Komputer I07
Ascarya Arkaandhiyaa Allaam (05111942000027)\
Farah Dhiah Qorirah (05111942000018)\
Julius Adetya Eka Bhaswara (05111942000026)

## Subnet

![image](https://user-images.githubusercontent.com/77782259/143684812-c3134e39-bd3a-48ba-9d5c-bd4671fc5577.png)

### Tabel Subnet


**Subnet**|**Alias**|**Jumlah IP**|**Netmask**|
:-------:| :-------------:|:---------:|:-------:
| A1      | Jipangu - Pucci               |  101      |  /25    |
| A2      | Courtyard - Calmbelt - Pucci  |  2021     |  /21    |
| A3      | Pucci - Water7                |  2        |  /30    |
| A4      | Ciper - Water7                |  701      |  /22    |
| A5      | Blueno - Foosha               |  1001     |  /22    |
| A6      | Water7 - Foosha               |  2        |  /30    |
| A7      | Foosha - Guanho               |  2        |  /30    |
| A8      | Jabra - Guanho                |  521      |  /22    |
| A9      | Guanho - Alabasta - Maingate  |  502      |  /23    |
| A10     | Alabasta - Jorge              |  13       |  /28    |
| A11     | Guanho - Oimo                 |  2        |  /30    |
| A12     | Enieslobby - Seastone - Oimo  |  252      |  /24    |
| A13     | Seastone - Elena              |  721      |  /22    |
| A14     | Foosha - Doriki               |  2        |  /30    |
| A15     | Oimo - Fukurou                |  2        |  /30    |
| Total   | -                             |  5845     |  /19    |


## Subnet Tree

![Subnet Tree](https://user-images.githubusercontent.com/73812417/143686373-b3ba9318-bbdd-4526-9fb0-161250b1702a.jpg)

## VLSM

[![image.png](https://i.postimg.cc/mZ7JcyhF/image.png)](https://postimg.cc/NLfpST6g)


## Config Router
### 1. FOOSHA
FA 0/0

```shell
10.41.12.1
255.255.252.0
```

FA 0/1

```shell
10.41.27.149
255.255.255.252
```

ETH 1/0

```shell
10.41.27.153
255.255.255.252
```

ETH 1/1

```shell
10.41.27.161
255.255.255.252
```

### 2. WATER7

FA 0/0

```shell
10.41.27.150
255.255.255.252
```

FA 0/1

```shell
10.41.8.1
255.255.252.0
```

FA 1/0

```shell
10.41.27.145
255.255.255.252
```

3. PUCCI

FA 0/0

```shell
10.41.27.146
255.255.255.252
```

FA 0/1

```shell
10.41.27.1
255.255.255.128
```

FA 1/0

```shell
10.41.0.1
255.255.248.0
```

4. GUANHAO

FA 0/0

```shell
10.41.27.154
255.255.255.252
```

FA 0/1

```shell
10.41.16.1
255.255.255.252
```

FA 1/0

```shell
10.41.24.1
255.255.254.0
```

FA 1/1

```shell
10.41.27.157
255.255.255.252
```

5. ALABASTA

FA 0/0

```shell
10.41.24.2
255.255.254.0
````

FA 0/1

```shell
10.41.27.129
255.255.255.240
```

6. OIMO

FA 0/0

```shell
10.41.27.158
255.255.255.252
```

FA 0/1

```shell
10.41.27.165
255.255.255.252
```

FA 1/0

```shell
10.41.26.1
255.255.255.0
```

7. SEASTONE

FA 0/0

```shell
10.41.26.2
255.255.255.0
```

FA 0/1

```shell
10.41.20.1
255.255.252.0
```

## Config PC & Server

1. BLUENO

```shell
10.41.12.2
255.255.252.0
10.41.12.1
```

2. CIPHER

```shell
10.41.8.2
255.255.252.0
10.41.8.1
```

3. JIPANGU

```shell
10.41.27.2
255.255.255.128
10.41.27.1
````

4. COURTYARD

```shell
10.41.0.2
255.255.248.0
10.41.0.1
```

5. CALMBELT

```shell
10.41.0.3
255.255.248.0
10.41.0.1
```

6. JABRA

```shell
10.41.16.2
255.255.252.0
10.41.16.1
```

7. MAINGATE

```shell
10.41.24.3
255.255.254.0
10.41.24.1
```

8. JORGE

```shell
10.41.27.130
255.255.255.240
10.41.27.129
```

9. FUKUROU

```shell
10.41.27.166
255.255.255.252
10.41.27.165
```

10. ENIESLOBBY

```shell
10.41.26.3
255.255.255.0
10.41.26.1
```

11. ELENA

```shell
10.41.20.2
255.255.252.0
10.41.20.1
```

12. DORIKI

```shell
10.41.27.162
255.255.255.252
10.41.27.161
```

## Static Routing

1. FOOSHA

```shell
BLUENO
10.41.12.0 
255.255.252.0
10.41.12.2

Cipher
10.41.8.0
255.255.252.0
10.41.27.150


JIPANGU
10.41.27.0
255.255.255.128
10.41.27.150


COURTYARD & CALMBELT
10.41.0.0
255.255.248.0
10.41.27.150

DORIKI
10.41.27.160
255.255.255.252
10.41.27.162

JABRA
10.41.16.0
255.255.252.0
10.41.27.154

MAINGATE
10.41.24.0
255.255.254.0
10.41.27.154

JORGE
10.41.27.128
255.255.255.240
10.41.27.154

ENIESLOBBY
10.41.26.0
255.255.255.0
10.41.27.154

ELENA
10.41.20.0
255.255.252.0
10.41.27.154

FUKUROU
10.41.27.164
255.255.255.252
10.41.27.154
```

Ruter terakhir 0.0.0.0 via sebelum menuju ruter 0.0.0.0/0 via 10.41.1.1

Ruter sebelum IP A yang belum via ip dari sebelum ke ruter 0.0.0.0/0 via 10.41.1.5 10.41.1.128/25 via 10.41.1.2

2. WATER7

```shell
JIPANGU
10.41.27.0
255.255.255.128
10.41.27.146

COURTYARD
10.41.0.0
255.255.248.0
10.41.27.146

0.0.0.0
0.0.0.0
10.41.27.149
```

3. PUCCI

```shell
0.0.0.0
0.0.0.0
10.41.27.145
```

4. GUANHAO

```shell
JORGE
10.41.27.128
255.255.255.240
10.41.24.2

FUKUROU
10.41.27.164
255.255.255.252
10.41.27.158

ENIESLOBBY
10.41.26.0
255.255.255.0
10.41.27.158

ELENA
10.41.20.0
255.255.252.0
10.41.27.158


0.0.0.0
0.0.0.0
10.41.27.153
```

5. ALABASTA

```shell
0.0.0.0
0.0.0.0
10.41.24.1
```

6. OIMO

```shell
ELENA
10.41.20.0
255.255.252.0
10.41.26.2

0.0.0.0
0.0.0.0
10.41.27.157
```

7. SEASTONE

```shell
0.0.0.0
0.0.0.0
10.41.26.1
```
