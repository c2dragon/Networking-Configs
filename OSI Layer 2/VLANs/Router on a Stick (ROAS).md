## How to configure ROAS (Layer 3)

1. Enter Interface Configuration Mode on the Router.
```
enable
conf t
interface <interface>
```

2. Turn on the interface. Router interfaces are shutdown by default.
```
no shutdown
```

3. Create sub-interface: Put a dot after the interface and then the sub-interface number.
```
interface <example: g0/0.10>
```

4. Choose encapsulation type for the VLAN.
```
encapsulation dot1q <vlan>
```

5. Give the interface an IP address.
```
ip address <address> <netmask>
```

6. Reset the interface to default settings
```
default interface <interface>
```
## Useful Show Commands

Shows the interfaces on the router. Including the sub-interfaces.
```
show ip interface brief
```

Shows the routes created by the IPs configured on the sub-interfaces. (i.e. the Connected and Local Routes)
```
show ip route
```

