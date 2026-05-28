# TODO

1. configure egrp between r2 and r3 with the network address

2. between r1 and r2 (ip route 192.168.1.0 255.255.255.252 192.168.1.1), r1 and r3 static routes to loopback

3. create a default route on r1 to r2 and test ping-ing the lo of the 2 servers, administrative distance 5, r1-r3 administrative distance 10 but same default route