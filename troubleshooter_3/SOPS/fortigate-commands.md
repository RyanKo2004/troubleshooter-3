# Fortigate Commands

### General Device Info

- <span style="color: #339966;">`<strong><span style="color: #339966;">get system status</span></strong>`</span> - Give you info about the device including Serial Number.

```
FUHO-S047-FW01 # get system status
Version: FortiGate-200E v6.0.8,build0303,191205 (GA)
Virus-DB: 81.00093(2020-10-14 18:20)
Extended DB: 81.00093(2020-10-14 18:19)
IPS-DB: 6.00741(2015-12-01 02:30)
IPS-ETDB: 16.00943(2020-10-14 00:22)
APP-DB: 16.00943(2020-10-14 00:22)
INDUSTRIAL-DB: 6.00741(2015-12-01 02:30)
Serial-Number: FG200ETK19912324
IPS Malicious URL Database: 2.00797(2020-10-14 05:06)
Botnet DB: 4.00661(2020-10-01 21:59)
BIOS version: 05000006
System Part-Number: P19082-03
Log hard disk: Not available
Hostname: FUHO-S047-FW01
Operation Mode: NAT
Current virtual domain: root
Max number of virtual domains: 10
Virtual domains status: 1 in NAT mode, 0 in TP mode
Virtual domain configuration: disable
FIPS-CC mode: disable
Current HA mode: standalone
Branch point: 0303
Release Version Information: GA
FortiOS x86-64: Yes
System time: Thu Oct 15 20:08:04 2020

FUHO-S047-FW01 #
```

- `<strong><span style="color: #339966;">get system performance status</span></strong>` - Shows device up time.

```
FUHO-S047-FW01 # get system performance status
CPU states: 0% user 0% system 0% nice 100% idle 0% iowait 0% irq 0% softirq
CPU0 states: 0% user 0% system 0% nice 100% idle 0% iowait 0% irq 0% softirq
CPU1 states: 0% user 0% system 0% nice 100% idle 0% iowait 0% irq 0% softirq
Memory: 4058156k total, 1445032k used (35.6%), 2461908k free (60.7%), 151216k freeable (3.7%)
Average network usage: 144 / 149 kbps in 1 minute, 290 / 294 kbps in 10 minutes, 507 / 511 kbps in 30 minutes
Average sessions: 370 sessions in 1 minute, 367 sessions in 10 minutes, 388 sessions in 30 minutes
Average session setup rate: 1 sessions per second in last 1 minute, 0 sessions per second in last 10 minutes, 0 sessions per second in last 30 minutes
Average NPU sessions: 79 sessions in last 1 minute, 78 sessions in last 10 minutes, 77 sessions in last 30 minutes
Virus caught: 0 total in 1 minute
IPS attacks blocked: 0 total in 1 minute
Uptime: 85 days,  2 hours,  55 minutes

FUHO-S047-FW01 #
```

- `<span style="color: #339966;"><strong>diagnose hardwar</strong></span><strong><span style="color: #339966;">e deviceinfo nic <interface-name></span></strong>` - Shows the received and transmitted packets for the specified interface.

```
FUHO-S047-FW01 # diagnose hardware deviceinfo nic
The following NICs are available:
        ha
        mgmt
        npu0_vlink0
        npu0_vlink1
        npu1_vlink0
        npu1_vlink1
        port1
        port10
        port11
        port12
        port13
        port14
        port15
        port16
        port17
        port18
        port2
        port3
        port4
        port5
        port6
        port7
        port8
        port9
        wan1
        wan2

FUHO-S047-FW01 # diagnose hardware deviceinfo nic wan1
Description     :FortiASIC NP6LITE Adapter
Driver Name     :FortiASIC NP6LITE Driver
PCI Slot        :PCI Bus 0000:08
irq             :16
Board           :200E
lif id          :12
lif oid         :76
netdev oid      :76
tx group        :0
Current_HWaddr   04:d5:90:32:5a:ac
Permanent_HWaddr 04:d5:90:32:5a:ac
========== Link Status ==========
Admin           :up
netdev status   :up
autonego_setting:1
link_setting    :1
speed_setting   :10
duplex_setting  :0
Speed           :1000
Duplex          :Full
link_status     :Up
============ Counters ===========
Rx Pkts         :2363883123
Rx Bytes        :2156294423298
Tx Pkts         :1948812804
Tx Bytes        :855411156578
Host Rx Pkts    :937661439
Host Rx Bytes   :633483433946
Host Tx Pkts    :902749925
Host Tx Bytes   :491832141345
Host Tx dropped :0
FragTxCreate    :0
FragTxOk        :0
FragTxDrop      :0

FUHO-S047-FW01 #
```

