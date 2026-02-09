# HP Aruba ArubaOS CLI Reference

**Last Updated**: 2026-02-09
**Platform**: Aruba Mobility Controllers, ArubaOS-CX Switches, ArubaOS-Switch
**Source**: [HPE Aruba Networking Support](https://support.hpe.com/)

## Official Documentation Links

### Main Resources
- [CLI Reference Guide for ArubaOS-CX](https://support.hpe.com/hpesc/public/docDisplay?docId=c04793912&docLocale=en_US)
- [Aruba CLI Bank](https://arubanetworking.hpe.com/techdocs/CLI-Bank/Content/Home.htm)
- [ArubaOS 8.6.x CLI Reference Guide](https://www.hpe.com/psnow/doc/a00100140en_us)

### Comparative Guides
- [CLI Reference Guide for ArubaOS-CX, ArubaOS-Switch, and Cisco IOS](https://www.hpe.com/psnow/doc/c04793912)
- [Best CLI Cheat Sheet: Cisco, Aruba CX, and Aruba OS Switch](https://cadinc.com/our-best-cli-cheat-sheet-cisco-aruba-cx-aruba-os-switch/)

## Platform Overview

Aruba has three main CLI platforms:
1. **ArubaOS** - Wireless controllers (Mobility Controllers)
2. **ArubaOS-CX** - Modern data center switches
3. **ArubaOS-Switch** - Traditional campus switches (formerly ProCurve)

---

## ArubaOS (Mobility Controllers) CLI Reference

### Access Methods
- **Console**: Serial connection (9600-8-N-1 or 115200-8-N-1)
- **SSH**: `ssh admin@<controller-ip>`
- **Telnet**: `telnet <controller-ip>`
- **WebUI**: HTTPS web interface

### Command Modes
```
# User mode
(host) >

# Enable mode
(host) #

# Configuration mode
(host) (config) #

# Node-specific mode
(host) [node-path] #
```

### System Information
```
# Show version
(host) # show version

# Show system information
(host) # show switches

# Show CPU utilization
(host) # show cpuload

# Show memory usage
(host) # show memory

# Show uptime
(host) # show uptime
```

### Wireless Commands
```
# Show AP database
(host) # show ap database

# Show AP status
(host) # show ap active

# Show WLAN SSID config
(host) # show wlan ssid-profile

# Show client association
(host) # show user-table

# Show RF summary
(host) # show ap arm rf-summary

# Show channel utilization
(host) # show ap monitor channel-utilization
```

### Configuration Example (ArubaOS Controller)
```
# Enter configuration mode
(host) # configure terminal

# Configure WLAN SSID
(host) (config) # wlan ssid-profile "Corporate-WiFi"
(host) (SSID Profile "Corporate-WiFi") # essid "CorpNet"
(host) (SSID Profile "Corporate-WiFi") # opmode wpa2-aes
(host) (SSID Profile "Corporate-WiFi") # exit

# Configure virtual AP
(host) (config) # wlan virtual-ap "Corp-VAP"
(host) (Virtual AP profile "Corp-VAP") # ssid-profile "Corporate-WiFi"
(host) (Virtual AP profile "Corp-VAP") # vlan 10
(host) (Virtual AP profile "Corp-VAP") # exit

# Commit configuration
(host) (config) # commit apply
```

---

## ArubaOS-CX (Modern Switches) CLI Reference

### Access Methods
- **Console**: Serial connection (115200-8-N-1)
- **SSH**: `ssh admin@<switch-ip>`
- **WebUI**: HTTPS web interface

### Command Modes
```
# Operator mode
switch>

# Manager mode (privileged)
switch#

# Configuration mode
switch(config)#

# Interface configuration mode
switch(config-if)#
```

### Key Features
- **Checkpoint/Rollback**: Similar to JunOS
- **Modular OS**: Linux-based
- **REST API**: Full programmatic access
- **Python/NAE**: Network Analytics Engine

### System Information
```
# Show version
switch# show version

# Show system information
switch# show system

# Show running configuration
switch# show running-config

# Show startup configuration
switch# show startup-config

# Show interface brief
switch# show interface brief

# Show CPU/memory
switch# show system resource-utilization
```

### VLAN Configuration (ArubaOS-CX)
```
# Create VLAN
switch(config)# vlan 10
switch(config-vlan-10)# name Sales
switch(config-vlan-10)# exit

# Assign port to VLAN (access)
switch(config)# interface 1/1/1
switch(config-if)# no shutdown
switch(config-if)# no routing
switch(config-if)# vlan access 10
switch(config-if)# exit

# Configure trunk port
switch(config)# interface 1/1/48
switch(config-if)# no shutdown
switch(config-if)# no routing
switch(config-if)# vlan trunk native 1
switch(config-if)# vlan trunk allowed 10,20,30
switch(config-if)# exit
```

### Layer 3 Interface (SVI) Configuration
```
# Create VLAN interface
switch(config)# interface vlan 10
switch(config-if-vlan)# ip address 192.168.10.1/24
switch(config-if-vlan)# active
switch(config-if-vlan)# exit
```

### Routing Configuration (ArubaOS-CX)
```
# Static route
switch(config)# ip route 0.0.0.0/0 203.0.113.1

# OSPF configuration
switch(config)# router ospf 1
switch(config-ospf-1)# router-id 1.1.1.1
switch(config-ospf-1)# area 0.0.0.0
switch(config-ospf-1)# exit

switch(config)# interface vlan 10
switch(config-if-vlan)# ip ospf 1 area 0.0.0.0
```

### Link Aggregation (LAG) - ArubaOS-CX
```
# Create LAG
switch(config)# interface lag 1
switch(config-lag-if)# no shutdown
switch(config-lag-if)# lacp mode active
switch(config-lag-if)# exit

# Add member ports
switch(config)# interface 1/1/1
switch(config-if)# lag 1
switch(config-if)# exit

switch(config)# interface 1/1/2
switch(config-if)# lag 1
switch(config-if)# exit
```

### Configuration Management (ArubaOS-CX)
```
# Create checkpoint
switch# checkpoint <checkpoint-name>

# Show checkpoints
switch# show checkpoint

# Rollback to checkpoint
switch# rollback <checkpoint-name>

# Copy running to startup
switch# write memory
# or
switch# copy running-config startup-config
```

---

## ArubaOS-Switch (Traditional Campus Switches) CLI Reference

### Access Methods
- **Console**: Serial connection (115200-8-N-1 or 9600-8-N-1)
- **SSH**: `ssh <username>@<switch-ip>`
- **WebUI**: HTTPS web interface

### Command Modes
```
# Manager mode
switch>

# Manager (privileged) mode
switch#

# Configuration mode
switch(config)#

# Interface configuration mode
switch(eth-1)#

# VLAN configuration mode
switch(vlan-10)#
```

### System Information
```
# Show version
switch# show version

# Show system information
switch# show system

# Show running configuration
switch# show running-config

# Show tech (comprehensive diagnostics)
switch# show tech

# Show MAC address table
switch# show mac-address
```

### VLAN Configuration (ArubaOS-Switch)
```
# Create VLAN
switch(config)# vlan 10
switch(vlan-10)# name "Sales"
switch(vlan-10)# untagged 1-12
switch(vlan-10)# tagged 24
switch(vlan-10)# ip address 192.168.10.1 255.255.255.0
switch(vlan-10)# exit

# Alternative method - assign ports individually
switch(config)# vlan 20 name "Engineering"
switch(config)# interface ethernet 13-20
switch(config-if-eth-range)# vlan 20 untagged
```

### Trunking (ArubaOS-Switch)
```
# Configure trunk port
switch(config)# vlan 10 tagged 24
switch(config)# vlan 20 tagged 24
switch(config)# vlan 30 tagged 24
```

### Spanning Tree
```
# Enable MSTP
switch(config)# spanning-tree

# Show spanning tree
switch# show spanning-tree

# Set priority
switch(config)# spanning-tree priority 4096
```

### Routing Configuration (ArubaOS-Switch)
```
# Enable IP routing
switch(config)# ip routing

# Static route
switch(config)# ip route 0.0.0.0 0.0.0.0 203.0.113.1

# OSPF configuration
switch(config)# router ospf
switch(ospf)# area 0.0.0.0
switch(ospf)# enable
switch(ospf)# exit

switch(config)# vlan 10
switch(vlan-10)# ip ospf area 0.0.0.0
```

### Link Aggregation (LAG/Trunk) - ArubaOS-Switch
```
# Create trunk (LAG)
switch(config)# trunk 1-4 trk1 lacp

# Show trunk status
switch# show trunk

# Configure trunk VLAN membership
switch(config)# vlan 10 tagged trk1
```

### ACL Configuration (ArubaOS-Switch)
```
# Create ACL
switch(config)# ip access-list extended "WEB-TRAFFIC"
switch(config-ext-nacl)# permit tcp any any eq 80
switch(config-ext-nacl)# permit tcp any any eq 443
switch(config-ext-nacl)# deny ip any any
switch(config-ext-nacl)# exit

# Apply to VLAN
switch(config)# vlan 10
switch(vlan-10)# ip access-group "WEB-TRAFFIC" in
```

### Configuration Management (ArubaOS-Switch)
```
# Save configuration
switch# write memory

# Show startup configuration
switch# show config

# Show running configuration
switch# show running-config

# Copy configuration to TFTP
switch# copy running-config tftp 192.168.1.100 backup.cfg

# Restore from TFTP
switch# copy tftp running-config 192.168.1.100 backup.cfg
```

---

## Common Troubleshooting Commands

### ArubaOS Controller
```
# Ping
(host) # ping <destination-ip>

# Traceroute
(host) # traceroute <destination-ip>

# Show logs
(host) # show log system 100

# Debug commands
(host) # show datapath session
(host) # show datapath user
```

### ArubaOS-CX Switch
```
# Ping
switch# ping <destination-ip>

# Traceroute
switch# traceroute <destination-ip>

# Show LLDP neighbors
switch# show lldp neighbor-info

# Show MAC table
switch# show mac-address-table

# Show ARP table
switch# show arp

# Show interface statistics
switch# show interface 1/1/1
```

### ArubaOS-Switch
```
# Ping
switch# ping <destination-ip>

# Traceroute
switch# traceroute <destination-ip>

# Show LLDP neighbors
switch# show lldp info remote-device

# Show MAC table
switch# show mac-address

# Show ARP table
switch# show arp

# Show interface statistics
switch# show interfaces 1
```

## Safety Considerations

### Destructive Commands
⚠️ **WARNING**: The following commands can cause service disruption:

**ArubaOS Controller:**
- `reload` - Reboots the controller
- `write erase` - Erases configuration

**ArubaOS-CX:**
- `boot system` - Changes boot image
- `erase startup-config` - Erases startup config
- `erase all` - Factory reset

**ArubaOS-Switch:**
- `reload` - Reboots the switch
- `erase startup-config` - Erases startup config

### Best Practices
1. **Backup configurations**: Regular backups before changes
2. **Use checkpoints** (ArubaOS-CX): Create checkpoint before major changes
3. **Test in lab**: Complex configurations should be tested first
4. **Console access**: Keep console cable available
5. **Commit apply** (ArubaOS): Use `commit apply` instead of `write memory`
6. **Staged deployment**: Test on one device before mass deployment

---

## Platform Comparison

| Feature | ArubaOS (Controller) | ArubaOS-CX | ArubaOS-Switch |
|---------|---------------------|------------|----------------|
| Primary Use | Wireless Controllers | Data Center | Campus |
| Config Syntax | Custom | Modern/Linux | Classic |
| Rollback | Limited | Checkpoint | Limited |
| API | REST | REST | REST |
| Automation | Python | Python/NAE | Limited |

---

## Aruba vs Cisco Comparison

| Function | ArubaOS-CX | Cisco IOS |
|----------|-----------|-----------|
| Config mode | `configure terminal` | `configure terminal` |
| Show config | `show running-config` | `show running-config` |
| Save config | `write memory` | `copy run start` |
| VLAN create | `vlan 10` | `vlan 10` |
| Access port | `vlan access 10` | `switchport access vlan 10` |
| Show int brief | `show interface brief` | `show ip int brief` |

| Function | ArubaOS-Switch | Cisco IOS |
|----------|---------------|-----------|
| Config mode | Similar | `configure terminal` |
| VLAN ports | `vlan 10 untagged 1-12` | Per-port config |
| Save | `write memory` | `copy run start` |
| Interface | `interface 1` | `interface g0/1` |

---

## Additional Resources

- [HPE Aruba Support Portal](https://support.hpe.com/)
- [Aruba Airheads Community](https://community.arubanetworks.com/)
- [Aruba Learning Center](https://www.arubanetworks.com/support-services/training-services/)
- [Aruba CLI Bank](https://arubanetworking.hpe.com/techdocs/CLI-Bank/)

---

## Quick Tips

### ArubaOS Controller
- Use tab completion for commands
- Configuration requires `commit apply` to take effect
- Use `show switchinfo` for controller details

### ArubaOS-CX
- Very similar to Cisco NX-OS
- Excellent checkpoint/rollback capability
- Built-in Python for automation
- Use `?` for context help

### ArubaOS-Switch
- Similar to older ProCurve switches
- VLAN configuration is interface-group based
- Simple, reliable platform
- Good for campus deployments

---

*Note: Aruba platforms have different CLI syntaxes. Always verify commands for your specific Aruba platform (ArubaOS, ArubaOS-CX, or ArubaOS-Switch) and software version.*
