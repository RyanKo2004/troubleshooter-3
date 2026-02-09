# Cisco NX-OS CLI Reference

**Last Updated**: 2026-02-09
**Latest Version**: NX-OS 10.5(x)
**Source**: [Cisco NX-OS Software Command References](https://www.cisco.com/c/en/us/support/ios-nx-os-software/nx-os-software/products-command-reference-list.html)

## Official Documentation Links

### Main Resources
- [Cisco NX-OS Software Command References](https://www.cisco.com/c/en/us/support/ios-nx-os-software/nx-os-software/products-command-reference-list.html)
- [Cisco Nexus 9000 Series Command References](https://www.cisco.com/c/en/us/support/switches/nexus-9000-series-switches/products-command-reference-list.html)
- [Cisco Nexus 7000 Series Command References](https://www.cisco.com/c/en/us/support/switches/nexus-7000-series-switches/products-command-reference-list.html)

### Release-Specific
- [Nexus 9000 NX-OS 10.2(x) Configuration Commands](https://www.cisco.com/c/en/us/td/docs/dcn/nx-os/nexus9000/102x/command-reference/config/b_n9k_config_commands_1021.html)
- [Nexus 9000 NX-OS 9.3(x) Command Reference](https://www.cisco.com/c/en/us/td/docs/switches/datacenter/nexus9000/sw/93x/command/reference/config/b_N9K_Config_Commands_93x.html)

## CLI Basics

### Access Methods
- **Console**: Serial connection (9600-8-N-1)
- **SSH**: `ssh admin@<switch-ip>`
- **Telnet**: Not recommended for security

### Command Modes
```
# User EXEC mode
switch>

# Privileged EXEC mode
switch#

# Global configuration mode
switch(config)#

# Interface configuration mode
switch(config-if)#

# VLAN configuration mode
switch(config-vlan)#
```

### Key Differences from IOS
- **Automatic config save**: Changes are immediately saved
- **Rollback capability**: Built-in configuration rollback
- **VDC support**: Virtual Device Contexts (Nexus 7000)
- **Enhanced scripting**: Python and Bash support

## Common Troubleshooting Commands

### System Information
```
# Show version
show version

# Show hardware
show hardware

# Show module status
show module

# Show system uptime
show system uptime

# Show system resources
show system resources

# Show processes CPU
show processes cpu sort

# Show environment
show environment
```

### Interface Commands
```
# Show interface brief
show interface brief

# Show interface status
show interface status

# Show specific interface
show interface <interface>

# Show interface counters
show interface counters

# Show interface errors
show interface counters errors

# Show transceiver info
show interface transceiver

# Show port-channel summary
show port-channel summary
```

### VLAN & Layer 2
```
# Show VLANs
show vlan

# Show VLAN brief
show vlan brief

# Show spanning-tree
show spanning-tree

# Show spanning-tree summary
show spanning-tree summary

# Show MAC address table
show mac address-table

# Show VTP status (if enabled)
show vtp status
```

### Routing (Layer 3)
```
# Show IP interface brief
show ip interface brief

# Show routing table
show ip route

# Show routing protocols
show ip protocols

# Show OSPF neighbors
show ip ospf neighbors

# Show OSPF database
show ip ospf database

# Show BGP summary
show ip bgp summary

# Show BGP neighbors
show ip bgp neighbors

# Show EIGRP neighbors
show ip eigrp neighbors
```

### Virtual Port Channel (vPC)
```
# Show vPC status
show vpc

# Show vPC brief
show vpc brief

# Show vPC consistency
show vpc consistency-parameters global

# Show vPC role
show vpc role
```

### Fabric Extender (FEX)
```
# Show FEX status
show fex

# Show FEX detail
show fex detail

# Show FEX interfaces
show interface fex-fabric
```

### Virtual Device Context (VDC) - Nexus 7000
```
# Show VDCs
show vdc

# Show current VDC
show vdc current-vdc

# Switch to VDC
switchto vdc <vdc-name>
```

### High Availability
```
# Show system redundancy status
show system redundancy status

# Show module status
show module

# Force switchover
system switchover
```

## Configuration Examples

### Basic Interface Configuration
```
switch(config)# interface Ethernet1/1
switch(config-if)# description Server Connection
switch(config-if)# no switchport
switch(config-if)# ip address 192.168.1.1/24
switch(config-if)# no shutdown
```

### VLAN Configuration
```
# Create VLAN
switch(config)# vlan 10
switch(config-vlan)# name Sales

# Assign interface to VLAN
switch(config)# interface Ethernet1/10
switch(config-if)# switchport mode access
switch(config-if)# switchport access vlan 10
```

### Trunk Configuration
```
switch(config)# interface Ethernet1/1
switch(config-if)# switchport mode trunk
switch(config-if)# switchport trunk allowed vlan 10,20,30
```

### Port-Channel (LAG) Configuration
```
# Create port-channel
switch(config)# interface port-channel 10
switch(config-if)# switchport mode trunk
switch(config-if)# switchport trunk allowed vlan 10,20,30

# Add members to port-channel
switch(config)# interface Ethernet1/1-2
switch(config-if-range)# channel-group 10 mode active
```

### vPC Configuration
```
# Enable features
switch(config)# feature vpc
switch(config)# feature lacp

# Configure vPC domain
switch(config)# vpc domain 1
switch(config-vpc-domain)# peer-keepalive destination 10.1.1.2 source 10.1.1.1
switch(config-vpc-domain)# peer-gateway

# Configure peer-link
switch(config)# interface port-channel 1
switch(config-if)# switchport mode trunk
switch(config-if)# vpc peer-link

# Configure vPC port-channel
switch(config)# interface port-channel 10
switch(config-if)# switchport mode trunk
switch(config-if)# vpc 10
```

### OSPF Configuration
```
# Enable OSPF feature
switch(config)# feature ospf

# Configure OSPF
switch(config)# router ospf 1
switch(config-router)# router-id 1.1.1.1

# Add interface to OSPF
switch(config)# interface Ethernet1/1
switch(config-if)# ip router ospf 1 area 0.0.0.0
```

### BGP Configuration
```
# Enable BGP feature
switch(config)# feature bgp

# Configure BGP
switch(config)# router bgp 65001
switch(config-router)# router-id 1.1.1.1
switch(config-router)# neighbor 192.168.1.2 remote-as 65002
switch(config-router)# address-family ipv4 unicast
```

## Configuration Management

### Checkpoint & Rollback
```
# Create checkpoint
checkpoint <checkpoint-name>

# Show checkpoints
show checkpoint summary

# Rollback to checkpoint
rollback running-config checkpoint <checkpoint-name>

# Delete checkpoint
no checkpoint <checkpoint-name>
```

### Configuration Copy
```
# Save running config
copy running-config startup-config

# Backup to file
copy running-config bootflash:backup-config.cfg

# Copy to remote server
copy running-config scp://user@server/path/config.cfg

# Restore configuration
copy bootflash:backup-config.cfg running-config
```

### Configuration Sessions
```
# Start configuration session
configure session <session-name>

# Verify changes
verify

# Commit changes
commit

# Abort session
abort
```

## Debugging & Troubleshooting

### Logging
```
# Show logging
show logging

# Show logging last messages
show logging last 100

# Configure logging
switch(config)# logging server 192.168.1.100
switch(config)# logging level 6
```

### Debugging
```
# Enable debugging
debug <component>

# Common debug commands
debug port-channel all
debug vpc all
debug spanning-tree all

# Show active debugs
show debugging

# Disable all debugs
no debug all
```

### Packet Capture (SPAN)
```
# Create SPAN session
switch(config)# monitor session 1
switch(config-monitor)# source interface Ethernet1/1
switch(config-monitor)# destination interface Ethernet1/48
switch(config-monitor)# no shut

# Show SPAN sessions
show monitor session all
```

### Ethanalyzer (Built-in Packet Capture)
```
# Capture packets
ethanalyzer local interface mgmt capture-filter "host 192.168.1.1"

# Capture and display
ethanalyzer local interface mgmt display-filter "tcp.port==22"
```

## Safety Considerations

### Destructive Commands
⚠️ **WARNING**: The following commands can cause service disruption:
- `reload` - Reboots the switch
- `write erase` - Erases configuration
- `install all` - Installs new software (causes reload)
- `clear` commands - Clear various tables/counters
- `no feature <feature>` - Disables features (may remove config)

### Best Practices
1. **Use checkpoints**: Create checkpoints before major changes
2. **Use configuration sessions**: Allows verification before commit
3. **Test in VDC**: Use VDC for testing (Nexus 7000)
4. **Schedule maintenance**: Plan changes during maintenance windows
5. **Keep console access**: Always have console during critical changes
6. **Backup configs**: Regular configuration backups

### Rollback Safety
```
# Automatic rollback on error
configure session MySession
  interface Ethernet1/1
    ip address 10.1.1.1/24
  verify
  commit

# Manual checkpoint and rollback
checkpoint pre-change
<make changes>
# If issues occur:
rollback running-config checkpoint pre-change
```

## Python Scripting

### Enable Python
```
# Enable feature
feature bash-shell

# Access Python
python

# Run Python script
python bootflash:script.py
```

### Example Python Script
```python
from cli import *

# Execute CLI command
output = cli("show version")
print(output)

# Configuration commands
cli("configure terminal ; interface Ethernet1/1 ; description Python-Config")
```

## Virtual Shell (Bash)

### Access Bash Shell
```
# Enter bash
run bash

# Run bash command
run bash ls -la /bootflash

# View system processes
run bash ps aux
```

## NX-OS vs IOS Comparison

| Feature | IOS | NX-OS |
|---------|-----|-------|
| Config Save | Manual (`copy run start`) | Automatic |
| Rollback | Limited | Built-in checkpoints |
| Scripting | TCL | Python, Bash |
| Modularity | Monolithic | Modular (features) |
| VDC | No | Yes (Nexus 7000) |
| vPC | VSS | vPC |

## Platform-Specific Notes

### Nexus 9000
- ACI and NX-OS modes
- VXLAN support
- High-density 100G ports

### Nexus 7000
- VDC support
- OTV for data center interconnect
- FabricPath

### Nexus 5000/6000
- Unified Fabric (FCoE)
- FEX support
- Compact data center switches

## Additional Resources

- [Cisco NX-OS Documentation Portal](https://www.cisco.com/c/en/us/support/ios-nx-os-software/nx-os-software/tsd-products-support-series-home.html)
- [Cisco Data Center Community](https://community.cisco.com/t5/data-center/ct-p/4481-discussions-datacenter)
- [NX-OS Command Reference Net](https://cmdref.net/hardware/cisco/index.html)

---
*Note: NX-OS syntax and features vary by platform and version. Always verify commands for your specific Nexus platform and NX-OS version.*
