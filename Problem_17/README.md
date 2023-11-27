The address space for Region 1 is `10.1.0.0/16`

```
B1-R1 branch router = 32,000 hosts = 32768 host = 2^15
                n = 32-15 = 17
                Network address = 10.1.0.0/17
                Last address    = 10.1.127.255/17
                Subnet mask   = 255.255.128.0
```
```
B2-R1 branch router = 16,000 hosts  = 16384 host = 2^14
                n = 32-14 = 18
                Network address = 10.1.128.0/18
                Last address    = 10.1.191.255/18
                Subnet mask   = 255.255.192.0
```
```
B3-R1 branch router = 8,000 hosts = 8192 host = 2^13
                n = 32-13 = 19
                Network address = 10.1.192.0/19
                Last address    = 10.1.223.255/19
                Subnet mask   = 255.255.224.0
```

>Divide the address space for each branch router into four equal subnets
```
B1-R1 branch router = 32768 host/4 = 8192 host = 2^13 (subnet n = 19)
                Network address = 10.1.0.0/17 , Last Address = 10.1.127.255/17
                B1-R1 Fa0/0 =  Network address = 10.1.0.0/19  , Last address = 10.1.31.255/19
                B1-R1 Fa0/1 =  Network address = 10.1.32.0/19 , Last address = 10.1.63.255/19
                B1-R1 Fa1/0 =  Network address = 10.1.64.0/19 , Last address = 10.1.95.255/19
                B1-R1 Fa1/1 =  Network address = 10.1.96.0/19 , Last address = 10.1.127.255/19
```
```
B2-R1 branch router = 16384 host/4 = 4096 host = 2^12 (subnet n = 20)
                Network address = 10.1.128.0/18 , Last address = 10.1.191.255/18
                B2-R1 Fa0/0 =  Network address = 10.1.128.0/20  , Last address = 10.143.255/20
                B2-R1 Fa0/1 =  Network address = 10.1.144.0/20 , Last address = 10.1.159.255/20
                B2-R1 Fa1/0 =  Network address = 10.1.160.0/20 , Last address = 10.1.95.255/20
                B2-R1 Fa1/1 =  Network address = 10.1.176.0/20 , Last address = 10.1.191.255/20
```
```
B3-R1 branch router = 8192 host/4 = 2048 host = 2^11 (subnet n = 21)
                Network address = 10.1.192.0/19 , Last address = 10.1.223.255/19
                B3-R1 Fa0/0 =  Network address = 10.1.192.0/21  , Last address = 10.199.255/21
                B3-R1 Fa0/1 =  Network address = 10.1.200.0/21 , Last address = 10.1.207.255/21
                B3-R1 Fa1/0 =  Network address = 10.1.208.0/21 , Last address = 10.1.215.255/21
                B3-R1 Fa1/1 =  Network address = 10.1.216.0/21 , Last address = 10.1.223.255/21
```
>For the WANs in Region 1, subnet the address space `10.1.255.240/28` 
>B1-R1 to R1 uses the first subnet, B2-R1 to R1 uses the second , B3-R1 to R1 the third.

```
 For WAN , we need 4 hosts. So = 
 First subnet  = Network address = 10.1.255.240/30 , Last address = 10.1.255.243/30
 Second subnet = Network address = 10.1.255.244/30 , Last address = 10.1.255.247/30
 Third subnet  = Network address = 10.1.255.248/30 , Last address = 10.1.255.251/30
```

<hr>
<hr>
<hr>

The address space for Region 2 is `172.20.0.0/16`

```
B1-R2 branch router = 4000 hosts = 4096 host = 2^12
                n = 32-12 = 20
                Network address = 172.20.0.0/20
                Last address    = 172.20.15.255/20
                Subnet mask   = 
```
```
B2-R2 branch router = 2000 hosts  = 2048 host = 2^11
                n = 32-11 = 21
                Network address = 172.20.16.0/21
                Last address    = 172.20.23.255/21
                Subnet mask   = 
```
```
B3-R2 branch router = 1000 hosts = 1024 host = 2^10
                n = 32-10 = 22
                Network address = 172.20.24.0/22
                Last address    = 172.20.27.255/22
                Subnet mask   = 
```

>Divide the address space for each branch router into four equal subnets
```
B1-R2 branch router = 4096 host/4 = 1024 host = 2^10 (subnet n = 22)
                Network address = 172.20.0.0/20 , Last Address = 172.20.15.255/20
                B1-R2 Fa0/0 =  Network address = 172.20.0.0/22 , Last address = 172.20.3.255/22
                B1-R2 Fa0/1 =  Network address = 172.20.4.0/22 , Last address = 172.20.7.255/22
                B1-R2 Fa1/0 =  Network address = 172.20.8.0/22 , Last address = 172.20.11.255/22
                B1-R2 Fa1/1 =  Network address = 172.20.12.0/22 , Last address = 172.20.15.255/22
```
```
B2-R2 branch router = 2048 host/4 = 512 host = 2^9 (subnet n = 23)
                Network address = 172.20.16.0/21 , Last address = 172.20.23.255/21
                B2-R2 Fa0/0 =  Network address = 172.20.16.0/23 , Last address = 172.20.17.255/23
                B2-R2 Fa0/1 =  Network address = 172.20.18.0/23 , Last address = 172.20.19.255/23
                B2-R2 Fa1/0 =  Network address = 172.20.20.0/23 , Last address = 172.20.21.255/23
                B2-R2 Fa1/1 =  Network address = 172.20.22.0/23 , Last address = 172.20.23.255/23
```
```
B3-R2 branch router = 1024 host/4 = 256 host = 2^8 (subnet n = 24)
                Network address = 172.20.24.0/22 , Last address = 172.20.26.255/22
                B3-R2 Fa0/0 =  Network address = 172.20.24.0/24 , Last address = 172.20.24.255/24
                B3-R2 Fa0/1 =  Network address = 172.20.25.0/24 , Last address = 172.20.25.255/24
                B3-R2 Fa1/0 =  Network address = 172.20.26.0/24 , Last address = 172.20.26.255/24
                B3-R2 Fa1/1 =  Network address = 172.20.27.0/24 , Last address = 172.20.27.255/24
```
>For the WANs in Region 2, subnet the address space `172.20.255.240/28`
>B1-R2 to R2 uses the first subnet, B2-R2 to R2 uses the second , B3-R2 to R2 the third

```
 For WAN , we need 4 hosts. So = 
 First subnet  = Network address = 172.20.255.240/30 , Last address = 172.20.255.243/30
 Second subnet = Network address = 172.20.255.244/30 , Last address = 172.20.255.247/30
 Third subnet  = Network address = 172.20.255.248/30 , Last address = 172.20.255.251/30
```

<hr>








