## How to configure RSTP Link type

#### Steps

1. Configure link type. Point-to-point (switches). Shared (hubs). Edge(not switches or hubs).
```
enable
configure terminal
interface range <interface range>
spanning-tree link-type <type i.e. point-to-point>
```