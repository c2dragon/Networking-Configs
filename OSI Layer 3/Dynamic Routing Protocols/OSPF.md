## How to configure 

#### Steps

1. Configure OSPF. Network must have a netmask and area specified.
```
enable
configure terminal
router ospf <process ID>
network <network> <netmask> area <area number>
```

1. Passive interface. Tells the router to stop sending OSPF 'hello' messages out of the interface.
```
enable
configure terminal
router ospf <process ID>
passive-interface <interface>
```

1. Configure certain interfaces to be active if 'passive-interface default' is used.
```
no passive-interface <interface>
```

1. Change router id.
```
enable
configure terminal
router ospf <process ID>
router-id <router id>
```

2. Default route. Advertise the default route.
```
enable
configure terminal
router ospf <process ID>
default-information originate
```

3. Clear OSPF process.
```
enable
clear ip ospf process
```

4. Change the max paths OSPF will load balance over.
```
enable
configure terminal
router ospf <process ID>
maximum-paths <number of paths>
```

5. Change the administrative distance.
```
enable
configure terminal
router ospf <process ID>
distance <distance>
```

6. Change the reference bandwidth.
```
enable
configure terminal
router ospf <process ID>
auto-cost reference-bandwidth <number[default 100]>
```

7. Change the OSPF cost on and interface.
```
enable
configure terminal
interaface <interface>
ip ospf cost <number>
```

8. Change the bandwidth to manipulate the metric.
```
enable
configure terminal
interface <interface>
bandwidth <number>
```

9. Change an interface to be in an OSPF area.
```
enable
configure terminal
interface <interface>
ip ospf <process ID> area <area number>
```

10. Change interface OSPF priority.
```
enable
configure terminal
interface <interface>
ip ospf priority <priority>
```

1. Change OSPF hello interval.
```
enable
configure terminal
interface <interface>
ip ospf hello-interval <seconds>
```

1. Change the OSPF dead interval.
```
enable
configure terminal
interface <interface>
ip ospf dead-interval <seconds>
```

1. Put a password on OSPF
```
enable
configure terminal
interface <interface>
ip ospf authentication-key jeremy
ip ospf authentication
```

1. Change the MTU.
```
enable
configure terminal
interface <interface>
ip mtu <bytes>
```

1. Change OSPF network type.
```
enable
configure terminal
router ospf <process ID> <netmask> area <area number>
interface <interface>
ip ospf network <type of network. point to point etc>
```
## Useful show commands

```
show ip protocols
```

```
show ip ospf interface <interface>
```

```
show ip ospf interface brief
```

```
show ip ospf neighbor
```

```
show running-config | section ospf
```

```
show ip ospf database
```

