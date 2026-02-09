# Juniper JunOS CLI Reference

**Last Updated**: 2026-02-09
**Platform**: Juniper SRX, MX, QFX, EX Series
**Source**: [Juniper Networks Documentation](https://www.juniper.net/documentation/)

## Official Documentation Links

### Main Resources
- [Junos CLI Reference](https://www.juniper.net/documentation/us/en/software/junos/cli-reference/index.html)
- [CLI User Guide for Junos OS](https://www.juniper.net/documentation/us/en/software/junos/cli/index.html)
- [Junos CLI User Guide PDF (Dec 2025)](https://www.juniper.net/documentation/us/en/software/junos/cli/cli.pdf)
- [CLI Explorer Tool](https://apps.juniper.net/cli-explorer/)

### Quick References
- [Juniper CLI Quick Reference](https://codingpackets.com/blog/juniper-cli-quick-reference/)
- [Junos CLI Commands Cheat Sheet](https://cmdref.net/hardware/junos/index.html)

## CLI Basics

### Access Methods
- **Console**: Serial connection (9600-8-N-1)
- **SSH**: `ssh <username>@<device-ip>`
- **Telnet**: Not recommended
- **J-Web**: Web-based GUI

### Command Modes
```
# Operational mode (after login)
user@router>

# Configuration mode
user@router# (enter with 'configure' or 'edit')

# Shell mode
user@router% (enter with 'start shell')
```

### Key Characteristics
- **Hierarchical configuration**: Tree-based config structure
- **Commit model**: Changes staged before activation
- **Rollback capability**: Built-in config version control
- **Context-sensitive help**: Use `?` for help
- **Tab completion**: Auto-complete commands

## JunOS Philosophy

### Configuration Process
1. Enter configuration mode: `configure`
2. Make changes (staged in candidate config)
3. Verify changes: `show | compare`
4. Commit changes: `commit` (activates changes)
5. Exit: `exit configuration-mode`

### Unlike Other Vendors
- Changes don't take effect until `commit`
- Can review all changes before applying
- Automatic config versioning
- Syntax-based, not line-by-line

## Common Operational Commands

### System Information
```
# Show version and hardware
show version

# Show system uptime
show system uptime

# Show chassis hardware
show chassis hardware

# Show routing engine
show chassis routing-engine

# Show system alarms
show system alarms

# Show system storage
show system storage

# Show system processes
show system processes extensive
```

### Interface Commands
```
# Show all interfaces
show interfaces terse

# Show specific interface details
show interfaces ge-0/0/0

# Show interface statistics
show interfaces ge-0/0/0 extensive

# Show interface errors
show interfaces ge-0/0/0 extensive | match error

# Monitor interface traffic (real-time)
monitor interface traffic
```

### Routing
```
# Show routing table
show route

# Show specific route
show route <destination>

# Show routing protocols
show route protocol ospf

# Show OSPF neighbors
show ospf neighbor

# Show OSPF database
show ospf database

# Show BGP summary
show bgp summary

# Show BGP neighbors
show bgp neighbor

# Show RIP neighbors
show rip neighbor
```

### Layer 2 (Switches)
```
# Show VLAN information
show vlans

# Show ethernet-switching table (MAC table)
show ethernet-switching table

# Show LLDP neighbors
show lldp neighbors

# Show spanning-tree
show spanning-tree bridge

# Show LACP interfaces
show lacp interfaces
```

### Security (SRX Firewalls)
```
# Show security policies
show security policies

# Show security zones
show security zones

# Show security flow sessions
show security flow session

# Show IPsec security associations
show security ipsec security-associations

# Show IKE security associations
show security ike security-associations

# Show NAT rules
show security nat source rule all
```

### System Logging
```
# Show system log messages
show log messages

# Show log messages with filter
show log messages | match error

# Show chassis log
show log chassisd

# Show interactive commands log
show log interactive-commands
```

## Configuration Mode Commands

### Entering Configuration Mode
```
# Enter configuration mode
user@router> configure

# Enter configuration mode (exclusive - locks config)
user@router> configure exclusive

# Enter configuration mode (private - separate candidate config)
user@router> configure private
```

### Navigation in Configuration Mode
```
# Show current hierarchy level
[edit]
user@router# pwd

# Move to specific hierarchy
[edit]
user@router# edit interfaces ge-0/0/0

# Move up one level
[edit interfaces ge-0/0/0]
user@router# up

# Move to top level
[edit interfaces ge-0/0/0]
user@router# top

# Show configuration
[edit]
user@router# show

# Show specific section
[edit]
user@router# show interfaces
```

### Making Changes
```
# Set configuration value
[edit]
user@router# set interfaces ge-0/0/0 unit 0 family inet address 192.168.1.1/24

# Delete configuration
[edit]
user@router# delete interfaces ge-0/0/0 unit 0 family inet address

# Deactivate (disable without deleting)
[edit]
user@router# deactivate interfaces ge-0/0/0

# Reactivate
[edit]
user@router# activate interfaces ge-0/0/0
```

## Configuration Examples

### Basic Interface Configuration
```
[edit]
user@router# set interfaces ge-0/0/0 description "LAN Interface"
user@router# set interfaces ge-0/0/0 unit 0 family inet address 192.168.1.1/24
user@router# commit
```

### VLAN Configuration (Switch)
```
[edit]
user@switch# set vlans sales vlan-id 10
user@switch# set vlans sales description "Sales Department"

# Assign port to VLAN (access mode)
user@switch# set interfaces ge-0/0/1 unit 0 family ethernet-switching interface-mode access
user@switch# set interfaces ge-0/0/1 unit 0 family ethernet-switching vlan members sales

# Configure trunk port
user@switch# set interfaces ge-0/0/24 unit 0 family ethernet-switching interface-mode trunk
user@switch# set interfaces ge-0/0/24 unit 0 family ethernet-switching vlan members [sales engineering]
user@switch# commit
```

### Static Route
```
[edit]
user@router# set routing-options static route 10.0.0.0/24 next-hop 192.168.1.254
user@router# set routing-options static route 0.0.0.0/0 next-hop 203.0.113.1
user@router# commit
```

### OSPF Configuration
```
[edit]
user@router# set protocols ospf area 0.0.0.0 interface ge-0/0/0.0
user@router# set protocols ospf area 0.0.0.0 interface ge-0/0/1.0
user@router# set routing-options router-id 1.1.1.1
user@router# commit
```

### BGP Configuration
```
[edit]
user@router# set routing-options autonomous-system 65001
user@router# set routing-options router-id 1.1.1.1
user@router# set protocols bgp group EXTERNAL type external
user@router# set protocols bgp group EXTERNAL peer-as 65002
user@router# set protocols bgp group EXTERNAL neighbor 192.168.1.2
user@router# commit
```

### Firewall Filter (ACL)
```
[edit]
user@router# set firewall family inet filter PERMIT-WEB term 1 from protocol tcp
user@router# set firewall family inet filter PERMIT-WEB term 1 from destination-port 80
user@router# set firewall family inet filter PERMIT-WEB term 1 then accept
user@router# set firewall family inet filter PERMIT-WEB term 2 from protocol tcp
user@router# set firewall family inet filter PERMIT-WEB term 2 from destination-port 443
user@router# set firewall family inet filter PERMIT-WEB term 2 then accept
user@router# set firewall family inet filter PERMIT-WEB term 3 then discard

# Apply to interface
user@router# set interfaces ge-0/0/0 unit 0 family inet filter input PERMIT-WEB
user@router# commit
```

### Security Policy (SRX)
```
[edit security]
user@srx# set zones security-zone trust interfaces ge-0/0/0.0
user@srx# set zones security-zone untrust interfaces ge-0/0/1.0

# Create address book
user@srx# set address-book global address SERVER1 192.168.1.10/32

# Create policy
user@srx# set policies from-zone trust to-zone untrust policy TRUST-TO-UNTRUST match source-address any
user@srx# set policies from-zone trust to-zone untrust policy TRUST-TO-UNTRUST match destination-address any
user@srx# set policies from-zone trust to-zone untrust policy TRUST-TO-UNTRUST match application any
user@srx# set policies from-zone trust to-zone untrust policy TRUST-TO-UNTRUST then permit
user@srx# commit
```

### NAT Configuration (SRX)
```
# Source NAT (PAT)
[edit security nat source]
user@srx# set rule-set NAT-OUT from zone trust
user@srx# set rule-set NAT-OUT to zone untrust
user@srx# set rule-set NAT-OUT rule RULE1 match source-address 192.168.1.0/24
user@srx# set rule-set NAT-OUT rule RULE1 then source-nat interface

# Destination NAT (port forwarding)
[edit security nat destination]
user@srx# set pool WEB-SERVER address 192.168.1.10/32
user@srx# set pool WEB-SERVER address port 80
user@srx# set rule-set DNAT from zone untrust
user@srx# set rule-set DNAT rule WEB match destination-address 203.0.113.10/32
user@srx# set rule-set DNAT rule WEB match destination-port 80
user@srx# set rule-set DNAT rule WEB then destination-nat pool WEB-SERVER
user@srx# commit
```

### Link Aggregation (LAG)
```
[edit]
user@router# set chassis aggregated-devices ethernet device-count 1
user@router# set interfaces ae0 aggregated-ether-options lacp active
user@router# set interfaces ae0 unit 0 family inet address 192.168.1.1/24
user@router# set interfaces ge-0/0/0 gigether-options 802.3ad ae0
user@router# set interfaces ge-0/0/1 gigether-options 802.3ad ae0
user@router# commit
```

## Commit Operations

### Basic Commit
```
# Commit changes
[edit]
user@router# commit

# Commit with comment
[edit]
user@router# commit comment "Added new VLAN configuration"

# Commit and quit
[edit]
user@router# commit and-quit
```

### Commit Check & Validation
```
# Check syntax before committing
[edit]
user@router# commit check

# Show what will be committed
[edit]
user@router# show | compare

# Show changes in set format
[edit]
user@router# show | display set | compare
```

### Commit Confirm (Safety Feature)
```
# Commit with auto-rollback after 5 minutes
[edit]
user@router# commit confirmed 5
# If you get disconnected, config automatically rolls back

# Confirm the commit (prevents rollback)
[edit]
user@router# commit
```

## Rollback Capability

### View Previous Configurations
```
# Show last 50 commits
user@router> show system commit

# Compare current config with previous
[edit]
user@router# show | compare rollback 1

# View specific rollback config
[edit]
user@router# show | compare rollback 5
```

### Rollback to Previous Configuration
```
# Rollback to previous config (staged, not active)
[edit]
user@router# rollback 1

# View what will change
[edit]
user@router# show | compare

# Commit the rollback
[edit]
user@router# commit
```

## Configuration Management

### Save Configuration
```
# Configuration automatically saved on commit
# JunOS maintains 50 rollback versions

# Save configuration to file
user@router> show configuration | save /var/tmp/backup-config.txt

# Load configuration from file
user@router> configure
[edit]
user@router# load override /var/tmp/backup-config.txt
user@router# commit
```

### Backup to Remote Server
```
# Copy config to remote server via SCP
user@router> file copy /config/juniper.conf.gz scp://user@server:/backup/

# Archive configuration to FTP
user@router> file copy /config/juniper.conf.gz ftp://server/backup/
```

### Factory Reset
```
# Load factory default configuration
user@router> configure
[edit]
user@router# load factory-default
user@router# commit

# Delete all configuration
[edit]
user@router# delete
user@router# commit
```

## Diagnostics & Troubleshooting

### Ping & Traceroute
```
# Ping with options
user@router> ping 8.8.8.8 count 5 size 1000

# Ping from specific source
user@router> ping 8.8.8.8 source 192.168.1.1

# Traceroute
user@router> traceroute 8.8.8.8

# MTU path discovery
user@router> ping 8.8.8.8 do-not-fragment size 1500
```

### Real-Time Monitoring
```
# Monitor interface traffic
user@router> monitor interface traffic

# Monitor system resources
user@router> monitor start messages

# Stop monitoring
user@router> monitor stop
```

### Packet Capture
```
# Start packet capture
user@router> monitor traffic interface ge-0/0/0

# Capture with filter
user@router> monitor traffic interface ge-0/0/0 matching "host 192.168.1.10"

# Save capture to file
user@router> monitor traffic interface ge-0/0/0 write-file /var/tmp/capture.pcap

# View capture file
user@router> monitor traffic interface ge-0/0/0 read-file /var/tmp/capture.pcap
```

### Flow Tracing (SRX)
```
# Test security policy match
user@srx> show security match-policies from-zone trust to-zone untrust source-ip 192.168.1.10 destination-ip 8.8.8.8 protocol tcp destination-port 80

# Show active sessions
user@srx> show security flow session

# Clear specific session
user@srx> clear security flow session destination-prefix 8.8.8.8/32
```

## Safety Considerations

### Destructive Commands
⚠️ **WARNING**: The following commands can cause service disruption:
- `request system reboot` - Reboots the device
- `request system halt` - Shuts down the device
- `load factory-default` - Resets to factory config
- `delete` (at top level) - Deletes entire configuration
- `request system zeroize` - Completely erases all config and data

### Best Practices
1. **Use commit confirmed**: Always use for risky changes
2. **Check before commit**: Use `commit check` and `show | compare`
3. **Add commit comments**: Document changes
4. **Test in lab**: Test complex configs in lab environment
5. **Keep console access**: Have console available during changes
6. **Use private mode**: For making experimental changes
7. **Regular backups**: Schedule configuration backups

### Safe Change Workflow
```
# 1. Enter configuration mode
user@router> configure

# 2. Make changes
[edit]
user@router# set <configuration>

# 3. Verify syntax
[edit]
user@router# commit check

# 4. Review changes
[edit]
user@router# show | compare

# 5. Commit with auto-rollback
[edit]
user@router# commit confirmed 10

# 6. Test functionality
# (exit config mode and test)

# 7. Confirm commit if successful
user@router> configure
[edit]
user@router# commit

# If issues occur, just wait 10 minutes for auto-rollback
```

## Useful Commands & Tricks

### Output Modifiers (Pipe Commands)
```
# Match pattern
show configuration | match ospf

# Display as set commands
show configuration | display set

# Display XML format
show configuration | display xml

# Find configuration location
show configuration | find "192.168.1"

# Display inheritance
show configuration | display inheritance

# Count lines
show interfaces | count
```

### Command Shortcuts
```
# Recent commands history
user@router> show cli history

# Run operational command from config mode
[edit]
user@router# run show interfaces terse

# Execute shell command
user@router> start shell
```

### Batch Configuration
```
# Load configuration snippet
[edit]
user@router# load merge terminal
# Paste configuration
# Press Ctrl+D when done

# Load from URL
[edit]
user@router# load merge http://server/config.txt
```

## JunOS vs Cisco IOS Comparison

| Function | Juniper JunOS | Cisco IOS |
|----------|---------------|-----------|
| Config mode | `configure` | `configure terminal` |
| Show config | `show configuration` | `show running-config` |
| Apply changes | `commit` | Immediate |
| Interface config | `set interfaces ge-0/0/0...` | `interface g0/0` |
| Rollback | `rollback <n>` | Limited |
| Show interfaces | `show interfaces terse` | `show ip int brief` |
| Exit config | `exit configuration-mode` | `exit` |

## Additional Resources

- [Juniper Learning Portal](https://learningportal.juniper.net/)
- [Day One Books (Free)](https://www.juniper.net/documentation/dayonebooks/)
- [J-Net Community](https://community.juniper.net/)
- [Junos Genius App](https://apps.juniper.net/)

---
*Note: JunOS syntax is consistent across all Juniper platforms (SRX, MX, QFX, EX), but some features are platform-specific. Always verify feature availability for your device model.*
