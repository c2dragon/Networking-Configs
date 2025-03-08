## How to configure a Layer 3 Switch for Inter-VLAN Routing

#### Steps:

1. Enter Global Configuration Mode.
```
enable
configure terminal
```

2. Enable routing on the layer 3 switch.
```
ip routing
```

3. Enter interface configuration mode.
```
interface <interface>
```

4. Configure interface as a router port.
```
no switchport
```

5. Configure the IP address on the interface.
```
ip address <address> <netmask>
```

1. Go back to Global Configuration Mode.
```
exit
```

1. Configure the static default route to the router.
```
ip route 0.0.0.0 0.0.0.0 <next hop>
```

1. Create SVI for each VLAN.
```
interface <vlan>
```

2. Configure the IP address for the SVI.
```
ip address <address> <netmask>
```

1. Bring up the interface. VLAN must exist. Create VLAN in Global Configuration Mode if not existing.
```
no shutdown
```

## Useful Show Commands

```
show interfaces status
```

```
show interfaces <interface>
```