### BGP

- `<strong><span style="color: #339966;">get router info bgp summary</span></strong>` - Use this command to display BGP summary information.

```
FUHO-S047-FW01 # get router info bgp summary
BGP router identifier 59.153.21.185, local AS number 65432
BGP table version is 101130
26 BGP AS-PATH entries
2 BGP community entries

Neighbor        V         AS MsgRcvd MsgSent   TblVer  InQ OutQ Up/Down  State/PfxRcd
59.153.21.184   4      17484  916522  559912    97532    0    0 03w6d15h     1130
59.153.21.186   4      65432  544699  608508   101130    0    0 03w4d20h        1
2406:2b00:151:5c::1 4      17484  504473  559817        0    0    0 03w6d15h        0
2406:2b00:151:5d::1 4      65432  524544  562010        0    0    0 03w4d20h        0

Total number of neighbors 4


FUHO-S047-FW01 #
```

- `<strong><span style="color: #339966;">get router info6 bgp summary</span></strong>` - Use this command to display ipv6 BGP summary information.

```
FUHO-S047-FW01 # get router info6 bgp summary
BGP router identifier 59.153.21.185, local AS number 65432
BGP table version is 78193
26 BGP AS-PATH entries
2 BGP community entries

Neighbor        V         AS MsgRcvd MsgSent   TblVer  InQ OutQ Up/Down  State/PfxRcd
59.153.21.184   4      17484  916690  560016    75528    0    0 03w6d15h        0
59.153.21.186   4      65432  544800  608625    78192    0    0 03w4d20h        0
2406:2b00:151:5c::1 4      17484  504565  559922    53037    0    0 03w6d15h      400
2406:2b00:151:5d::1 4      65432  524642  562114    78131    0    0 03w4d20h        2

Total number of neighbors 4


FUHO-S047-FW01 #
```

- `<strong><span style="color: #339966;">get router info6 routing-table detail</span></strong>`- Use this command to show a detailed view of the routing table

```
FUHO-S047-FW01 # get router info6 bgp summary
BGP router identifier 59.153.21.185, local AS number 65432
BGP table version is 78193
26 BGP AS-PATH entries
2 BGP community entries

Neighbor        V         AS MsgRcvd MsgSent   TblVer  InQ OutQ Up/Down  State/PfxRcd
59.153.21.184   4      17484  916690  560016    75528    0    0 03w6d15h        0
59.153.21.186   4      65432  544800  608625    78192    0    0 03w4d20h        0
2406:2b00:151:5c::1 4      17484  504565  559922    53037    0    0 03w6d15h      400
2406:2b00:151:5d::1 4      65432  524642  562114    78131    0    0 03w4d20h        2

Total number of neighbors 4


FUHO-S047-FW01 #
```

- `<strong><span style="color: #339966;">get router info routing-table all</span></strong>` - Use this command to display the routing table.

