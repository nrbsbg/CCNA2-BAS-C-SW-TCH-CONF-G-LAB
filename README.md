## R1 Yapılandırması

Router> enable

Router# conf t

Router(config)# hostname R1

R1(config)# interface GigabitEthernet 0/0

R1(config-if)# ip address 192.168.10.1 255.255.255.0 // Gi 0/0 portuna IP adresi atandı.

R1(config-if)# description OFIS_AGI

R1(config-if)# no shutdown

R1(config-if)# exit

R1(config)# int Gi 0/1

R1(config-if)# ip address 192.168.20.1 255.255.255.0 // Gi 0/1portuna IP adresi atandı.

R1(config-if)# description SUNUCU_AGI

R1(config-if)# no shutdown

R1(config-if)# end

R1# copy running-config startup-config

## SW1 config
hostname SW1


enable secret cisco123

line console 0

password cisco123

login

exit

service password-encryption

SSH Konfigurasyonu:

ip domain-name ag.org.tr

crypto key generate rsa

The name for the keys will be:
SW1.agyoneticileri.org
How many bits in the modulus[512]:1024


username ayd password ayd123

line vty 0 15

login local

transport input ssh


exit

interface vlan 1

ip add 192.168.10.201 255.255.255.0

no shutdown

exit

ip default-gateway 192.168.10.1

end

copy running-config startup-config

## SW2 CONFİG
hostname SW2

enable secret cisco123

line console 0

password cisco123

login

exit

service password-encryption

SSH Konfigurasyonu:

ip domain-name ag.org.tr

crypto key generate rsa

The name for the keys will be:
SW1.agyoneticileri.org
How many bits in the modulus[512]:1024


username ayd password ayd123

line vty 0 15

login local

transport input ssh


exit

interface vlan 1

ip add 192.168.10.202 255.255.255.0

no shutdown

exit

ip default-gateway 192.168.10.1

end

copy running-config startup-config

## SW3 CONFİG

hostname SW3


enable secret cisco123

line console 0

password cisco123

login

exit

service password-encryption

SSH Konfigurasyonu:

ip domain-name ag.org.tr

crypto key generate rsa

The name for the keys will be:
SW1.agyoneticileri.org
How many bits in the modulus[512]:1024


username ayd password ayd123

line vty 0 15

login local

transport input ssh


exit

interface vlan 1

ip add 192.168.10.203 255.255.255.0

no shutdown

exit

ip default-gateway 192.168.10.1

end

copy running-config startup-config

## SW4 CONFİG

hostname SW4


enable secret cisco123

line console 0

password cisco123

login

exit

service password-encryption

SSH Konfigurasyonu:

ip domain-name ag.org.tr

crypto key generate rsa

The name for the keys will be:
SW1.agyoneticileri.org
How many bits in the modulus[512]:1024


username ayd password ayd123

line vty 0 15

login local

transport input ssh


exit

interface vlan 1

ip add 192.168.20.201 255.255.255.0

no shutdown

exit

ip default-gateway 192.168.10.1

end

copy running-config startup-config

## SW 5 CONFİG
hostname SW5


enable secret cisco123

line console 0

password cisco123

login

exit

service password-encryption

SSH Konfigurasyonu:

ip domain-name ag.org.tr

crypto key generate rsa

The name for the keys will be:
SW1.agyoneticileri.org
How many bits in the modulus[512]:1024


username ayd password ayd123

line vty 0 15

login local

transport input ssh


exit

interface vlan 1

ip add 192.168.20.202 255.255.255.0

no shutdown

exit

ip default-gateway 192.168.10.1

end

copy running-config startup-config

## SW 6 CONFİG
hostname SW6


enable secret cisco123

line console 0

password cisco123

login

exit

service password-encryption

SSH Konfigurasyonu:

ip domain-name ag.org.tr

crypto key generate rsa

The name for the keys will be:
SW1.agyoneticileri.org
How many bits in the modulus[512]:1024


username ayd password ayd123

line vty 0 15

login local

transport input ssh


exit

interface vlan 1

ip add 192.168.20.203 255.255.255.0

no shutdown

exit

ip default-gateway 192.168.20.1

end

copy running-config startup-config



SW1(config)# interface Gi 0/1

SW1(config-if)# speed 100

SW1(config-if)# duplex full

SW2(config)# interface Gi 0/1

SW2(config-if)# speed 100

SW1(config-if)# duplex full

SW1(config-if)# end


