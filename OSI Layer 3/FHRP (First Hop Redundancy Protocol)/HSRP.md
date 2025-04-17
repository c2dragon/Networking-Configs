## How to configure 

#### Steps

1. Configure HSRP. Configure VIP.
```
enable
configure terminal
interface <interface>
standby <group number> ip <VIP>
```

2. Change standby version.
```
enable
configure terminal
interface <interface>
standby <version number>
```

1. Change priority.
```
enable
configure terminal
interface <interface>
standby <group number> priority <number [default 100]>
```

1. Add Pre-emption.
```
enable
configure terminal
interface <interface>
standby <group number> preempt
```
