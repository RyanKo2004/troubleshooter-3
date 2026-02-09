# Cisco ASA (Adaptive Security Appliance) CLI Reference

**Last Updated**: 2026-02-09
**Latest Documentation Update**: December 1, 2025
**Source**: [Cisco Secure Firewall ASA Command References](https://www.cisco.com/c/en/us/support/security/adaptive-security-appliance-asa-software/products-command-reference-list.html)

## Official Documentation Links

### Main Resources
- [Cisco Secure Firewall ASA Command Reference (Main)](https://www.cisco.com/c/en/us/support/security/adaptive-security-appliance-asa-software/products-command-reference-list.html)
- [ASA Command Reference A-H Commands](https://www.cisco.com/c/en/us/td/docs/security/asa/asa-cli-reference/A-H/asa-command-ref-A-H.html)
- [ASA Command Reference I-R Commands](https://www.cisco.com/c/en/us/td/docs/security/asa/asa-cli-reference/I-R/asa-command-ref-I-R.html)
- [ASA Command Reference S Commands](https://www.cisco.com/c/en/us/td/docs/security/asa/asa-cli-reference/S/asa-command-ref-S.html)
- [ASA Command Reference T-Z Commands (Latest: Dec 2025)](https://www.cisco.com/c/en/us/td/docs/security/asa/asa-cli-reference/T-Z/asa-command-ref-T-Z.html)

## CLI Basics

### Access Methods
- **Console**: Serial connection (9600-8-N-1)
- **SSH**: `ssh <username>@<asa-ip>`
- **ASDM**: Web-based GUI management
- **Telnet**: Not recommended

### Command Modes
```
# User EXEC mode
ciscoasa>

# Privileged EXEC mode
ciscoasa#

# Global configuration mode
ciscoasa(config)#

# Interface configuration mode
ciscoasa(config-if)#

# Other context modes
ciscoasa(config-router)#    # Routing protocol config
ciscoasa(config-tunnel-general)#  # VPN config
```

### Context Help
```
# Show available commands
?

# Show command options
command ?

# Show partial command matches
<partial><Tab>
```

## Common Troubleshooting Commands

### System Information
```
# Show version and license
show version

# Show running configuration
show running-config

# Show startup configuration
show startup-config

# Show system uptime
show version | include up

# Show CPU usage
show cpu usage

# Show memory usage
show memory

# Show processes
show processes

# Show failover status
show failover
```

### Interface Commands
```
# Show all interfaces
show interface

# Show interface summary
show interface ip brief

# Show specific interface
show interface <interface-name>

# Show interface statistics
show interface <interface-name> stats

# Show nameif assignments
show nameif
```

### NAT & Translation
```
# Show NAT rules
show nat

# Show NAT statistics
show nat detail

# Show xlate (translation) table
show xlate

# Show xlate for specific IP
show xlate local <ip-address>

# Clear xlate entries
clear xlate
```

### Access Control & Policies
```
# Show access lists
show access-list

# Show specific ACL
show access-list <acl-name>

# Show access-list hit counts
show access-list <acl-name> | include hitcnt

# Show service policy
show service-policy

# Show connection statistics
show conn

# Show connection count
show conn count
```

### VPN Troubleshooting
```
# Show IPsec SA (Security Associations)
show crypto ipsec sa

# Show IKEv1 SA
show crypto isakmp sa

# Show IKEv2 SA
show crypto ikev2 sa

# Show VPN sessions
show vpn-sessiondb

# Show SSL VPN sessions
show vpn-sessiondb detail svc

# Show remote access VPN statistics
show vpn-sessiondb summary
```

### Routing
```
# Show routing table
show route

# Show OSPF neighbors
show ospf neighbor

# Show OSPF routes
show route ospf

# Show BGP summary
show bgp summary

# Show static routes
show route static
```

### High Availability (Failover)
```
# Show failover status
show failover

# Show failover state
show failover state

# Show failover history
show failover history

# Force failover
failover active

# Reload standby unit
failover reload-standby
```

### Logging & Debugging
```
# Show logging buffer
show logging

# Show logging settings
show logging setting

# Show logging statistics
show logging | include <search-term>

# Enable debugging
debug crypto ipsec
debug crypto isakmp
debug icmp trace

# Show active debugs
show debug

# Disable all debugging
no debug all
```

## Configuration Examples

### Basic Interface Configuration
```
ciscoasa(config)# interface GigabitEthernet0/0
ciscoasa(config-if)# nameif outside
ciscoasa(config-if)# security-level 0
ciscoasa(config-if)# ip address 203.0.113.1 255.255.255.0
ciscoasa(config-if)# no shutdown

ciscoasa(config)# interface GigabitEthernet0/1
ciscoasa(config-if)# nameif inside
ciscoasa(config-if)# security-level 100
ciscoasa(config-if)# ip address 192.168.1.1 255.255.255.0
ciscoasa(config-if)# no shutdown
```

### Static NAT (1-to-1)
```
# NAT 9.x syntax
ciscoasa(config)# object network INSIDE-SERVER
ciscoasa(config-network-object)# host 192.168.1.10
ciscoasa(config-network-object)# nat (inside,outside) static 203.0.113.10
```

### Dynamic PAT (NAT Overload)
```
ciscoasa(config)# object network INSIDE-NET
ciscoasa(config-network-object)# subnet 192.168.1.0 255.255.255.0
ciscoasa(config-network-object)# nat (inside,outside) dynamic interface
```

### Access Control List (ACL)
```
# Allow specific traffic from outside
ciscoasa(config)# access-list OUTSIDE-IN extended permit tcp any host 203.0.113.10 eq 443
ciscoasa(config)# access-list OUTSIDE-IN extended permit tcp any host 203.0.113.10 eq 80
ciscoasa(config)# access-list OUTSIDE-IN extended deny ip any any log

# Apply to interface
ciscoasa(config)# access-group OUTSIDE-IN in interface outside
```

### Site-to-Site VPN (IKEv2)
```
# IKEv2 Policy
ciscoasa(config)# crypto ikev2 policy 10
ciscoasa(config-ikev2-policy)# encryption aes-256
ciscoasa(config-ikev2-policy)# integrity sha256
ciscoasa(config-ikev2-policy)# group 14
ciscoasa(config-ikev2-policy)# prf sha256
ciscoasa(config-ikev2-policy)# lifetime seconds 86400

# IKEv2 Enable
ciscoasa(config)# crypto ikev2 enable outside

# Tunnel Group
ciscoasa(config)# tunnel-group 203.0.113.100 type ipsec-l2l
ciscoasa(config)# tunnel-group 203.0.113.100 ipsec-attributes
ciscoasa(config-tunnel-ipsec)# ikev2 remote-authentication pre-shared-key SECRET123
ciscoasa(config-tunnel-ipsec)# ikev2 local-authentication pre-shared-key SECRET123

# Crypto Map
ciscoasa(config)# crypto ipsec ikev2 ipsec-proposal MY-PROPOSAL
ciscoasa(config-ipsec-proposal)# protocol esp encryption aes-256
ciscoasa(config-ipsec-proposal)# protocol esp integrity sha-256

ciscoasa(config)# access-list VPN-ACL extended permit ip 192.168.1.0 255.255.255.0 10.0.0.0 255.255.255.0

ciscoasa(config)# crypto map OUTSIDE-MAP 10 match address VPN-ACL
ciscoasa(config)# crypto map OUTSIDE-MAP 10 set peer 203.0.113.100
ciscoasa(config)# crypto map OUTSIDE-MAP 10 set ikev2 ipsec-proposal MY-PROPOSAL
ciscoasa(config)# crypto map OUTSIDE-MAP interface outside
```

### Static Route
```
ciscoasa(config)# route outside 0.0.0.0 0.0.0.0 203.0.113.254
ciscoasa(config)# route inside 10.0.0.0 255.255.255.0 192.168.1.254
```

### Active/Standby Failover
```
# Primary unit
ciscoasa(config)# failover
ciscoasa(config)# failover lan unit primary
ciscoasa(config)# failover lan interface failover GigabitEthernet0/2
ciscoasa(config)# failover interface ip failover 10.0.0.1 255.255.255.252 standby 10.0.0.2
ciscoasa(config)# failover key SECRET123
ciscoasa(config)# failover link failover GigabitEthernet0/2

# Secondary unit
ciscoasa(config)# failover
ciscoasa(config)# failover lan unit secondary
ciscoasa(config)# failover lan interface failover GigabitEthernet0/2
ciscoasa(config)# failover interface ip failover 10.0.0.1 255.255.255.252 standby 10.0.0.2
ciscoasa(config)# failover key SECRET123
```

## Configuration Management

### Save Configuration
```
# Save running to startup
write memory
# or
copy running-config startup-config
```

### Backup Configuration
```
# Backup to TFTP
copy running-config tftp://192.168.1.100/asa-backup.cfg

# Backup to flash
copy running-config flash:asa-backup.cfg
```

### Restore Configuration
```
# Restore from TFTP
copy tftp://192.168.1.100/asa-backup.cfg running-config

# Restore from flash
copy flash:asa-backup.cfg running-config
```

## Packet Capture

### Configure Packet Capture
```
# Create capture buffer
ciscoasa(config)# access-list CAP-ACL extended permit ip host 192.168.1.10 any
ciscoasa(config)# capture CAP1 access-list CAP-ACL interface inside

# Show capture
show capture CAP1

# Export capture to TFTP
copy /pcap capture:CAP1 tftp://192.168.1.100/capture1.pcap

# Clear capture
no capture CAP1
```

### Packet Tracer Tool
```
# Simulate packet flow through ASA
packet-tracer input inside tcp 192.168.1.10 12345 203.0.113.50 80 detailed

# Test with ICMP
packet-tracer input inside icmp 192.168.1.10 8 0 8.8.8.8
```

## Safety Considerations

### Destructive Commands
⚠️ **WARNING**: The following commands can cause service disruption:
- `reload` - Reboots the ASA
- `write erase` - Erases startup configuration
- `clear xlate` - Clears translation table (breaks existing connections)
- `clear conn` - Clears all connections
- `failover active` - Forces failover
- `no failover` - Disables failover

### Best Practices
1. **Backup before changes**: Always backup configuration
2. **Use ACLs carefully**: Wrong ACL can lock you out
3. **Test with packet-tracer**: Verify policy before applying
4. **Schedule maintenance**: Plan changes during maintenance windows
5. **Console access**: Keep console cable connected during critical changes
6. **Test failover**: Regularly test failover in maintenance window
7. **Monitor connections**: Check `show conn count` before/after changes

### Connection Limits
```
# Check connection limits
show resource usage

# Show connection details
show conn detail

# Show connection by protocol
show conn protocol tcp
```

## Common Issues & Solutions

### Issue: High CPU Usage
```
# Check processes
show processes cpu-usage sorted

# Check connection count
show conn count

# Check for attacks
show threat-detection statistics
```

### Issue: VPN Not Connecting
```
# Check IKE/IPsec
show crypto isakmp sa
show crypto ipsec sa

# Enable debugging
debug crypto ikev2
debug crypto ipsec
```

### Issue: NAT Not Working
```
# Verify NAT config
show nat detail

# Check xlate table
show xlate

# Verify packet flow
packet-tracer input inside tcp 192.168.1.10 12345 8.8.8.8 80 detailed
```

### Issue: Traffic Blocked
```
# Check ACLs
show access-list

# Use packet-tracer
packet-tracer input <interface> <protocol> <src-ip> <src-port> <dst-ip> <dst-port>

# Check logging
show logging | include <ip-address>
```

## Security Levels

### Security Level Rules
- **Higher to Lower**: Allowed by default
- **Lower to Higher**: Blocked by default (requires ACL)
- **Same Level**: Blocked by default (requires `same-security-traffic permit inter-interface`)

### Common Security Levels
- **inside**: 100
- **dmz**: 50
- **outside**: 0

## Performance Monitoring

### Connection Statistics
```
# Show current connections
show conn count

# Show connection rate
show perfmon

# Show traffic statistics
show traffic
```

### Threat Detection
```
# Show threat detection statistics
show threat-detection statistics

# Show scanning threat
show threat-detection scanning-threat

# Show shun statistics
show shun
```

## Additional Resources

- [Cisco ASA Configuration Guide](https://www.cisco.com/c/en/us/support/security/asa-5500-series-next-generation-firewalls/products-installation-and-configuration-guides-list.html)
- [Cisco ASA Community](https://community.cisco.com/t5/security/ct-p/4451-discussions-security)
- [ASA Firewall Handbook](https://www.cisco.com/c/dam/en/us/td/docs/security/asa/roadmap/asaroadmap.pdf)

---
*Note: ASA CLI syntax may vary between software versions (8.x vs 9.x). Always verify commands for your specific ASA software version.*