```
FUHO-S047-FW01 # get router info routing-table all

Routing table for VRF=0
Codes: K - kernel, C - connected, S - static, R - RIP, B - BGP
       O - OSPF, IA - OSPF inter area
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2
       i - IS-IS, L1 - IS-IS level-1, L2 - IS-IS level-2, ia - IS-IS inter area
       * - candidate default

B*      0.0.0.0/0 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.21.8.0/21 [20/0] via 59.153.21.184, VL20-CCLWAN, 01w0d00h
B       10.21.16.0/21 [20/0] via 59.153.21.184, VL20-CCLWAN, 01w3d19h
B       10.21.24.0/21 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.21.40.0/21 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.21.56.0/21 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.21.64.0/21 [20/0] via 59.153.21.184, VL20-CCLWAN, 01w3d05h
B       10.48.0.0/12 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.2.0/24 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.4.0/23 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.4.79/32 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.6.0/24 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.7.0/24 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.8.0/24 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.9.0/25 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.9.128/25 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.11.0/24 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.12.0/24 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h
B       10.64.14.0/24 [20/0] via 59.153.21.184, VL20-CCLWAN, 03w6d15h

FUHO-S047-FW01 #
```

- `<strong><span style="color: #339966;">get router info6 routing-table all</span></strong>` - Use this command to display the IPv6 routing table.

```
FUHO-S047-FW01 # get router info6 routing-table
IPv6 Routing Table
Codes: K - kernel route, C - connected, S - static, R - RIP, O - OSPF,
       IA - OSPF inter area
       N1 - OSPF NSSA external type 1, N2 - OSPF NSSA external type 2
       E1 - OSPF external type 1, E2 - OSPF external type 2
       i - IS-IS, B - BGP
       * - candidate default

Timers: Uptime

C       ::1/128 via ::, root, 12w1d03h
B       2406:2b00:8::3e/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 5d06h39m
B       2406:2b00:8::41/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 5d06h38m
B       2406:2b00:8::93/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::94/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::1cd/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::23b/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w4d21h
B       2406:2b00:8::27c/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 02w3d06h
B       2406:2b00:8::29a/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 02w3d06h
B       2406:2b00:8::29d/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 02w6d15h
B       2406:2b00:8::2be/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 02w6d15h
B       2406:2b00:8::55d/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::55f/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::82a/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::82b/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::82c/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::82d/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::845/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::846/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::847/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::848/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::849/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::84a/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::9f9/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 2d20h54m
B       2406:2b00:8::9fa/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 2d20h54m
B       2406:2b00:8::9fb/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::9fc/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h
B       2406:2b00:8::9fd/128 [20/0] via fe80::b226:80ff:fe0a:f1ee, VL20-CCLWAN, 03w6d15h

FUHO-S047-FW01 #
```

- `<strong><span style="color: #339966;">get router info protocols</span></strong>` - Use this command to display all the running routing protocols.

```
FUHO-S047-FW01 # get router info protocols
Routing Protocol is "rip"
  Sending updates every 30 seconds with +/-50%
  Timeout after 180 seconds, garbage collect after 120 seconds
  Outgoing update filter list for all interface is not set
  Incoming update filter list for all interface is not set
  Default redistribution metric is 1
  Maximum output metric is 15
  Redistributing:
  Default version control: send version 2, receive version 2
    Interface        Send  Recv   Key-chain
  Routing for Networks:
  Routing Information Sources:
    Gateway          Distance  Last Update  Bad Packets  Bad Routes
  Distance: (default is 120)

Routing Protocol is "ospf 0", VRF 0
  Invalid after 0 seconds, hold down 0, flushed after 0
  Outgoing update filter list for all interfaces is
  Incoming update filter list for all interfaces is
  Redistributing:
  Routing for Networks:
  Routing Information Sources:
    Gateway         Distance      Last Update
  Distance: (default is 110)
    Address         Mask            Distance List


Routing Protocol is "isis"
  System ID: 0000.0000.0000
  Area addr: Non-configured
  IS type: level-1-2
  Number of Neighbors: 0

Routing Protocol is "bgp 65432"
  IGP synchronization is disabled
  Automatic route summarization is disabled
  Default local-preference applied to incoming route is 100
  Redistributing:
  Neighbor(s):
  Address          AddressFamily  FiltIn  FiltOut  DistIn  DistOut  RouteMapIn  RouteMapOut  Weight
59.153.21.184           unicast
59.153.21.186           unicast
2406:2b00:151:5c::1     unicast
2406:2b00:151:5d::1     unicast



FUHO-S047-FW01 #
```

