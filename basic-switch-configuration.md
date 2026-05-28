# Basic Cisco Switch Configuration

## Configure Hostname
hostname SW1

## Configure Management IP
interface vlan 1
 ip address 192.168.1.10 255.255.255.0
 no shutdown

## Configure Default Gateway
ip default-gateway 192.168.1.1

## Configure SSH Access
ip domain-name lab.local
crypto key generate rsa
username admin secret Cisco123

line vty 0 4
 login local
 transport input ssh

## Save Configuration
write memory
