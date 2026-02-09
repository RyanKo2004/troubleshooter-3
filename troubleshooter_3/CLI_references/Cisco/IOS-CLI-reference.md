# Cisco IOS CLI Reference

**Last Updated**: 2026-02-09
**Latest Documentation Update**: January 15, 2026
**Source**: [Cisco IOS Command Reference](https://www.cisco.com/c/en/us/td/docs/ios/fundamentals/command/reference/cf_book.html)

## Official Documentation Links

### Main Resources
- [Cisco IOS Configuration Fundamentals Command Reference](https://www.cisco.com/c/en/us/td/docs/ios/fundamentals/command/reference/cf_book.html)
- [Cisco IOS Master Command List (All Releases)](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/mcl/allreleasemcl/all-book.html)
- [Cisco IOS Configuration Fundamentals PDF](https://www.cisco.com/c/en/us/td/docs/ios/fundamentals/command/reference/cf_book.pdf)

### Specialized References
- [Cisco IOS Network Management Command Reference](https://www.cisco.com/c/en/us/support/ios-nx-os-software/ios-software/products-command-reference-list.html)
- [Cisco IOS IP SLAs Command Reference](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/ipsla/command/sla-cr-book.html)
- [Cisco IOS LAN Switching Command Reference](https://www.cisco.com/c/en/us/td/docs/ios-xml/ios/lanswitch/command/lsw-cr-book.html)

## CLI Basics

### Access Methods
- **Console**: Serial connection (9600-8-N-1)
- **SSH**: `ssh -l <username> <router-ip>`
- **Telnet**: `telnet <router-ip>` (not recommended)

### Privilege Levels
```
# User EXEC mode (privilege level 1)
Router>

# Privileged EXEC mode (privilege level 15)
Router# (enter with 'enable' command)

# Global configuration mode
Router(config)#

# Interface configuration mode
Router(config-if)#

# Router configuration mode
Router(config-router)#
```

### Context Help
```
# Show available commands
?

# Show command options
command ?

# Complete partial command
<partial-command><Tab>
```

## Common Troubleshooting Commands

### System Information
```
# Show version and hardware info
show version

# Show running configuration
show running-config

# Show startup configuration
show startup-config

# Show system uptime and reload reason
show version | include uptime|reload

# Show CPU utilization
show processes cpu sorted

# Show memory usage
show memory

# Show environment (temperature, power)
show environment all
```

### Interface Commands
```
# Show all interfaces summary
show ip interface brief

# Show detailed interface info
show interface <interface>

# Show interface statistics
show interface <interface> stats

# Show interface errors
show interface <interface> | include error

# Show interface status (switches)
show interface status

# Show port statistics (switches)
show interface counters errors
```

### Routing
```
# Show routing table
show ip route

# Show specific route
show ip route <network>

# Show routing protocols
show ip protocols

# Show OSPF neighbors
show ip ospf neighbor

# Show OSPF database
show ip ospf database

# Show BGP summary
show ip bgp summary

# Show BGP neighbors
show ip bgp neighbors

# Show EIGRP neighbors
show ip eigrp neighbors
```

### Switching (Layer 2)
```
# Show MAC address table
show mac address-table

# Show VLAN information
show vlan brief

# Show VTP status
show vtp status

# Show spanning-tree status
show spanning-tree

# Show trunk interfaces
show interface trunk

# Show port-channel summary
show etherchannel summary
```

### Sessions & Connections
```
# Show active sessions
show sessions

# Show TCP connections
show tcp brief

# Show NAT translations
show ip nat translations

# Show NAT statistics
show ip nat statistics
```

### Access Control Lists (ACLs)
```
# Show all ACLs
show access-lists

# Show specific ACL
show access-lists <acl-number|name>

# Show ACL applied to interface
show ip interface <interface> | include access list
```

### Debugging
```
# Enable debugging (be careful - can impact performance)
debug ip packet
debug ip routing
debug ip ospf events
debug ip bgp

# Disable all debugging
undebug all (or) no debug all

# Show active debugs
show debugging
```

### Logging
```
# Show log messages
show logging

# Show log buffer
show logging | include <search-term>

# Clear logging buffer
clear logging
```

## Configuration Examples

### Basic Interface Configuration
```
Router(config)# interface GigabitEthernet0/0
Router(config-if)# ip address 192.168.1.1 255.255.255.0
Router(config-if)# description LAN Interface
Router(config-if)# no shutdown
Router(config-if)# exit
```

### Static Route
```
Router(config)# ip route 10.0.0.0 255.255.255.0 192.168.1.254
```

### OSPF Configuration
```
Router(config)# router ospf 1
Router(config-router)# network 192.168.1.0 0.0.0.255 area 0
Router(config-router)# network 10.0.0.0 0.0.0.255 area 0
Router(config-router)# exit
```

### Standard ACL
```
Router(config)# access-list 10 permit 192.168.1.0 0.0.0.255
Router(config)# access-list 10 deny any

# Apply to interface
Router(config)# interface GigabitEthernet0/1
Router(config-if)# ip access-group 10 in
```

### Extended ACL
```
Router(config)# ip access-list extended WEB-TRAFFIC
Router(config-ext-nacl)# permit tcp any any eq 80
Router(config-ext-nacl)# permit tcp any any eq 443
Router(config-ext-nacl)# deny ip any any
Router(config-ext-nacl)# exit

# Apply to interface
Router(config)# interface GigabitEthernet0/1
Router(config-if)# ip access-group WEB-TRAFFIC out
```

### NAT Configuration (PAT)
```
# Define inside/outside interfaces
Router(config)# interface GigabitEthernet0/0
Router(config-if)# ip nat inside

Router(config)# interface GigabitEthernet0/1
Router(config-if)# ip nat outside

# Configure PAT
Router(config)# access-list 1 permit 192.168.1.0 0.0.0.255
Router(config)# ip nat inside source list 1 interface GigabitEthernet0/1 overload
```

### VLAN Configuration (Switch)
```
# Create VLAN
Switch(config)# vlan 10
Switch(config-vlan)# name Sales
Switch(config-vlan)# exit

# Assign port to VLAN
Switch(config)# interface FastEthernet0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10
```

### Trunk Configuration (Switch)
```
Switch(config)# interface GigabitEthernet0/1
Switch(config-if)# switchport trunk encapsulation dot1q
Switch(config-if)# switchport mode trunk
Switch(config-if)# switchport trunk allowed vlan 10,20,30
```

## Configuration Management

### Save Configuration
```
# Save running config to startup config
copy running-config startup-config
# or
write memory
# or
wr
```

### Backup Configuration
```
# Copy to TFTP server
copy running-config tftp://192.168.1.100/router-config.txt

# Copy to FTP server
copy running-config ftp://username:password@192.168.1.100/router-config.txt
```

### Restore Configuration
```
# Copy from TFTP server
copy tftp://192.168.1.100/router-config.txt running-config
```

## Safety Considerations

### Destructive Commands
⚠️ **WARNING**: The following commands can cause service disruption:
- `reload` - Reboots the device
- `erase startup-config` - Erases saved configuration
- `write erase` - Erases saved configuration
- `delete flash:` - Deletes files from flash
- `format flash:` - Formats the flash filesystem
- `clear line <line-number>` - Disconnects active sessions

### Best Practices
1. **Always save configuration before testing**: `copy running-config startup-config`
2. **Use `reload in <minutes>`**: Provides automatic rollback if connection is lost
3. **Test ACLs carefully**: Wrong ACL can lock you out
4. **Verify before reloading**: `show running-config` before `reload`
5. **Use configuration archive**: Enable config archive for rollback capability
6. **Keep console access**: Always have console access during critical changes

### Configuration Rollback
```
# Configure archive
Router(config)# archive
Router(config-archive)# path flash:config-backup
Router(config-archive)# maximum 14
Router(config-archive)# time-period 1440

# View archived configs
show archive

# Rollback to previous config
configure replace flash:config-backup-1
```

## Useful Command Shortcuts

### Output Modifiers
```
# Show specific section
show running-config | section interface

# Search for keyword
show running-config | include <keyword>

# Exclude lines
show running-config | exclude !

# Begin output from match
show running-config | begin interface
```

### Common Shortcuts
```
conf t          # configure terminal
int gi0/0       # interface GigabitEthernet0/0
ip add          # ip address
no shut         # no shutdown
wr              # write memory
sh              # show
sh ip int br    # show ip interface brief
sh run          # show running-config
```

## Password Recovery

### Router Password Recovery
1. Power cycle and press Break during boot
2. `confreg 0x2142` (bypass startup-config)
3. `reset`
4. After boot: `copy startup-config running-config`
5. Change password: `enable secret <new-password>`
6. Restore config register: `config-register 0x2102`
7. Save: `write memory`
8. Reload

### Switch Password Recovery
1. Hold Mode button during boot until LED flashes
2. Initialize flash: `flash_init`
3. Rename config: `rename flash:config.text flash:config.old`
4. Boot: `boot`
5. Restore and change password
6. Rename back: `rename flash:config.old flash:config.text`

## Platform-Specific Considerations

### IOS vs IOS-XE
- **IOS**: Traditional Cisco IOS (monolithic)
- **IOS-XE**: Linux-based, modular architecture
- Most commands are the same, but IOS-XE has additional features

### Common Issues
- Command variations between IOS versions
- Feature availability depends on license and platform
- Some commands require specific hardware support

## Additional Resources

- [Cisco Command Lookup Tool](https://www.cisco.com/c/en/us/support/index.html)
- [Cisco Learning Network](https://learningnetwork.cisco.com/)
- [Cisco Support Community](https://community.cisco.com/)

---
*Note: Commands may vary between IOS versions and platforms. Always verify command syntax for your specific IOS version using `?` context help.*
