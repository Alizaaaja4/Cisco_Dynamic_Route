# Cisco Dynamic Route
Practice Simulation of Dynamic Routing in Cisco Packet Tracer Application

Repository Title : Dynamic Routing in Cisco Packet Tracer

Description : This simulation visualizes routing concepts using dynamic methods. It has 3 visual rooms, consisting of computers, laptops, and switches. It is connected by two routers configured with dynamic routing.

## Designed Network
![Design Cisco](https://github.com/Alizaaaja4/Cisco_Dynamic_Route/blob/main/Dokumentasi.jpeg)

### Dynamic Routing (RIP)
Dynamic routing is routing carried out by routers by creating data communication paths automatically according to the settings made. If there is a change in topology in the network, the router will automatically create a new routing path

#### Change the Router Name
    Router> enable
    Router# configure terminal
    Router(config)# hostname [new name]
    
    ---- example :
    
    Router(config)# hostname RouterA
    RouterA(config)# exit
    RouterA# ....

#### Using Encryption
    Router> enable
    Router# configure terminal
    Router(config)# enable secret [name password]
    Router(config)# ....

#### Connect Device to Router
    Router> enable
    Router# configure terminal
    Router(config)# interface [ex: fa1/0]
    Router(config-if)# ip address [ip default] [subnetmask]
    Router(config-if)# no shutdown
    Router(config-if)# exit
    Router(config)# ....

#### Connect Router to Router (Dynamic Methods)
    Router> enable
    Router# configure terminal
    Router(config)# router rip
    Router(config-router)# network ip address [1]
    Router(config-router)# network ip address [2]
    Router(config-router)# network ip address [3]
    Router(config-router)# exit
    Router(config)# exit
    Router# show ip route
