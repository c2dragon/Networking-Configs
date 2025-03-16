## Purpose

Prevents loops caused by unidirectional links.

Disables a port(loop inconsistent) if doesn't receive BPDUs for 20 seconds

Should be enabled on Root and Non-designated ports. (Ports that are supposed to receive BPDUs.)

## How to configure Loop Guard

#### Steps

1. Enable Loop Guard on an interface
```
enable
configure terminal
interface <interface>
spanning-tree guard loop
```

1. Enable Loop Guard on all ports.
```
enable
configure terminal
spanning-tree loopguard default
```

1. Disable Loop Guard on an interface
```
enable
configure terminal
interface <interface>
spanning-tree guard none
```

