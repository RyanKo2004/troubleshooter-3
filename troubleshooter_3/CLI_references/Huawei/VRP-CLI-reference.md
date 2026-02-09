# Huawei VRP (Versatile Routing Platform) CLI Reference

**Last Updated**: 2026-02-09
**Platform**: Huawei AR Series, NE Series, S Series Switches
**Source**: [Huawei Enterprise Support](https://support.huawei.com/enterprise/)

## Official Documentation Links

### Main Resources
- [Huawei Enterprise Support Portal](https://support.huawei.com/enterprise/en/index.html)
- [AR Router Command Reference](https://support.huawei.com/enterprise/en/doc/EDOC1000174046/bbd0bc8e/cli-overview-commands)
- [Huawei VRP NED Documentation](https://nso-docs.cisco.com/neds/cisco-provided-neds/huawei-vrp/huawei-vrp)

### Educational Resources
- [Huawei VRP Command Cheat Sheet](https://www.scribd.com/document/196491929/Huawei-VRP-Command-Cheat-Sheet)
- [Huawei CLI Introduction](https://labnario.com/huawei-cli-introduction/)

## CLI Basics

### Access Methods
- **Console**: Serial connection (9600-8-N-1 or 115200-8-N-1)
- **Telnet**: `telnet <device-ip>`
- **SSH**: `ssh <username>@<device-ip>`
- **Web UI**: HTTP/HTTPS management interface

### User Levels
VRP has multiple user privilege levels (0-15):
- **Level 0**: Visit level (basic commands like ping)
- **Level 1**: Monitoring level (display commands)
- **Level 2**: Configuration level (service configuration)
- **Level 3-15**: Management level (system management, user management)

### Command Views
```
# User view (after login)
<Huawei>

# System view (configuration mode)
[Huawei]

# Interface view
[Huawei-GigabitEthernet0/0/1]

# Protocol view (e.g., OSPF)
[Huawei-ospf-1]

# VLAN view
[Huawei-vlan10]
```

### Basic Navigation
```
# Enter system view
system-view

# Return to user view
quit (or return)

# Show command options
?

# Command completion
<Tab>

# Command abbreviation
dis cur  (short for display current-configuration)
```

## Common Troubleshooting Commands

### System Information
```
# Show version information
display version

# Show device information
display device

# Show system uptime
display clock

# Show CPU usage
display cpu-usage

# Show memory usage
display memory-usage

# Show device temperature
display temperature

# Show power supply
display power
```

### Interface Commands
```
# Show all interfaces brief
display interface brief

# Show specific interface
display interface GigabitEthernet 0/0/1

# Show IP interface brief
display ip interface brief

# Show interface statistics
display interface GigabitEthernet 0/0/1 statistics

# Reset interface counters
reset counters interface GigabitEthernet 0/0/1
```

### VLAN & Switching
```
# Show VLAN information
display vlan

# Show VLAN summary
display vlan summary

# Show MAC address table
display mac-address

# Show STP information
display stp brief

# Show port status
display port vlan

# Show trunk interfaces
display interface trunk
```

### Routing
```
# Show routing table
display ip routing-table

# Show static routes
display ip routing-table protocol static

# Show OSPF neighbors
display ospf peer brief

# Show OSPF routing table
display ospf routing

# Show OSPF database
display ospf lsdb

# Show BGP peer status
display bgp peer

# Show BGP routing table
display bgp routing-table

# Show RIP status
display rip route
```

### ACL & Security
```
# Show ACL configuration
display acl all

# Show specific ACL
display acl <acl-number>

# Show traffic policy
display traffic policy applied-record

# Show firewall sessions
display firewall session table
```

### Diagnostics
```
# Ping
ping <destination-ip>
ping -c 5 -s 1000 <destination-ip>

# Traceroute
tracert <destination-ip>

# Test connectivity with source
ping -a <source-ip> <destination-ip>

# ARP table
display arp

# ARP for specific interface
display arp interface GigabitEthernet 0/0/1
```

## Configuration Examples

### Basic Interface Configuration
```
[Huawei] interface GigabitEthernet 0/0/1
[Huawei-GigabitEthernet0/0/1] description LAN Interface
[Huawei-GigabitEthernet0/0/1] ip address 192.168.1.1 255.255.255.0
[Huawei-GigabitEthernet0/0/1] undo shutdown
[Huawei-GigabitEthernet0/0/1] quit
```

### VLAN Configuration (Switch)
```
# Create VLAN
[Huawei] vlan 10
[Huawei-vlan10] description Sales Department
[Huawei-vlan10] quit

# Assign port to VLAN (access mode)
[Huawei] interface GigabitEthernet 0/0/1
[Huawei-GigabitEthernet0/0/1] port link-type access
[Huawei-GigabitEthernet0/0/1] port default vlan 10
[Huawei-GigabitEthernet0/0/1] quit

# Configure trunk port
[Huawei] interface GigabitEthernet 0/0/24
[Huawei-GigabitEthernet0/0/24] port link-type trunk
[Huawei-GigabitEthernet0/0/24] port trunk allow-pass vlan 10 20 30
[Huawei-GigabitEthernet0/0/24] quit
```

### VLAN Interface (SVI)
```
[Huawei] interface Vlanif 10
[Huawei-Vlanif10] ip address 192.168.10.1 255.255.255.0
[Huawei-Vlanif10] quit
```

### Static Route
```
[Huawei] ip route-static 10.0.0.0 255.255.255.0 192.168.1.254
[Huawei] ip route-static 0.0.0.0 0.0.0.0 203.0.113.1
```

### OSPF Configuration
```
# Enable OSPF
[Huawei] ospf 1 router-id 1.1.1.1
[Huawei-ospf-1] area 0
[Huawei-ospf-1-area-0.0.0.0] network 192.168.1.0 0.0.0.255
[Huawei-ospf-1-area-0.0.0.0] network 10.0.0.0 0.0.0.255
[Huawei-ospf-1-area-0.0.0.0] quit
[Huawei-ospf-1] quit
```

### BGP Configuration
```
[Huawei] bgp 65001
[Huawei-bgp] router-id 1.1.1.1
[Huawei-bgp] peer 192.168.1.2 as-number 65002
[Huawei-bgp] ipv4-family unicast
[Huawei-bgp-af-ipv4] peer 192.168.1.2 enable
[Huawei-bgp-af-ipv4] network 10.0.0.0 255.255.255.0
[Huawei-bgp-af-ipv4] quit
[Huawei-bgp] quit
```

### ACL Configuration
```
# Basic ACL (2000-2999)
[Huawei] acl 2000
[Huawei-acl-basic-2000] rule permit source 192.168.1.0 0.0.0.255
[Huawei-acl-basic-2000] rule deny source any
[Huawei-acl-basic-2000] quit

# Advanced ACL (3000-3999)
[Huawei] acl 3000
[Huawei-acl-adv-3000] rule permit tcp source 192.168.1.0 0.0.0.255 destination any destination-port eq 80
[Huawei-acl-adv-3000] rule permit tcp source 192.168.1.0 0.0.0.255 destination any destination-port eq 443
[Huawei-acl-adv-3000] rule deny ip source any destination any
[Huawei-acl-adv-3000] quit

# Apply ACL to interface
[Huawei] interface GigabitEthernet 0/0/1
[Huawei-GigabitEthernet0/0/1] traffic-filter inbound acl 3000
[Huawei-GigabitEthernet0/0/1] quit
```

### NAT Configuration
```
# NAT outbound (PAT/NAT overload)
[Huawei] acl 2000
[Huawei-acl-basic-2000] rule permit source 192.168.1.0 0.0.0.255
[Huawei-acl-basic-2000] quit

[Huawei] interface GigabitEthernet 0/0/1
[Huawei-GigabitEthernet0/0/1] nat outbound 2000

# Static NAT (1-to-1)
[Huawei] interface GigabitEthernet 0/0/1
[Huawei-GigabitEthernet0/0/1] nat static global 203.0.113.10 inside 192.168.1.10
```

### Link Aggregation (Eth-Trunk)
```
# Create Eth-Trunk
[Huawei] interface Eth-Trunk 1
[Huawei-Eth-Trunk1] description Link Aggregation to Core
[Huawei-Eth-Trunk1] quit

# Add member interfaces
[Huawei] interface GigabitEthernet 0/0/1
[Huawei-GigabitEthernet0/0/1] eth-trunk 1
[Huawei-GigabitEthernet0/0/1] quit

[Huawei] interface GigabitEthernet 0/0/2
[Huawei-GigabitEthernet0/0/2] eth-trunk 1
[Huawei-GigabitEthernet0/0/2] quit
```

### DHCP Server Configuration
```
# Enable DHCP
[Huawei] dhcp enable

# Create DHCP pool
[Huawei] ip pool VLAN10
[Huawei-ip-pool-VLAN10] network 192.168.10.0 mask 255.255.255.0
[Huawei-ip-pool-VLAN10] gateway-list 192.168.10.1
[Huawei-ip-pool-VLAN10] dns-list 8.8.8.8 8.8.4.4
[Huawei-ip-pool-VLAN10] lease day 7
[Huawei-ip-pool-VLAN10] quit

# Apply DHCP to interface
[Huawei] interface Vlanif 10
[Huawei-Vlanif10] dhcp select global
[Huawei-Vlanif10] quit
```

## Configuration Management

### Save Configuration
```
# Save current configuration
<Huawei> save
# System will prompt: Are you sure? [Y/N]
# Enter: Y

# Save without prompt
<Huawei> save safely
```

### Backup & Restore Configuration
```
# Display current configuration
<Huawei> display current-configuration

# Display saved configuration
<Huawei> display saved-configuration

# Backup to TFTP
[Huawei] tftp <tftp-server-ip> put vrpcfg.zip backup-config.zip

# Restore from TFTP
[Huawei] tftp <tftp-server-ip> get backup-config.zip vrpcfg.zip

# Reset to factory defaults
<Huawei> reset saved-configuration
<Huawei> reboot
```

### Configuration Rollback
```
# Enable configuration rollback
[Huawei] configure commit delay 5
# Makes changes that will auto-rollback in 5 minutes if not confirmed

# Confirm changes (prevent rollback)
[Huawei] configure commit

# Manual rollback to previous config
[Huawei] rollback configuration to label <label-name>
```

## User Management

### Create User
```
# Local user for SSH/Telnet
[Huawei] aaa
[Huawei-aaa] local-user admin password cipher Admin@123
[Huawei-aaa] local-user admin privilege level 15
[Huawei-aaa] local-user admin service-type ssh telnet terminal
[Huawei-aaa] quit
```

### Configure SSH
```
# Generate RSA keys
[Huawei] rsa local-key-pair create

# Enable SSH
[Huawei] ssh server enable

# Configure VTY for SSH
[Huawei] user-interface vty 0 4
[Huawei-ui-vty0-4] authentication-mode aaa
[Huawei-ui-vty0-4] protocol inbound ssh
[Huawei-ui-vty0-4] quit
```

## Debugging & Logging

### Logging
```
# Show logs
<Huawei> display logbuffer

# Configure syslog server
[Huawei] info-center enable
[Huawei] info-center loghost 192.168.1.100

# Set log level
[Huawei] info-center source default channel loghost log level informational
```

### Debugging
```
# Enable debugging
<Huawei> debugging ospf packet
<Huawei> debugging bgp all

# Show debugging status
<Huawei> display debugging

# Disable debugging
<Huawei> undo debugging all
```

### Monitor Terminal Output
```
# Enable terminal monitoring (see real-time logs)
<Huawei> terminal monitor
<Huawei> terminal debugging

# Disable terminal monitoring
<Huawei> undo terminal monitor
<Huawei> undo terminal debugging
```

## Safety Considerations

### Destructive Commands
⚠️ **WARNING**: The following commands can cause service disruption:
- `reboot` - Reboots the device
- `reset saved-configuration` - Erases saved configuration
- `undo` commands - Removes configuration (use carefully)
- `clear` commands - Clears tables/counters
- `reset interface` - Resets interface statistics

### Best Practices
1. **Always save configuration**: Use `save` after making changes
2. **Use configuration labels**: Create checkpoints before major changes
3. **Test in lab first**: Test complex configurations in lab environment
4. **Keep console access**: Always have console cable during critical changes
5. **Document changes**: Use `description` commands for interfaces
6. **Regular backups**: Schedule regular configuration backups

### Safe Change Procedure
```
# 1. Backup current config
<Huawei> save

# 2. Make changes
[Huawei] <configuration commands>

# 3. Verify changes
<Huawei> display current-configuration

# 4. Test connectivity
<Huawei> ping <test-destination>

# 5. Save if successful
<Huawei> save
```

## Useful Shortcuts

### Command Abbreviation
```
dis = display
int = interface
sys = system-view
quit = q
dis cur = display current-configuration
dis int bri = display interface brief
dis ip int bri = display ip interface brief
```

### Output Filters
```
# Include keyword
display current-configuration | include vlan

# Exclude keyword
display current-configuration | exclude description

# Begin from match
display current-configuration | begin interface
```

## Common Issues & Solutions

### Issue: Cannot Save Configuration
```
# Check storage space
<Huawei> display device

# Clear unnecessary files
<Huawei> delete /unreserved <filename>

# Reset recycle bin
<Huawei> reset recycle-bin
```

### Issue: Interface Down
```
# Check interface status
<Huawei> display interface GigabitEthernet 0/0/1

# Check for shutdown
[Huawei-GigabitEthernet0/0/1] undo shutdown

# Check cable and transceiver
<Huawei> display transceiver
```

### Issue: Routing Not Working
```
# Verify routing table
<Huawei> display ip routing-table

# Check routing protocols
<Huawei> display ospf peer
<Huawei> display bgp peer

# Verify interface IP
<Huawei> display ip interface brief
```

## VRP vs Cisco IOS Comparison

| Function | Huawei VRP | Cisco IOS |
|----------|------------|-----------|
| Enter config mode | `system-view` | `configure terminal` |
| Show config | `display current-configuration` | `show running-config` |
| Save config | `save` | `copy run start` |
| Show interfaces | `display interface brief` | `show ip interface brief` |
| Exit mode | `quit` or `return` | `exit` |
| Negate command | `undo` | `no` |
| Show version | `display version` | `show version` |

## Additional Resources

- [Huawei Enterprise Support Portal](https://support.huawei.com/enterprise/)
- [HCIA-Datacom Study Resources](https://www.huawei.com/en/learn/)
- [Huawei Forum](https://forum.huawei.com/)

---
*Note: VRP commands may vary slightly between different device series (AR, NE, S Series). Always consult the specific device documentation for your model.*
