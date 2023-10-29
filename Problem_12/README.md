Network Address = `192.168.1.0/24`

```
HQ LAN1 = 50 host = 64 host = 2^6
        n = 32-6 = 26
        First address = 192.168.1.0/26
        Last  address = 192.168.1.63/26
        Subnet mask   = 255.255.255.192
```
```
HQ LAN2 = 50 host = 64 host = 2^6
        n = 32-6 = 26
        First address = 192.168.1.64/26
        Last  address = 192.168.1.127/26
        Subnet mask   = 255.255.255.192
```
```
BRANCH1 LAN1 = 20 host = 32 host = 2^5
            n = 32-5 = 27
            First address = 192.168.1.128/27
            Last  address = 192.168.1.159/27
            Subnet mask   = 255.255.255.224
```
```
BRANCH1 LAN2 = 20 host = 32 host = 2^5
            n = 32-5 = 27
            First address = 192.168.1.160/27
            Last  address = 192.168.1.191/27
            Subnet mask   = 255.255.255.224
```
```
BRANCH2 LAN1 = 12 host = 16 host = 2^4
            n = 32-4 = 28
            First address = 192.168.1.192/28
            Last  address = 192.168.1.207/28
            Subnet mask   = 255.255.255.240
```
```
BRANCH2 LAN2 = 12 host = 16 host = 2^4
            n = 32-4 = 28
            First address = 192.168.1.208/28
            Last  address = 192.168.1.223/28
            Subnet mask   = 255.255.255.240
```

```
link HQ to BRANCH1 = 4 host = 4 host = 2^2
                n = 32-2 = 30
                First address = 192.168.1.224/30
                Last  address = 192.168.1.227/30
                Subnet mask   = 255.255.255.252
```
```
link HQ to BRANCH2 = 4 host = 4 host = 2^2
                n = 32-2 = 30
                First address = 192.168.1.228/30
                Last  address = 192.168.1.231/30
                Subnet mask   = 255.255.255.252
```
```
link Branch1 to BRANCH2 = 4 host = 4 host = 2^2
                    n = 32-2 = 30
                    First address = 192.168.1.232/30
                    Last  address = 192.168.1.235/30
                    Subnet mask   = 255.255.255.252
```