### NTP

- <span style="color: #339966;">`<strong>diagnose sys ntp status</strong>` </span>- Use following commands to check the NTP server status

```
TAHU-S008-FW01 # diagnose sys ntp status
synchronized: yes, ntpsync: enabled, server-mode: enabled

ipv6 server(2406:2B00:10:200::10) 2406:2b00:10:200::10 -- reachable(0x1) S:2 T:8
        server-version=4, stratum=3
        reference time is e332a161.32188afb -- UTC Thu Oct 15 10:22:25 2020
        clock offset is 0.001061 sec, root delay is 0.003983 sec
        root dispersion is 0.028214 sec, peer dispersion is 28 msec

ipv6 server(2406:2B00:10:100::10) 2406:2b00:10:100::10 -- reachable(0xff) S:2 T:8 selected
        server-version=4, stratum=3
        reference time is e3329d96.981109d3 -- UTC Thu Oct 15 10:06:14 2020
        clock offset is 0.000842 sec, root delay is 0.018616 sec
        root dispersion is 0.064194 sec, peer dispersion is 4 msec


TAHU-S008-FW01 #
```

### Check the 4G signal of the FortiExtender

- `<strong><span style="color: #339966;">get extender modem-status <S/N of Forti Extender></span></strong>` - Use this command to check all 4G metrics (RRSI,SINR,RSRQ, and RSRP).

```
TAHU-S008-FW01 # get extender modem-status ?
<sn>    extender serial number.
FX211E5920001612        extender

TAHU-S008-FW01 # get extender modem-status FX211E5920001612
physical_port:       2-1.2
manufacture:         Sierra Wireless, Incorporated
product:             Sierra Wireless, Incorporated
model:               EM7565
revision:            SWI9X50C_01.08.04.00 dbb5d0 jenkins 2018/08/21 21:40:11
imsi:                530058721472489
pin_status:          disable
service:             LTE
signal_strength:     52
RSSI:                -74 dBm
connection_status:   CONN_STATE_CONNE0TED
Profile 0TED:
NAI:
Profile:
home_addr:
primary_ha:
secondary_ha:
aaa_spi:
ha_spi:
esn_imei:            353533101322785
activation_status:
roaming_status:      N/A
usim_status:
oma_dm_version:
plmn:
band:                B1
signal_rsrq:         -11.7
signal_rsrp:         -105
lte_sinr:            0.6
lte_rssi:            -74
lte_rs_throughput:
lte_ts_throughput:
lte_physical_cellid: 00044886
modem_type:          EM7565
drc_cdma_evdo:
current_snr:
wireless_operator:   Spark
operating_mode:
wireless_signal:     52
usb_wan_mac:

TAHU-S008-FW01 #
```

### Basic CLI Commands

- `<span style="color: #339966;"><strong>execute ping</strong></span>` - <span class="_Override">U</span>se these commands to perform an ICMP `ECHO` request to a host by specifying its fully qualified domain name (FQDN) or IPv4 address.

```
FUHO-S047-FW01 # execute ping 59.153.21.184
PING 59.153.21.184 (59.153.21.184): 56 data bytes
64 bytes from 59.153.21.184: icmp_seq=0 ttl=255 time=1.7 ms
64 bytes from 59.153.21.184: icmp_seq=1 ttl=255 time=1.8 ms
64 bytes from 59.153.21.184: icmp_seq=2 ttl=255 time=1.7 ms
64 bytes from 59.153.21.184: icmp_seq=3 ttl=255 time=1.6 ms
64 bytes from 59.153.21.184: icmp_seq=4 ttl=255 time=1.6 ms

--- 59.153.21.184 ping statistics ---
5 packets transmitted, 5 packets received, 0% packet loss
round-trip min/avg/max = 1.6/1.6/1.8 ms

FUHO-S047-FW01 #
```

- `<span style="color: #339966;"><strong>execute ping6</strong></span>` - <span class="_Override">U</span>se these commands to perform an ICMP `ECHO` request to a IPv6 address.

