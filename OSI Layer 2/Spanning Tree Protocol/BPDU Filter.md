## Purpose

Stop port from sending bpdu's. End host devices dont need bpdus.

## How to configure BPDU Filter

#### Steps

1. Enable BPDU Filter on an interface. Disables STP on that port. It will not send BPDUs and will ignore BPDUs it receives.
```
enable
configure terminal
interface <interface>
spanning-tree bpdufilter enable
```

1.  Enable BPDU Filter in Global Configuration Mode. It will enable BPDU filter on all PortFast ports by default. It will not send BPDUs. If it receives a BPDU it will disable PortFast and BPDU Filter and at like a normal STP port.
```
enable
configure terminal
spanning-tree portfast [edge] bpdufilter default
```

1. Disable BPDU Filter on an interface.
```
enable
configure terminal
interface <interface>
spanning-tree bpdufilter disable
```
