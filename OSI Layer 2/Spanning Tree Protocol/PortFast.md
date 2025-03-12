## How to configure PortFast:

#### Steps
1. Enable PortFast on an individual interface. Enter Interface Configuration Mode. Only works on access ports.
```
enable
configure terminal
interface <interface>
```

2. Configure PortFast.
```
spanning-tree portfast
```

1. Disable PortFast on an Interface.
```
spanning-tree portfast disable
```


#### Steps to enable PortFast on ALL access ports

1. Enable PortFast on all access ports. Enter Global Configuration Mode.
```
enable
configure terminal
```

2. Configure PortFast on all access ports.
```
spanning-tree portfast default
```


#### Steps to enable PortFast on Trunk ports

1. Used mostly for VMs and ROAS. Enter Interface Configuration Mode.
```
enable
configure terminal
interface <interface>
```

1. Configure PortFast on the trunk.
```
spanning-tree portfast trunk
```


## Useful Show Commands

```
show spanning-tree interface <interface> detail
```
