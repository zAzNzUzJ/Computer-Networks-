# Computer-Networks-
PACKET TRACER - ROUTING

routing protocols  -- types -- static or dynamic routing

 Static routing config
 set up the topology and decide the newtwork range :
router config:
Router 0
en
in conofgure terminal --conf t
 int g0/0/0 <interface 1>
ip address <ip address > <subnetmask>
no shutdown
exit

int g0/0/1 <interface 2>
ip address <ip address> <subnetmask>
no shutdown
exit

ip route <network> <network mask> <next hop IP>  or 


Router 1
ip route 192.168.1.0 255.255.255.0 10.10.10.1 (next hop IP)

DHCP - 
setup one router as server --  provied IP to the all the other nodes in the network
configure server router
Router(config)#int fa0/0 <interface>
Router(config-if)#ip add <ip> <subnetmask>
Router(config-if)#no shut
setup pool range of ip 
Router(config)#ip dhcp pool <name> 
Router(dhcp-config)#network <network> <network mask>    
Router(dhcp-config)#default-router <default router ip>
Router(dhcp-config)#dns-server <ip>
Router(dhcp-config)#exit
Router(config)#ip dhcp excluded-address <server ip> <gateway ip>
Router(config)#exit

check :
Router#show ip dhcp binding 

setup routing protocols on the other router so the nodes connected to other router in the network gets the IP from the same server 


---------------------------------------------


set up RIP -- routing protocol





