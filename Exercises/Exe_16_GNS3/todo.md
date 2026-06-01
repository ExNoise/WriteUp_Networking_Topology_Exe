# TODO



ip route, da r2 a loopback di r1 e stessa cosa per r3 to r1

r2# ip route 192.168.1.1 255.255.255.0 serial 0/1 



1. configure eigrp between r2 and r3 with the network address

2. between r1 and r2 (ip route 192.168.1.0 255.255.255.252 192.168.1.1), r1 and r3 static routes to loopback

3. create a default route on r1 to r2 and test ping-ing the lo of the 2 servers, administrative distance 5, r1-r3 administrative distance 10 but same default route

4. add to r1 2 monitoring processes sla

5. create 2 object for tracking object, track 1 and track 2, to associate sla 1 and sla2 respectivly





10. show ip sla statistics


## eigrp

1. setup iniziale

2. loopback di isp1 e web server