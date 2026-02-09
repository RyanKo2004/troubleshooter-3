# All Vendors - Quick Cable Testing / Diagnostics

<p class="callout danger">WARNING: Running a cable test *will* be disruptive for PoE devices. They should be considered *possibly* disruptive to other connected device while the test runs. If in doubt get permission from the client, or check with Alan or Engineering.</p>

Is an interface:

- bouncing?
- getting errors?
- not negotiating to 1000/full?
- not providing PoE correctly?

There might be a cabling fault.

All our vendor's switches give you a means to perform a basic cable test. The tests are based on time domain reflectometry (TDR). These work by sending a signal down each pair of wires, then listening for the signal that is reflected from the other end. This can provide an estimate of cable length and indicate if a pair is broken.

<p class="callout info">NOTE: These on board tests are not going to be as reliable or accurate as a cable test with specialist equipment that's placed on both ends. Their results should be considered *strongly suggestive*. You should really only be doing a cable test if there is already some indicator that there is an issue.</p>

##### Cable Pairs &amp; 100 Mbps

Both Cisco and Huawei refer to pairs A, B, C, D. These pairs should be:

<table border="1" id="bkmrk-a-this-pair-controls" style="border-collapse: collapse; width: 100%;"><tbody><tr><td style="width: 8.51855%;">A</td><td style="width: 91.4815%;">This pair controls whether or not the port should go up or down.</td></tr><tr><td style="width: 8.51855%;">B</td><td style="width: 91.4815%;">Protocol-level and controls FastEthernet.</td></tr><tr><td style="width: 8.51855%;">C</td><td style="width: 91.4815%;">Power over Ethernet (PoE)</td></tr><tr><td style="width: 8.51855%;">D</td><td style="width: 91.4815%;">Gigabit</td></tr></tbody></table>

So a connection running at 100 Mbps needs to be considered carefully. It could be that the device only supports 100 Mbps. But potentially a bad cable could result in only 100 Mbps being possible.

*\* Taken from the Cisco reference listed at the end of this page.*

### **Cisco**

Cisco has the "test cable-diagnostics tdr" command.

Even though there are no messages indicating the interface goes down, you should assume testing causes some disruption to an interface that is up.

```
CELLO-S004-SW01#test cable-diagnostics tdr interface gi1/0/9
TDR test started on interface Gi1/0/9
A TDR test can take a few seconds to run on an interface
Use 'show cable-diagnostics tdr' to read the TDR results.

CELLO-S004-SW01#show cable-diagnostics tdr int gi1/0/9

TDR test last run on: October 06 11:34:40

Interface Speed Local pair Pair length        Remote pair Pair status
--------- ----- ---------- ------------------ ----------- --------------------
Gi1/0/9   1000M Pair A     33   +/- 10 meters Pair A      Normal              
                Pair B     33   +/- 10 meters Pair B      Normal              
                Pair C     33   +/- 10 meters Pair C      Normal              
                Pair D     33   +/- 10 meters Pair D      Normal       

```

The key things to check are:

- Speed is 1000M
- Does the *Local pair* match the *Remote pair*?
- Are all pairs the same (or very similar) length?
- Is the *Pair status* Normal (good)? Anything else is bad.

This is a greatly summarised; for much more detail on the output see the Cisco reference at the end.

Here are some examples of bad test results:

```
Interface Speed Local pair Pair length        Remote pair Pair status
--------- ----- ---------- ------------------ ----------- --------------------
Gi1/0/10  100M  Pair A     N/A                Pair B      Normal              
                Pair B     N/A                Pair A      Normal              
                Pair C     28   +/- 10 meters Pair D      Short               
                Pair D     27   +/- 10 meters Pair C      Short       

```

The pairs do not match and some pairs have no length detected.

```
Interface Speed Local pair Pair length        Remote pair Pair status
--------- ----- ---------- ------------------ ----------- --------------------
Gi1/0/16  auto  Pair A     24   +/- 10 meters N/A         Short/Crosstalk     
                Pair B     24   +/- 10 meters N/A         Short/Crosstalk     
                Pair C     24   +/- 10 meters N/A         Open                
                Pair D     25   +/- 10 meters N/A         Open           

```

