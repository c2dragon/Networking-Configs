## How to configure VTP on a switch

#### Steps:

1. Enter Global Configuration mode on the switch.
```
enable
configure terminal
```

1. Configure the VTP domain name. 
```
vtp domain <domain name>
```

1. Configure a switch to be in client mode. Cannot create, modify, or add VLANs.
```
vtp mode Client
```

1. VTP Transparent. WON'T forward advertisements if not in the same domain.
```
vtp mode transparent
```

1. Change the VTP version.
```
vtp version <number>
```

## Useful Show Commands

```
show vtp status
```

