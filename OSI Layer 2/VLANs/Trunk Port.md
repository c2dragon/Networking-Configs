## How to configure a VLAN Trunk

#### Steps
1. Enter Global configuration mode on the switch.
```
enable
configure terminal
```

2. Create the VLAN.
```
vlan <VLAN-ID>
```

3. Name the VLAN.
```
name <VLAN-NAME>
```

4. Enter Interface Configuration Mode.
```
interface <interface> 
```

5. Choose encapsulation type. Usually dot1q. Step only needed on older switches where encapsulation type is auto by default
```
switchport trunk encapsulation dot1q
```

6. Configure Trunk Ports to allow multiple VLANs on the interface.
```
switchport mode trunk
switchport trunk allowed vlan 10,20
```

1. Other trunk options
```
switchport trunk allowed vlan add 10
switchport trunk allowed vlan remove 10
switchport trunk allowed vlan all
switchport trunk allowed vlan except
switchport trunk allowed vlan none
```

1. Change Native VLAN
```
switchport trunk native vlan 1001
```

## Useful Show Commands

Shows VLANs and what interfaces are in them
```
show vlan brief
```

Shows Trunks and what VLANs are in them
```
show interfaces trunk
```