Remote pair hasn't been detected; crosstalk has been detected on some pairs.

```
Interface Speed Local pair Pair length        Remote pair Pair status
--------- ----- ---------- ------------------ ----------- --------------------
Gi1/0/20  100M  Pair A     5    +/- 10 meters N/A         Normal              
                Pair B     5    +/- 10 meters N/A         Normal              
                Pair C     6    +/- 5  meters N/A         Short               
                Pair D     6    +/- 5  meters N/A         Short   

```

Remote pair hasn't been detected; shorting has been detected on some pairs.

### **Huawei**

Huawei has the "virtual-cable-test" command.

I'm not sure this is as reliable as the Cisco version. I've tried it on a lot of interfaces and am yet to get a no-zero length reported on all pairs.

For an interface that is up, messages will be logged showing the interface bouncing.\*

\* Usually. Sometimes the "test" seems to run in zero time, the interface doesn't bounce, no lengths are reported, and it just says all pairs are OK.

```
<PSO-S004-SW02>system-view
Enter system view, return user view with Ctrl+Z.
[PSO-S004-SW02]interface gi0/0/41
[PSO-S004-SW02-GigabitEthernet0/0/41]virtual-cable-test 
Warning: The command will stop service for a while. Continue? [Y/N]:y
Info: This operation may take a few seconds. Please wait for a moment..................done.
Pair A length: 0meter(s)
Pair B length: 0meter(s)
Pair C length: 0meter(s)
Pair D length: 0meter(s)
Pair A state: Open
Pair B state: Open
Pair C state: Open
Pair D state: Open
Info: The test result is only for reference.

```

If you need to display the result again, you can do so with "display virtual-cable-test"

```
[PSO-S004-SW02-GigabitEthernet0/0/41]display virtual-cable-test gi0/0/41
VCT test last ran on: 2020-10-06 10:48:16 DST
Pair A length: 0meter(s)
Pair B length: 0meter(s)
Pair C length: 0meter(s)
Pair D length: 0meter(s)
Pair A state: Open
Pair B state: Open
Pair C state: Open
Pair D state: Open
Info: The test result is only for reference.

```

The test must be run from "system-view" mode. The results can be displayed from any mode.

```
<PSO-S001-SW08>system-view 
Enter system view, return user view with Ctrl+Z.
[PSO-S001-SW08]int gi0/0/17
[PSO-S001-SW08-GigabitEthernet0/0/17]vi
[PSO-S001-SW08-GigabitEthernet0/0/17]virtual-cable-test 
Warning: The command will stop service for a while. Continue? [Y/N]:y
Info: This operation may take a few seconds. Please wait for a moment...
2020-10-6 11:53:57+13:00 DST PSO-S001-SW08 %%01IFPDT/4/IF_STATE(l)[0]:Interface GigabitEthernet0/0/17 has turned into DOWN state.
2020-10-6 11:53:57+13:00 DST PSO-S001-SW08 %%01IFADP/4/PORTDOWNINFO(l)[1]:Interface GigabitEthernet0/0/17 has turned into DOWN state. (Information=Physical state: down, Negotiation: enable, Negotiation complete: no, Local full-duplex(10M: yes, 100M: yes, 1000M: yes), Local half-duplex(10M: yes, 100M: yes, 1000M: no), Remote full-duplex(10M: no, 100M: no, 1000M: no), Remote half-duplex(10M: no, 100M: no, 1000M: no))
Oct  6 2020 11:53:57+13:00 DST PSO-S001-SW08 LLDP/4/NBRCHGTRAP:OID 1.0.8802.1.1.2.0.0.1 Neighbor information is changed. (LldpStatsRemTablesInserts=0, LldpStatsRemTablesDeletes=1, LldpStatsRemTablesDrops=0, LldpStatsRemTablesAgeouts=0)...............done.
Pair A length: Unknown
Pair B length: Unknown
Pair C length: 24meter(s)
Pair D length: 23meter(s)
Pair A state: Ok
Pair B state: Ok
Pair C state: Short
Pair D state: Short
Info: The test result is only for reference.
[PSO-S001-SW08-GigabitEthernet0/0/17]
Oct  6 2020 11:54:08+13:00 DST PSO-S001-SW08 LLDP/4/NBRCHGTRAP:OID 1.0.8802.1.1.2.0.0.1 Neighbor information is changed. (LldpStatsRemTablesInserts=1, LldpStatsRemTablesDeletes=0, LldpStatsRemTablesDrops=0, LldpStatsRemTablesAgeouts=0)
2020-10-6 11:54:08+13:00 DST PSO-S001-SW08 %%01IFPDT/4/IF_STATE(l)[2]:Interface GigabitEthernet0/0/17 has turned into UP state.

```

