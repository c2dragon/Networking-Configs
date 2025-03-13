## How to configure BPDU Guard

#### Steps

1. Interface BPDU Guard
```
enable
configure terminal
interface <interface>
spanning-tree bpduguard enable
```

1. Global BPDU Guard. Enables BPDU Guard on all PortFast ports.
```
enable
configure terminal
spanning-tree portfast [edge] bpduguard default
```

1. Manually re-enable an err-disabled port.
```
shutdown
no shutdown
```

1. Errdisable Recovery
```
errdisable recovery cause <cause ie. bpduguard>
```

1. Errdisable Recovery Interval. 5 min by default
```
errdisable recovery interval
```

## Useful Show Commands

```
show spanning-tree interface g0/1 detail
```

```
show errdisable recovery
```

