# knx-gateway-discover

Nmap NSE script to discover KNX home automation gateways by sending multicast search requests.

## Usage

```
# knx  nmap -e enp0s25 --script ./knx-gateway-discover.nse
```

*Note*: Increase verbosity/debug to see full message contents:

```
# knx  nmap -e enp0s25 -v -d --script ./knx-gateway-discover.nse
```

## Sample Output

```
# knx-gateway-discover git:(master) ✗ nmap -e enp0s25 --script ./knx-gateway-discover.nse

Starting Nmap 6.47SVN ( http://nmap.org ) at 2015-08-07 00:39 CEST
Pre-scan script results:
| knx-gateway-discover: 
|   status: Found 2 KNX gateway(s)
|   gateways: 
|     gateway2: 
|       IP address: 192.168.178.20
|       Port: 3671
|       KNX address: 1.1.5
|       
|         services: 
|           KNXnet/IP Core
|           KNXnet/IP Device Management
|           KNXnet/IP Tunnelling
|     gateway1: 
|       IP address: 192.168.178.11
|       Port: 3671
|       KNX address: 15.15.255
|       
|         services: 
|           KNXnet/IP Core
|           KNXnet/IP Device Management
|           KNXnet/IP Tunnelling
|_          KNXnet/IP Object Server
WARNING: No targets were specified, so 0 hosts scanned.
Nmap done: 0 IP addresses (0 hosts up) scanned in 3.31 seconds
```