```
FUHO-S047-FW01 # execute ping6 2406:2b00:8::ad0
PING 2406:2b00:8::ad0(2406:2b00:8::ad0) 56 data bytes
64 bytes from 2406:2b00:8::ad0: icmp_seq=1 ttl=64 time=0.608 ms
64 bytes from 2406:2b00:8::ad0: icmp_seq=2 ttl=64 time=0.702 ms
64 bytes from 2406:2b00:8::ad0: icmp_seq=3 ttl=64 time=0.687 ms
64 bytes from 2406:2b00:8::ad0: icmp_seq=4 ttl=64 time=0.736 ms
64 bytes from 2406:2b00:8::ad0: icmp_seq=5 ttl=64 time=0.749 ms

--- 2406:2b00:8::ad0 ping statistics ---
5 packets transmitted, 5 packets received, 0% packet loss, time 4048ms
rtt min/avg/max/mdev = 0.608/0.696/0.749/0.054 ms

FUHO-S047-FW01 #
```

- `<span style="color: #339966;"><strong>get system per firewall</strong></span>` - Use this command to display packet distribution and traffic statistics information for the FortiGate firewall.

```
TAHU-S044-FW01 # get system per firewall
packet-distribution    Show distribution statistics.
statistics             Show traffic stats.

TAHU-S044-FW01 # get system per firewall statistics
getting traffic statistics...
Browsing: 70174 packets, 58351886 bytes
DNS: 1392 packets, 236655 bytes
E-Mail: 7 packets, 448 bytes
FTP: 0 packets, 0 bytes
Gaming: 0 packets, 0 bytes
IM: 0 packets, 0 bytes
Newsgroups: 0 packets, 0 bytes
P2P: 0 packets, 0 bytes
Streaming: 0 packets, 0 bytes
TFTP: 0 packets, 0 bytes
VoIP: 0 packets, 0 bytes
Generic TCP: 21992 packets, 8986863 bytes
Generic UDP: 10897 packets, 3563002 bytes
Generic ICMP: 374 packets, 22944 bytes
Generic IP: 139 packets, 11120 bytes

TAHU-S044-FW01 # get system per firewall packet-distribution
getting packet distribution statistics...
0 bytes - 63 bytes: 3925 packets
64 bytes - 127 bytes: 1226 packets
128 bytes - 255 bytes: 647 packets
256 bytes - 383 bytes: 291 packets
384 bytes - 511 bytes: 179 packets
512 bytes - 767 bytes: 94 packets
768 bytes - 1023 bytes: 68 packets
1024 bytes - 1279 bytes: 63 packets
1280 bytes - 1500 bytes: 693 packets
 > 1500 bytes: 0 packets

TAHU-S044-FW01 #
```

- `<span style="color: #339966;"><strong>diagnose ip address list</strong></span>` - Use this command to display packet distribution and traffic statistics information for the FortiGate firewall.

```
FUHO-S555-FW01 # diagnose ip address list
IP=192.168.1.100->192.168.1.100/255.255.255.0 index=5 devname=wan1
IP=192.0.2.1->192.0.2.1/255.255.255.0 index=7 devname=internal8
IP=127.0.0.1->127.0.0.1/255.0.0.0 index=18 devname=root
IP=127.0.0.1->127.0.0.1/255.0.0.0 index=20 devname=Loopback0
IP=100.90.187.0->100.90.187.0/255.255.255.255 index=21 devname=fex
IP=169.254.1.1->169.254.1.1/255.255.255.0 index=22 devname=fortilink
IP=10.73.121.1->10.73.121.1/255.255.255.0 index=23 devname=SWITCH
IP=10.190.0.12->10.190.0.1/255.255.254.0 index=24 devname=FH-VPN-WAN-1
IP=10.190.2.12->10.190.2.1/255.255.254.0 index=25 devname=FH-VPN-WAN-2
IP=10.73.120.1->10.73.120.1/255.255.255.0 index=26 devname=VL606-MGMT
IP=10.73.122.1->10.73.122.1/255.255.255.0 index=27 devname=VL608-FWXCONN
IP=10.73.123.1->10.73.123.1/255.255.255.0 index=28 devname=VL609-WIFIREST
IP=10.73.124.1->10.73.124.1/255.255.255.0 index=29 devname=VL610-VOIP
IP=10.73.126.1->10.73.126.1/255.255.255.0 index=30 devname=VL612-CORPWIFI
IP=10.73.127.1->10.73.127.1/255.255.255.0 index=31 devname=VL614-SECURITY
IP=10.73.125.1->10.73.125.1/255.255.255.0 index=32 devname=VL615-BYOD
IP=127.0.0.1->127.0.0.1/255.0.0.0 index=33 devname=vsys_ha
IP=127.0.0.1->127.0.0.1/255.0.0.0 index=35 devname=vsys_fgfm
IP=169.254.3.100->169.254.3.100/255.255.0.0 index=36 devname=tun_fgfm

FUHO-S555-FW01 #

```

