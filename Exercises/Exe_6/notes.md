# on r1

interface g0/0/1
    ip address 10.10.0.1 255.255.255.248
interface lo0
    ip address 209.165.200.225 255.255.255.220
interface lo1
    ip address 192.168.1.225 255.255.223
interface lo2
    description internet
    ip address 209.165.200.224 255.255.255.228

# on a1

interface f0/11
    ip address 10.10.0.