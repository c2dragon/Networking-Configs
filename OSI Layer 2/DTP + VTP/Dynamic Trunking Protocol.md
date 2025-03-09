## How to configure DTP on an interface.

#### Steps:

1. Enter Interface Configuration Mode.
```
enable
configure terminal
interface <interface>
```

1. Configure DTP in auto mode. This will not actively try to form a trunk.
```
switchport mode dynamic auto
```

1. Configure DTP in desirable mode. This will actively try to form a trunk.
```
switchport mode dynamic desirable
```

1. Disable DTP on an interface.
```
switchport nonegotiate
```

## Useful Show Commands

```
show interfaces <interface> switchport
```

