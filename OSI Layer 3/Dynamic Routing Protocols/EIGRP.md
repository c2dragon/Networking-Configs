## How to configure 

#### Steps

1. Configure EIGRP. Network will assume a classful network is no netmask is specified.
```
enable
configure terminal
router eigrp <AS number>
no auto-summary
passive-interface <interface>
network <network> <netmask>
```

1. Configure EIGRP router id.
```
enable
configure terminal
router eigrp <AS number>
no auto-summary
eigrp router-id <router-id>
```
## Useful show commands

```
show ip protocols
```

