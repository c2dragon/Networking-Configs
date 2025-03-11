## How to configure Spanning tree

#### Steps:

STP is automatically configured on switches. Usually rapid-PVST

1. Change mode
```
enable
configure terminal
spanning-tree mode <mode ie mst/pvst/rapid-pvst
```

2. Configure the root bridge.
```
enable
configure terminal
spanning-tree vlan <number> root primary
```

3. Change the Cost of and interface. To cause the switch to choose a different root port.
```
enable
configure terminal
interface <interface>
spanning-tree vlan <number> cost <cost>
```

4. Change Port Priority on a Port. Last tie-breaker after Root cost and Sender bridge ID.
```
enable
configure terminal
interface <interface>
spanning-tree vlan <number> port-priority <number>
```

## Useful Show Commands

```
show spanning-tree
```

```
show spanning-tree vlan <number>
```

```
show spanning-tree summary
```