## How to Configure a Static Route

#### Steps:

1. Enter Global Configuration Mode
```
enable
configure terminal
```

1. Configure Static Route. Default route is  0.0.0.0/0
```
ip route <network> <netmask> <exit interface or next hop address or both> <administrative distance>
```
## Useful Show Commands

```
show ip route
```

