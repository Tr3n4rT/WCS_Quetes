## Fichiers de configurations 

#### Machine 10

![config-m-10](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/Network/Routage_Linux/images/config-m-10.png)

#### Machine 11

![config-m-11](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/Network/Routage_Linux/images/config-m-11.png)

#### Machine 12

![config-m12](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/Network/Routage_Linux/images/config-m12.png)

#### Machine 13

![config-m13](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/Network/Routage_Linux/images/config-m13.png)

#### Routeur 0

__Configuration :__

![config-r0](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/Network/Routage_Linux/images/config-r0.png)

__Route :__

![route-r0.png](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/Network/Routage_Linux/images/route-r0.png)

#### Routeur 1

__Configuration :__

![config-r1](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/Network/Routage_Linux/images/config-r1.png)

__Route :__

![route-r0](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/Network/Routage_Linux/images/route-r0.png)

#### Routeur 2

__Configuration :__

![config-r1](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/Network/Routage_Linux/images/route-r1.png)

__Route :__

![route-r2](https://github.com/Tr3n4rT/WCS_Quetes/blob/main/Network/Routage_Linux/images/route-r2.png)



## Routage 


#### Routeur 0
__Commandes ipv4 :__\
sudo ip route add 10.0.1.0/24 via 192.168.0.251 dev ens5\
sudo ip route add 10.0.2.0/24 via 192.168.0.252 dev ens5

__Commandes ipv6 :__\
sudo ip route add fd18:93ee:1::/64 via fd18:93ee:192::251 dev ens5\
sudo ip route add fd18:93ee:2::/64 via fd18:93ee:192::252 dev ens5


#### Routeur 1
__Commandes ipv4 :__\
sudo ip route add 10.0.0.0/24 via 192.168.0.250 dev ens5\
sudo ip route add 10.0.2.0/24 via 192.168.0.252 dev ens5

__Commandes ipv6 :__\
sudo ip route add fd18:93ee:2::/64 via fd18:93ee:192::252 dev ens5\
sudo ip route add fd18:93ee:5810::/64 via fd18:93ee:192::250 dev ens5


#### Routeur 2
__Commandes ipv4 :__\
sudo ip route add 10.0.0.0/24 via 192.168.0.250 dev ens5\
sudo ip route add 10.0.1.0/24 via 192.168.0.251 dev ens5

__Commandes ipv6 :__\
sudo ip route add fd18:93ee:1::/64 via fd18:93ee:192::251 dev ens5\
sudo ip route add fd18:93ee:5810::/64 via fd18:93ee:192::250 dev ens5