- `<span style="color: #339966;"><strong>diagnose ipv6 address list</strong></span>` - Use this command to display packet distribution and traffic statistics information for the FortiGate firewall.

```
FUHO-S555-FW01 # diagnose ipv6 address list
dev=18 devname=root flag=P scope=254 prefix=128 addr=::1 preferred=4294967295 valid=4294967295 cstamp=4881 tstamp=4881
dev=20 devname=Loopback0 flag=P scope=0 prefix=128 addr=2406:2b00:8::41f preferred=4294967295 valid=4294967295 cstamp=12480 tstamp=12480
dev=24 devname=FH-VPN-WAN-1 flag=P scope=0 prefix=64 addr=2406:2b00:151:101::c preferred=4294967295 valid=4294967295 cstamp=12480 tstamp=12480
dev=25 devname=FH-VPN-WAN-2 flag=P scope=0 prefix=64 addr=2406:2b00:151:102::c preferred=4294967295 valid=4294967295 cstamp=12480 tstamp=12480
dev=33 devname=vsys_ha flag=P scope=254 prefix=128 addr=::1 preferred=4294967295 valid=4294967295 cstamp=11838 tstamp=11838
dev=35 devname=vsys_fgfm flag=P scope=254 prefix=128 addr=::1 preferred=4294967295 valid=4294967295 cstamp=12497 tstamp=12497

FUHO-S555-FW01 #

```

- `<span style="color: #339966;"><strong>get system interface</strong></span>` - Use this command to list all interfaces on the device

```
FUHO-S047-FW01 # get system interface
== [ wan1 ]
name: wan1   mode: dhcp    ip: 0.0.0.0 0.0.0.0   status: up    netbios-forward: disable    type: physical   netflow-sampler: disable    sflow-sampler: disable    src-check: enable    explicit-web-proxy: disable    explicit-ftp-proxy: disable    proxy-captive-portal: disable    trunk: disable    wccp: disable    drop-overlapped-fragment: disable    drop-fragment: disable    mtu-override: disable
== [ wan2 ]
name: wan2   mode: dhcp    ip: 0.0.0.0 0.0.0.0   status: up    netbios-forward: disable    type: physical   netflow-sampler: disable    sflow-sampler: disable    src-check: enable    explicit-web-proxy: disable    explicit-ftp-proxy: disable    proxy-captive-portal: disable    trunk: disable    wccp: disable    drop-overlapped-fragment: disable    drop-fragment: disable    mtu-override: disable
== [ dmz ]
name: dmz   mode: static    ip: 0.0.0.0 0.0.0.0   status: down    netbios-forward: disable    type: physical   netflow-sampler: disable    sflow-sampler: disable    src-check: enable    explicit-web-proxy: disable    explicit-ftp-proxy: disable    proxy-captive-portal: disable    trunk: disable    wccp: disable    drop-overlapped-fragment: disable    drop-fragment: disable    mtu-override: disable
...
```

- `<span style="color: #339966;"><strong>get system interface physical</strong></span>` - Use this command to show all physical interfaces that are up or down.

