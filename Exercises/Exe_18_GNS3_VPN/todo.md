# TODO

## steps

1. copy and paste the scripts in /scripts to the routers

2. from r1 and r3 to r2 place a static route and ping the loopback

3. add a policy with crypto isakmp

4. add a key with crypto isakmp key [ key ] on r1 and r3

5. add access-list on r1 and r3 from the loopback to the loopback of the other router with icmp as protocol

6. add policy - R1(config)# crypto ipsec transform-set on r1 and r3

7. add crypto map with ipsec-isakmp on r1 and r3
    1. add "match address (access list)"
    2. set trasnform-set
    3. set peer of the other router
    4. set pfs group    (diffie-hellman group) [optional]
    5. set security-association [optional]

8. interface (interface to use)

9. crypto map [name_map]

10. "show crypto map" to check

11. ping lo-r3 source lo-r1 and check with wireshark

12. "show crypto isakmp sa" after some traffic to check the connection

13. "show crypto ipsec sa" to check the functionality of the vpn

14. PROFIT