Notice the interface goes down during the test, and comes back up after the test.

### **Fortinet**

The FortiSwitches managed by a local FortiGate or by FortiManager can also run cable tests.

6.4 or later is required.

**From FortiManager**

- Once you have navigated to the switch, you need to Lock the configuration before running the test.
- [https://docs.fortinet.com/document/fortimanager/6.4.2/administration-guide/75376/run-cable-test-on-fortiswitch-ports-from-fortimanager](https://docs.fortinet.com/document/fortimanager/6.4.2/administration-guide/75376/run-cable-test-on-fortiswitch-ports-from-fortimanager)

**From the FortiGate**

- You need to be in Read/Write mode to be able to run the test.
- [https://docs.fortinet.com/document/fortiswitch/6.4.2/devices-managed-by-fortios/968028/using-the-fortigate-gui#Run\_Cable\_Test](https://docs.fortinet.com/document/fortiswitch/6.4.2/devices-managed-by-fortios/968028/using-the-fortigate-gui#Run_Cable_Test)

If you at the CLI of the switch, I think you should be able to use the command `diagnose switch physical-ports cable-diag <physical port name>`.

### **Aruba CX Switch**

There are two methods to run Cable Diagnostics with the Aruba CX Switches, either from Aruba Central or from the switch CLI.

#### **Aruba Central Method**

Using Aruba Central, from the switch group

1. **Tools**
2. **Device Check**
3. Select the **Source** switch from the list
4. Select the **Cable Test** from the list of tests
5. Enter the **Port** number e.g. 1/1/34
6. Click on the **Run** button to execute the test
7. After a minute the results will be updated.

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/scaled-1680-/5s7image.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/5s7image.png)

Using Aruba Central to

#### **CLI Method**

The CLI method first requires **enabling diagnostics** on the switch to use the **diag** sub-commands. With diagnostic enabled, the other diag commands are now available.

```shell
ANZCO-S003-SW04# term
Terminal-monitor is enabled successfully

ANZCO-S003-SW04# diagnostics 

ANZCO-S003-SW04# diag cable-diagnostic test 1/1/34
This command will cause a loss of link on the port under test
and will take several seconds to complete.

Continue (y/n)? y
ANZCO-S003-SW04# 
2024-01-10T09:40:59.835696+1300 intfd[617] <INFO> Event|404|LOG_INFO|AMM|1/1|Link status for interface 1/1/34 is down
2024-01-10T09:41:02.204382+1300 intfd[617] <INFO> Event|403|LOG_INFO|AMM|1/1|Link status for interface 1/1/34 is up at 100 Mbps
2024-01-10T09:41:02.768717+1300 intfd[617] <INFO> Event|404|LOG_INFO|AMM|1/1|Link status for interface 1/1/34 is down
2024-01-10T09:41:05.567329+1300 intfd[617] <INFO> Event|403|LOG_INFO|AMM|1/1|Link status for interface 1/1/34 is up at 100 Mbps

ANZCO-S003-SW04# diag cable-diagnostic show 1/1/34
                          Cable        Impedance    Distance*   MDI
Interface        Pinout   Status       (Ohms)       (Meters)    Mode
---------------------------------------------------------------------
1/1/34           1-2      good         85-115       58 +/- 10   mdi 
(1GbT)           3-6      open         >115          2 +/- 5    mdi 
                 4-5      intra_short  <85          56 +/- 5    mdi 
                 7-8      intra_short  <85          54 +/- 5    mdi 

* Full cable length for good cables or distance to fault for faulty cables.

Cable status legend (1GbT):

Cable        Impedance
Status       (Ohms)     Description
----------------------------------------------------------------
good         85-115     No cable faults found
open         >115       Open circuit detected
intra_short  <85        Short circuit within the same wire pair
inter_short  <85        Short circuit with another wire pair
high_imp     >115       Cable impedance higher than expected
low_imp      <85        Cable impedance lower than expected
unknown      --         Cable test inconclusive
ANZCO-S003-SW04#        
```

#### Results 

Interpreting the results provided by Aruba CX switches from the example above. The Aruba CX switches include the cable resistance in the results.

While this port is sort of working at 100Mbps there are a lot of errors on the interfere.

As shown in the example:

- Pair 1-2 are with in expected cable resistance (85-115Ω).
- Pair 3-6 excess the expected cable resistance (&gt;115Ω) and therefore probably open.
- Pair 4-5 less than the expected cable resistance (&lt;85Ω) shorted
- Pair 7-8 less than the expected cable resistance (&lt;85Ω) shorted

As we know for 100BASE-TX Ethernet it requires a minimum of 2 pairs to operate. We know the interface is up at 100Mbps but there are a lot of errors, therefore we can assume that pair 3-6 isn't open but has a poor termination causing the high resistance.   
Clearly the is still still a short on the other cable pairs as shown in the output.

### **Meraki**

<p class="callout info">**July 2025:** There is a known issue on C9300 Meraki switches running CS17.x.x where the cable test doesn't work, you might need to try it a few times </p>

##### Things to know:   


- Can only be done on the MS (Switches) not the MX,
- Make sure the cable is connected to devices at both ends, before running this test.
- Can only be done with copper cabling not fibre.

##### To run a cable test:

1. From the Dashboard navigate to Switching&gt;Switches then choose a switch and navigate to the Tools section
2. Scroll to the Cable Test section
3. Enter the port or port range (e,g. "1" or "1-24" without quotes) and hit Run
4. [![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/scaled-1680-/0ptimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/0ptimage.png)

##### Test outputs

<table border="1" id="bkmrk-ok-good-cable-and-go" style="border-collapse: collapse; width: 100%; height: 152.766px;"><colgroup><col style="width: 50%;"></col><col style="width: 50%;"></col></colgroup><tbody><tr style="height: 57.7812px;"><td style="height: 57.7812px;">OK

</td><td style="height: 57.7812px;">Good cable and good pair

</td></tr><tr style="height: 35.3906px;"><td style="height: 35.3906px;">OPEN

</td><td style="height: 35.3906px;">Unused or terminated pair  
</td></tr><tr style="height: 29.7969px;"><td style="height: 29.7969px;">ABNORMAL</td><td style="height: 29.7969px;">The impedance is not within the expected bounds, either too high or too low

</td></tr><tr style="height: 29.7969px;"><td style="height: 29.7969px;">COUPLEX</td><td style="height: 29.7969px;">Specified pair too strongly coupled to pair X, indicating a high amount of crosstalk

</td></tr></tbody></table>

#### Examples of output

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/scaled-1680-/r64image.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/r64image.png)

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/scaled-1680-/mBlimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/mBlimage.png)


#### **Reference**

[https://en.wikipedia.org/wiki/Ethernet\_over\_twisted\_pair](https://en.wikipedia.org/wiki/Ethernet_over_twisted_pair)

[https://community.cisco.com/t5/networking-documents/how-to-use-time-domain-reflectometer-tdr/ta-p/3119327](https://community.cisco.com/t5/networking-documents/how-to-use-time-domain-reflectometer-tdr/ta-p/3119327)

[https://support.huawei.com/enterprise/en/doc/EDOC1000178172/25edcf9/configuring-virtual-cable-test](https://support.huawei.com/enterprise/en/doc/EDOC1000178172/25edcf9/configuring-virtual-cable-test)

[https://www.arubanetworks.com/techdocs/AOS-CX/10.10/HTML/diagnostics\_4100i-6000-6100/Content/Chp\_CabDiag/cab-dia.htm](https://www.arubanetworks.com/techdocs/AOS-CX/10.10/HTML/diagnostics_4100i-6000-6100/Content/Chp_CabDiag/cab-dia.htm)