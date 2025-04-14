## How to configure 

#### Steps

1. Configure. A network to use RIP version 2. The network command is classful so it assumes the netmask.
```
enable
configure terminal
router rip
version 2
no auto-summary
network <network>
```

1. Passive interface. Tells the router to stop sending RIP advertisements out of the interface.
```
enable
configure terminal
router rip
version 2
no auto-summary
passive-interface g2/0
```

1. Default route. Advertise the default route using rip.
```
enable
configure terminal
router rip
version 2
no auto-summary
default-information originate
```

## Useful show commands

```
show ip protocols
```