```
FUHO-S047-FW01 # get system interface physical
== [onboard]
        ==[a]
                mode: static
                ip: 0.0.0.0 0.0.0.0
                ipv6: ::/0
                status: down
                speed: n/a
                FEC: none
                FEC_cap: none
        ==[b]
                mode: static
                ip: 0.0.0.0 0.0.0.0
                ipv6: ::/0
                status: down
                speed: n/a
                FEC: none
                FEC_cap: none
        ==[dmz]
                mode: static
                ip: 0.0.0.0 0.0.0.0
                ipv6: ::/0
                status: down
                speed: n/a
                FEC: none
                FEC_cap: none
...
```

- `<strong><span style="color: #339966;">get vpn ipsec tunnel summary </span></strong>` - Use this command to display status of all IPsec VPN tunnels

```
FUHO-S047-FW01 # get vpn ipsec tunnel summary
...
```

- `<strong><span style="color: #339966;">diag debug rating</span></strong>` - Use this command to display show system resources/debugs

```
FUHO-S047-FW01 # diag debug rating
Locale       : english

Service      : Web-filter
Status       : Disable

Service      : Antispam
Status       : Disable

Service      : Virus Outbreak Prevention
Status       : Disable

```

- `<strong><span style="color: #339966;">diagnose sys tcpsock</span></strong>` - Use this command to show active TCP socket connections ('listen' means it is open and ready to be connected'

```
FUHO-S047-FW01 # diagnose sys tcpsock
0.0.0.0:10400->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20588 process=186/authd
0.0.0.0:10500->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20594 process=186/authd
0.0.0.0:5060->0.0.0.0:0->state=listen err=0 socktype=2 rma=0 wma=0 fma=0 tma=0 inode=18629 process=197/voipd
0.0.0.0:5061->0.0.0.0:0->state=listen err=0 socktype=2 rma=0 wma=0 fma=0 tma=0 inode=18630 process=197/voipd
0.0.0.0:1004->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=13702 process=187/foauthd
0.0.0.0:8013->0.0.0.0:0->state=listen err=0 socktype=1 rma=0 wma=0 fma=0 tma=0 inode=14453 process=213/fsvrd
0.0.0.0:910->0.0.0.0:0->state=listen err=0 socktype=1 rma=0 wma=0 fma=0 tma=0 inode=18622 process=197/voipd
0.0.0.0:1007->0.0.0.0:0->state=listen err=0 socktype=2 rma=0 wma=0 fma=0 tma=0 inode=6084 process=353/ipsengine
0.0.0.0:10000->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20592 process=186/authd
0.0.0.0:2000->0.0.0.0:0->state=listen err=0 socktype=2 rma=0 wma=0 fma=0 tma=0 inode=18624 process=197/voipd
0.0.0.0:1011->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20600 process=186/authd
0.0.0.0:179->0.0.0.0:0->state=listen err=0 socktype=1 rma=0 wma=0 fma=0 tma=0 inode=8892 process=169/bgpd
0.0.0.0:1012->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20602 process=186/authd
0.0.0.0:10100->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20593 process=186/authd
127.0.0.1:54100->0.0.0.0:0->state=listen err=0 socktype=1 rma=0 wma=0 fma=0 tma=0 inode=18725 process=223/fgfmd
0.0.0.0:1013->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20601 process=186/authd
0.0.0.0:53->0.0.0.0:0->state=listen err=0 socktype=1 rma=0 wma=0 fma=0 tma=0 inode=18616 process=220/dnsproxy
0.0.0.0:1014->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20603 process=186/authd
0.0.0.0:22->0.0.0.0:0->state=listen err=0 socktype=1 rma=0 wma=0 fma=0 tma=0 inode=8791 process=212/sshd
0.0.0.0:1015->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20604 process=186/authd
127.0.0.1:8023->0.0.0.0:0->state=listen err=0 socktype=1 rma=0 wma=0 fma=0 tma=0 inode=14387 process=189/httpclid
0.0.0.0:1016->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20606 process=186/authd
0.0.0.0:10200->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20598 process=186/authd
0.0.0.0:1018->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=13706 process=187/foauthd
0.0.0.0:10300->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20590 process=186/authd
0.0.0.0:7900->0.0.0.0:0->state=listen err=0 socktype=2 rma=0 wma=0 fma=0 tma=0 inode=12791 process=233/dnsproxy
127.0.0.1:9980->0.0.0.0:0->state=listen err=0 socktype=1 rma=0 wma=0 fma=0 tma=0 inode=13738 process=177/httpsd
0.0.0.0:541->0.0.0.0:0->state=listen err=0 socktype=1 rma=0 wma=0 fma=0 tma=0 inode=18719 process=223/fgfmd
0.0.0.0:1023->0.0.0.0:0->state=listen err=0 socktype=4 rma=0 wma=0 fma=0 tma=0 inode=20605 process=186/authd
127.0.0.1:24363->127.0.0.1:80->state=time_wait err=0 socktype=4 inode=0 process=-
127.0.0.1:9980->127.0.0.1:8926->state=time_wait err=0 socktype=53392 inode=0 process=-
202.49.26.46:3798->202.49.26.1:179->state=established err=0 socktype=1 rma=0 wma=4928 fma=3264 tma=0 inode=25897 process=169/bgpd
59.153.21.177:4388->59.153.21.176:179->state=established err=0 socktype=1 rma=0 wma=0 fma=0 tma=0 inode=324579108 process=169/bgpd

```

#### Reference

<table border="1" id="bkmrk-https%3A%2F%2Fdocs.fortine" style="border-collapse: collapse; width: 100%;"><tbody><tr><td style="width: 100%;">[https://docs.fortinet.com/document/fortiadc/6.0.0/cli-reference/117564](https://docs.fortinet.com/document/fortiadc/6.0.0/cli-reference/117564)

[https://help.fortinet.com/fos50hlp/52data/Content/FortiOS/fortigate-system-administration-52/The%20CLI/using\_cli.htm](https://help.fortinet.com/fos50hlp/52data/Content/FortiOS/fortigate-system-administration-52/The%20CLI/using_cli.htm)

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-end-of-sop-sop-docum" style="border-collapse: collapse; width: 538.4pt; border-spacing: 0px; height: 192.986px;" width="718"><tbody><tr style="height: 23.2639px;"><td colspan="5" style="width: 538.4pt; border: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 23.2639px;" width="718">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">End Of SOP</span>**

</td></tr><tr style="height: 23.2639px;"><td colspan="5" style="width: 538.4pt; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 23.2639px;" width="718">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">SOP Document Version Control</span>**

</td></tr><tr style="height: 76.6667px;"><td style="width: 63.55pt; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 76.6667px;" width="85">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Version No:</span>**

</td><td style="width: 77.95pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 76.6667px;" width="104">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Effective Date</span>**

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 76.6667px;" width="146">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Author</span>**

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 76.6667px;" width="146">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Approver</span>**

</td><td style="width: 178pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 76.6667px;" width="237">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Brief Description of Change (referring Tack and Step)</span>**

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;"> </span>**

</td></tr><tr style="height: 23.2639px;"><td style="width: 63.55pt; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 23.2639px;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1.0</span>

</td><td style="width: 77.95pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">15 October 2020</span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> Blair Harrison </span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 178pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Creation artefact</span>

</td></tr><tr style="height: 23.2639px;"><td style="width: 63.55pt; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 23.2639px;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> 2.0</span>

</td><td style="width: 77.95pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> 04 December 2025</span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> Michelle Lee</span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 178pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Additional Commands </span>

</td></tr><tr style="height: 23.2639px;"><td style="width: 63.55pt; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 23.2639px;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> 2.1</span>

</td><td style="width: 77.95pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">10 December 2025 </span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Michelle Lee </span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">G Millar </span>

</td><td style="width: 178pt; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2639px;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Add in examples for newly added commands </span>

</td></tr></tbody></table>

**<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; color: white; mso-themecolor: background1;"> </span>**