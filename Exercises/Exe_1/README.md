# [name of the exercise/ folder name]

## Table of Content

- [Description](#description)
- [References](#references-linkimages-of-topology)
- [Topology](#images-of-the-topology)
- [Automation Script](#link-to-scripts)
    - [Disclaimer](#disclaimer)

## Description


## References (link/images of topology)

![Reference image from instructor][ref_image]


## (Images of the) Topology

![Image of the topology] [final_image]

## Link to scripts

NOT AVAILABLE 
Reason: this is initial basic config, refer to [Command Used](#commands-used) for more info about this config

### Commands used

On Router(R1):

    enable
        configure terminal
            hostname R1
            enable secret cisco
            service password-encryption
            line console 0
                password cisco
                login
                exit
            ip domain-name try.try.io
            crypto key generate rsa
            2048 [ enter ]
            line vty 0 4
                transport input ssh
                login local
                username cisco password cisco
            interface GigabitEthernet 0/0
                ip address 192.168.2.253 255.255.255.224
                no shutdown
            interface GigabitEthernet 0/1
                ip address 192.168.3.253 255.255.255.224
                no shutdown
            

On Left Switch (S1):

    enable
        configure terminal
            hostname S1
            enable secret cisco
            service password-encryption
            line console 0
                password cisco
                login
                exit
            ip domain-name try.try.io
            crypto key generate rsa
            2048 [ enter ]
            line vty 0 4
                transport input ssh
                login local
                username cisco password cisco
            interface vlan 1
                ip address 192.168.1.200 255.255.255.224
                no shutdown
                exit

On Right Switch (R2):

    enable
        configure terminal
            hostname S2
            enable secret cisco
            service password-encryption
            line console 0
                password cisco
                login
                exit
            ip domain-name try.try.io
            crypto key generate rsa
            2048 [ enter ]
            line vty 0 4
                transport input ssh
                login local
                username cisco password cisco
            interface vlan 1
                ip address 192.168.1.201 255.255.255.224
                no shutdown
                exit
            
Set Up end device via GUI with the following IPs (in counter clockwise order):
- 192.168.1.1 /27
- 192.168.1.2 /27
- 192.168.1.3 /27
- 192.168.1.4 /27


### Disclaimer

Combo user/pass: cisco/cisco
General password: cisco

[x] Tested on cisco packet tracer
[ ] Tested IRL
[ ] Used AI in some way (specify):
    - 


[ref_image]: Exe_1.png "Reference image for instructor"

[final_image]: Exe_1_final.png "Image of the topology taken from simulator/emulator [to specify]"

[script_url]: script_exe_1.py