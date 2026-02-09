# Fortinet FortiOS CLI Reference

**Last Updated**: 2026-02-09
**Latest Version**: FortiOS 7.6.4
**Source**: [Fortinet Document Library](https://docs.fortinet.com/document/fortigate/7.6.4/cli-reference/84566/fortios-cli-reference)

## Official Documentation Links

### Latest Versions
- [FortiOS 7.6.4 CLI Reference](https://docs.fortinet.com/document/fortigate/7.6.4/cli-reference/84566/fortios-cli-reference)
- [FortiOS 7.6.3 CLI Reference](https://docs.fortinet.com/document/fortigate/7.6.3/cli-reference/84566/fortios-cli-reference)
- [FortiOS 7.6.0 CLI Reference](https://docs.fortinet.com/document/fortigate/7.6.0/cli-reference/84566/fortios-cli-reference)
- [FortiOS 7.4.11 CLI Reference](https://docs.fortinet.com/document/fortigate/7.4.11/cli-reference/84566/fortios-cli-reference)

### PDF Downloads
- [FortiOS 7.4.0 CLI Reference PDF](https://fortinetweb.s3.amazonaws.com/docs.fortinet.com/v2/attachments/9193cdf6-ef51-11ed-8e6d-fa163e15d75b/FortiOS-7.4.0-CLI_Reference.pdf)
- [FortiOS 6.4.12 CLI Reference PDF](https://fortinetweb.s3.amazonaws.com/docs.fortinet.com/v2/attachments/f3d2280a-b3ab-11ed-8e6d-fa163e15d75b/FortiOS-6.4.12-CLI_Reference.pdf)

## CLI Basics

### Access Methods
- **Console**: Serial connection to FortiGate
- **SSH**: `ssh admin@<fortigate-ip>`
- **Telnet**: Not recommended for security reasons

### Navigation
```
# View entire CLI command tree
tree

# View available commands at current level
?

# Exit current context
end
```

## Common Troubleshooting Commands

### System Status
```
# Show system status
get system status

# Show system performance
get system performance status

# Show system resources
get system performance firewall statistics

# Show HA status
get system ha status
```

### Interface Commands
```
# Show all interfaces
get system interface

# Show specific interface
get system interface physical

# Show interface statistics
diagnose hardware deviceinfo nic <interface>

# Debug interface traffic
diagnose sniffer packet <interface> <filter> <verbosity> <count>
# Example: diagnose sniffer packet port1 'host 192.168.1.1' 4 100
```

### Routing
```
# Show routing table
get router info routing-table all

# Show specific route
get router info routing-table details <destination>

# Show BGP status
get router info bgp summary

# Show OSPF neighbors
get router info ospf neighbor
```

### VPN Troubleshooting
```
# Show IPsec VPN status
get vpn ipsec tunnel summary

# Show SSL VPN status
get vpn ssl monitor

# Debug IKE
diagnose debug application ike -1
diagnose debug enable

# Show VPN tunnel details
diagnose vpn tunnel list
```

### Firewall Policies
```
# Show firewall policies
show firewall policy

# Show policy statistics
get firewall policy

# Check policy hit count
diagnose firewall iprope show 100000
```

### Sessions
```
# Show current sessions
get system session list

# Show session statistics
diagnose sys session stat

# Clear specific session
diagnose sys session clear

# Show top sessions
diagnose sys session top-summary
```

### Logging & Debugging
```
# Show logs
execute log display

# Enable debugging
diagnose debug enable
diagnose debug application <component> <level>

# Common debug components:
# - ike: IPsec VPN
# - fnbamd: Authentication
# - httpsd: Web admin
# - sslvpn: SSL VPN

# Disable debugging
diagnose debug disable
diagnose debug reset
```

### Configuration
```
# Enter configuration mode
config <context>

# Show configuration
show

# Show full configuration
show full-configuration

# Backup configuration
execute backup config management-station <filename>

# Restore configuration
execute restore config management-station <filename>
```

## Configuration Examples

### Basic Interface Configuration
```
config system interface
    edit port1
        set ip 192.168.1.1 255.255.255.0
        set allowaccess ping https ssh
        set description "LAN Interface"
    next
end
```

### Static Route
```
config router static
    edit 1
        set dst 10.0.0.0 255.255.255.0
        set gateway 192.168.1.254
        set device port1
    next
end
```

### Firewall Policy
```
config firewall policy
    edit 1
        set name "LAN-to-WAN"
        set srcintf "port1"
        set dstintf "port2"
        set srcaddr "all"
        set dstaddr "all"
        set action accept
        set schedule "always"
        set service "ALL"
        set nat enable
    next
end
```

## Safety Considerations

### Destructive Commands
⚠️ **WARNING**: The following commands can cause service disruption:
- `execute reboot` - Reboots the device
- `execute shutdown` - Shuts down the device
- `execute factoryreset` - Resets to factory defaults
- `execute formatlogdisk` - Formats the log disk
- `delete <config>` - Deletes configuration

### Best Practices
1. Always backup configuration before major changes
2. Test changes in maintenance window
3. Use `show` to verify configuration before committing
4. Keep console access available during changes
5. Document all changes

## Privilege Levels

### Admin Profiles
- **super_admin**: Full access to all commands
- **prof_admin**: Administrative access with some restrictions
- **read_only**: View-only access

### Checking Current Privileges
```
get system admin list
```

## Version-Specific Notes

### FortiOS 7.6.x
- Enhanced SD-WAN features
- Improved security fabric integration
- New CLI commands for cloud integration

### FortiOS 7.4.x
- ZTNA enhancements
- FortiSwitch controller improvements
- Security rating features

### FortiOS 7.2.x
- Universal ZTNA support
- Enhanced threat protection
- OT security features

## Additional Resources

- [Fortinet Documentation Library](https://docs.fortinet.com/)
- [Fortinet Community Forums](https://community.fortinet.com/)
- [FortiGate Cookbook](https://docs.fortinet.com/document/fortigate/7.4.0/cookbook/1/introduction)

---
*Note: Commands may vary between FortiOS versions. Always verify command syntax for your specific FortiOS version.*
