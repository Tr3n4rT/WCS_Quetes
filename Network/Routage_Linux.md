## Fichiers de configurations 

#### Machine 10


#### Machine 11

#### Machine 12

#### Machine 13

#### Routeur 1

#### Routeur 2

#### Routeur 3


## Routage 


#### Routeur 0
__Commandes ipv4 :__
sudo ip route add 10.0.1.0/24 via 192.168.0.251 dev ens5
sudo ip route add 10.0.2.0/24 via 192.168.0.252 dev ens5

__Commandes ipv6 :__
sudo ip route add fd18:93ee:1::/64 via fd18:93ee:192::251 dev ens5
sudo ip route add fd18:93ee:2::/64 via fd18:93ee:192::252 dev ens5


#### Routeur 1
__Commandes ipv4 :__
sudo ip route add 10.0.0.0/24 via 192.168.0.250 dev ens5
sudo ip route add 10.0.2.0/24 via 192.168.0.252 dev ens5

__Commandes ipv6 :__
sudo ip route add fd18:93ee:2::/64 via fd18:93ee:192::252 dev ens5
sudo ip route add fd18:93ee:5810::/64 via fd18:93ee:192::250 dev ens5


#### Routeur 2
__Commandes ipv4 :__
sudo ip route add 10.0.0.0/24 via 192.168.0.250 dev ens5
sudo ip route add 10.0.1.0/24 via 192.168.0.251 dev ens5

__Commandes ipv6 :__
sudo ip route add fd18:93ee:1::/64 via fd18:93ee:192::251 dev ens5
sudo ip route add fd18:93ee:5810::/64 via fd18:93ee:192::250 dev ens5
