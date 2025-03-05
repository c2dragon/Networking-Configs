## How to configure a VLAN

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

4. Assign Ports to the VLAN.
```
interface <interface> 
### OR interface range <interface range>
switchport mode access
switchport access vlan <VLAN-ID>
```

#### Example:
```
vlan 10
name Engineering VLAN
interface f0/0
switchport mode access
switchport access vlan 10
```

## Useful Show Commands

Shows vlans
```
show vlan brief
```

