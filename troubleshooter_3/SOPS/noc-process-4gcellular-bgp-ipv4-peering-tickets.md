# NOC PROCESS - 4G/Cellular BGP IPv4 Peering Tickets

![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/embedded-image-zevk8fn2.png)

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-purpose-%C2%A0-scope-%C2%A0-bu" style="border-collapse: collapse; width: 720px; height: 261.953px; border-spacing: 0px;" width="720"><tbody><tr style="height: 46.5938px;"><td style="width: 87.5938px; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 46.5938px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Purpose</span>**

</td><td class="align-left" style="width: 636px; height: 46.5938px;">This is the process to follow when the NOC are resolving a 4G BGP peering alert for a cellular connection.

</td></tr><tr style="height: 32.375px;"><td style="width: 87.5938px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 32.375px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Scope</span>**

</td><td class="align-left" style="width: 636px; height: 32.375px;">NOC, 4G BGP Peering Alerts, NOC Team, All 4G Backup Clients.</td></tr><tr style="height: 34.5938px;"><td style="width: 87.5938px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 34.5938px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Business Rules</span>**</td><td class="align-left" style="width: 636px; height: 34.5938px;">This is part of the process for the resolution of the 4G services for the clients backup connection</td></tr><tr style="height: 29.7969px;"><td style="width: 87.5938px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 29.7969px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Inputs</span>**

</td><td class="align-left" style="width: 636px; height: 29.7969px;">LogicMonitor Networking Alerting, ticket BGP 4G alerts.

</td></tr><tr style="height: 48px;"><td style="width: 87.5938px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 48px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Outputs</span>**

</td><td class="align-left" style="width: 636px; height: 48px;">Resolved ticket - potentially adjustment/ replacement of the antenna, or been solved through deployment of a new 4G solution.

</td></tr><tr style="height: 70.5938px;"><td style="width: 87.5938px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 70.5938px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Notes</span>**

</td><td class="align-left" style="width: 636px; height: 70.5938px;"><p class="callout warning">NOTE: for the whole process NOC member(s) will maintain ownership of the ticket unless advised by engineering.</p>

</td></tr></tbody></table>

**PROCESS FLOW CHART**

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-05/scaled-1680-/g0Ximage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-05/g0Ximage.png)

##### Check for **primary** or **secondary** connection. Disabling a **4G primary** site can cause a **significant outage.** 

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-1-%E2%80%93-1-%C2%A0-2" style="border-collapse: collapse; width: 718px; height: 158px; border-spacing: 0px;" width="718"><tbody><tr style="height: 28px;"><td style="width: 67.125px; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 28px;" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 651.266px; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 28px;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">**Ticket Types**</span>**

</td></tr><tr style="height: 65px;"><td style="width: 67.125px; height: 65px;">**1**

</td><td class="align-left" style="width: 651.266px; height: 65px;">**The Signal Cellular tickets**

**[https://bookstack.cello.co.nz/books/4g-processes/page/noc-process-4gcellular-signal-issue-tickets](https://bookstack.cello.co.nz/books/4g-processes/page/noc-process-4gcellular-signal-issue-tickets)**

</td></tr><tr style="height: 65px;"><td style="width: 67.125px; height: 65px;">**2**

</td><td style="width: 651.266px; height: 65px;">**4G BGP peering Tickets**

These tickets generate after 5 minutes or so of visible issues - theses alerts generate due to the 4G BGP peering to the CORE being unreachable or impacted, they can be investigated right away.

</td></tr></tbody></table>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-1a---noc-" style="border-collapse: collapse; width: 718px; height: 253.438px; border-spacing: 0px;" width="718"><tbody><tr style="height: 42.3906px;"><td style="width: 67.125px; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 42.3906px;" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td class="align-left" style="width: 651.266px; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 42.3906px;" width="651">##### **<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">**Task 1A - Acknowledgement and Observation**</span>**

</td></tr><tr style="height: 211.047px;"><td style="width: 67.125px; height: 211.047px;">**1**

</td><td class="align-left" style="width: 651.266px; height: 211.047px;">If the ticket clears on its own then use the "**Resolve - 4G Complete**" Scenario within Fresh service to close the ticket - However if after 50 minutes the ticket hasn't cleared, then check the following:

- **BGP Peering history** - Does this peering flap constantly or is this a one-off event?
- **Signal quality** - Is this why it is flapping constantly
- **SDT** - Consider if an SDT needs to be applied to the alert type? This will prevent numerous tickets from being generated while you ID root cause.

- Then continue with "**Task 1B - NOC - Troubleshooting and Resetting 4G interfaces**".

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-2-%E2%80%93-1-%C2%A0-2" style="border-collapse: collapse; width: 720px; border-spacing: 0px; height: 1518.36px;" width="720"><tbody><tr style="height: 42.3906px;"><td style="width: 68.7188px; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 42.3906px;" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 651.266px; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 42.3906px;" width="651">##### **<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">**Task 1B - First Level Troubleshooting and Resetting 4G interfaces** </span>**

</td></tr><tr style="height: 369.062px;"><td style="width: 68.7188px; height: 369.062px;">**1**

</td><td style="width: 651.266px; height: 369.062px;">Firstly, identify the Device type of the affected equipment:

- Cisco,
- Huawei or
- FortiGate FEX.

For example Netbox identifies "SUN-S021-RT01" as a cisco router:

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/scaled-1680-/mKeimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/mKeimage.png)

  
Alternativity if you login to the impacted device you can identify the device that way, for FortiGate device's they will have some forum of "FW" within their device name. while with the other devices, we can identify them by looking at the command syntax, for example: on a cisco device to view the device version information run the "show version" command however on a Huawei device you run the "display version" command instead.

<p class="callout warning align-left">**Note:** while in Netbox identify if the service is provided by spark or a different provider.</p>

</td></tr><tr style="height: 805.828px;"><td style="width: 68.7188px; height: 805.828px;">**2**

</td><td style="width: 651.266px; height: 805.828px;">For **non-spark** services <span style="text-decoration: underline;">skip</span> to the next step.

For Spark cellular services, check the service within Jasper:

<span style="text-decoration: underline;">spark.jasperwireless.com</span>

For example: "**SUN-S021-RT01**" which is a cisco router:

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/scaled-1680-/jqnimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/jqnimage.png)

  
Currently Jasper is reporting that the cellular service for this router is in session as indicated under the "**In Session**" heading:

  
[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/scaled-1680-/aGaimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/aGaimage.png)

We can also click on the ICCID number to run diagnostics:

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/scaled-1680-/hXIimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/hXIimage.png)

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/scaled-1680-/567image.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/567image.png)

<p class="callout warning">In some cases, it tells us the service is in session, however the 4G peering may still be impacted.</p>

</td></tr><tr style="height: 46.5938px;"><td style="width: 68.7188px; height: 46.5938px;">**3**

</td><td class="align-left" style="width: 651.266px; height: 46.5938px;">Based on the device type identified, follow the related process for resetting the 4G interfaces (See below for links)</td></tr><tr style="height: 65.75px;"><td style="width: 68.7188px; height: 65.75px;">**3A**

</td><td style="width: 651.266px; height: 65.75px;">For <span style="text-decoration: underline;">**Cisco**</span> devices:

 [NOC PROCESS - Resetting 4G Interfaces - Cisco (SOP)](https://bookstack.cello.co.nz/books/4g-processes/page/noc-process-resetting-4g-interfaces-cisco-sop)"

</td></tr><tr style="height: 68.9844px;"><td style="width: 68.7188px; height: 68.9844px;">**3B**

</td><td style="width: 651.266px; height: 68.9844px;">For <span style="text-decoration: underline;">**Huawei**</span> devices:

[NOC PROCESS - Resetting 4G Interfaces - Huawei (SOP)](https://bookstack.cello.co.nz/books/4g-processes/page/noc-process-resetting-4g-interfaces-huawei-sop)

</td></tr><tr style="height: 70.75px;"><td style="width: 68.7188px; height: 70.75px;">**3C**

</td><td style="width: 651.266px; height: 70.75px;">For **<span style="text-decoration: underline;">Fortigate</span>** devices:

[NOC PROCESS - Resetting 4G on Fortiextender (FEX) from FortiGate Firewall (SOP)](https://bookstack.cello.co.nz/books/4g-processes/page/noc-process-resetting-4g-on-fortiextender-fex-from-fortigate-firewall-sop)" -

</td></tr><tr style="height: 49px;"><td style="width: 68.7188px; height: 49px;">**4**

</td><td class="align-left" style="width: 651.266px; height: 49px;">If this didn't resolve the issues with the BGP peering or cellular connectivity, then follow "**Task 1C - NOC - Further Troubleshooting**"</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-2-%E2%80%93-1-%C2%A0-2-1" style="border-collapse: collapse; width: 720px; border-spacing: 0px; border: initial none initial;" width="720"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes; height: 23.55pt;"><td style="width: 68.7188px; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 23.55pt;" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 651.266px; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 23.55pt;" width="651">##### **<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">**Task 1C Further Troubleshooting**</span>**

</td></tr><tr style="mso-yfti-irow: 1;"><td style="width: 68.7188px;">**1**

</td><td style="width: 651.266px;">Before continuing with "**Further Troubleshooting**", in certain cases the cellular signal might be temporally bad in an area, this is due to it being a best effort service along with atmospheric conditions and other factors.

As such after the first day where you have reset the interface a few times within that day, Wait another day or so and reset the interface a few more times (as sometimes it will just end up fixing itself the next day after interface resets.)

However, if this isn't the case then continue below with step 3.

</td></tr><tr style="mso-yfti-irow: 2; mso-yfti-lastrow: yes;"><td style="width: 68.7188px;">**2**

</td><td style="width: 651.266px;"><p class="callout warning align-left">Note: if the cellular card is identified to be faulty in the previous device 4G interface resetting steps then proceed to step 4B.</p>

Identify the cellular connectivity to the device, along with what cellular band (4G(**LTE**) or 3G(**GSM/UMTS**)) the device is using, this can be done by following below:

For <span style="text-decoration: underline;">**Huawei** </span>devices use:

"*<span class="fontstyle0">display cellular &lt;4G Interface&gt; radio"</span>*<span class="fontstyle0"> to retried the cellular statistics from the device. </span>

<span class="fontstyle0">you can also record the result of:</span>

<span class="fontstyle0">"*display cellular &lt;4G Interface&gt; all*" command which identifies other potentially useful information such as selected / current cellular network type.</span>

For <span style="text-decoration: underline;">**Cisco**</span> devices use:

"*<span class="fontstyle0">show cellular &lt;4G Interface&gt; radio</span>*<span class="fontstyle0">" to retried the cellular statistics from the device or to filter results use:</span>

<span class="fontstyle0">*sh cellular &lt;4G Interface&gt; radio | inc RSSI  
sh cellular &lt;4G Interface&gt; radio | inc RSRP  
sh cellular &lt;4G Interface&gt; radio | inc SNR* </span>

On <span style="text-decoration: underline;">**Cisco**</span> device you can also use the "<span class="fontstyle0">*show cellular &lt;4G Interface&gt; all*" to view all information, however on cisco they list the selected cellular band within the output of the "*show cellular &lt;4G Interface&gt; radio*" command</span>

<span class="fontstyle0">Once you have retired the stats from the device put these in the ticket and then compare to the graphic below to determine reception quality:</span>

<span class="fontstyle0">[![image-1601868229207.png](https://bookstack.cello.co.nz/uploads/images/gallery/2020-10/scaled-1680-/image-1601868229207.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2020-10/image-1601868229207.png)</span>

<p class="callout info align-left"><span class="fontstyle0">Note: for persistent device that alert a lot this could be the cause is the Signal is not good enough in the area</span></p>

<span class="fontstyle0">Another thing to look at is the **provider coverage maps**: for example if it is a Spark SIM check the Spark coverage in the area - if Spark say it should have good signal but we can see its within the fair or poor range this could mean that the antenna needs to be adjusted to get a better signal or replaced with an indoor external 4g antenna to help get better signal.</span>

<span style="text-decoration: underline;"><span style="color: rgb(0, 0, 0); text-decoration: underline;">**<span class="fontstyle0">Coverage Map List:</span>**</span></span>

<span class="fontstyle0">[https://www.spark.co.nz/shop/mobile/network/](https://www.spark.co.nz/shop/mobile/network/)</span>

<span class="fontstyle0">[https://www.vodafone.co.nz/network/coverage/](https://www.vodafone.co.nz/network/coverage/)</span>

<span class="fontstyle0">[https://www.2degrees.nz/coverage/](https://www.2degrees.nz/coverage/)</span>

<p class="callout warning"><span class="fontstyle0">Note: a lot of our clients are on Spark with a few on Vodafone - currently none on 2 Degrees</span></p>

</td></tr><tr><td style="width: 68.7188px;">**3**

</td><td class="align-left" style="width: 651.266px;"><span style="text-decoration: underline;">**Photos:**</span>

During the install process - we usually request the NEC technician/installer take photos of the installation - have a look at these photos to work out the position of the antennas, however if you can't from the current pictures, request new picture from the client.

</td></tr><tr><td style="width: 68.7188px;">**4**

</td><td style="width: 651.266px;">**<span style="text-decoration: underline;">Contacting the client:</span>**

At this point the cello NOC should advise the client that their 4G/ Cellular backup service is impacted. There is a template in Outlook.

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/scaled-1680-/aGFimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2026-01/aGFimage.png)

**Optional questions you could ask depending on issue:**

- <span lang="EN-US">Can you please check the POE injector is plugged in and providing power to the FEX &lt;FEX name&gt;</span>
- <span lang="EN-US">Check that the POE injector is plugged into the Firewall in &lt;port number of firewall&gt; to LAN port of the POE injector – then POE port to the FEX in LAN port 4.</span>
- <span lang="EN-US">If the device has power, can you please manually power cycled the FEX?</span>
- <span lang="EN-US">can we arrange a time to perform a reboot of the router &lt;router name&gt;? (only if site is using router) </span>

</td></tr><tr><td style="width: 68.7188px;">**5**

</td><td style="width: 651.266px;"><p class="callout warning align-left">For suspected faulty **cellular cards**</p>

**Note:** if the cellular card is identified to be faulty - Escalate to ben crooks and NSE to verify, after verification, depending on the error we may want to request and arrange a device reboot with the client - if this doesn't resolve the issue then advise engineering and arrange a replacement cellular card.

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-2-%E2%80%93-1-%C2%A0-2-2" style="border-collapse: collapse; width: 721px; border-spacing: 0px; height: 111.578px;" width="720"><tbody><tr style="height: 42.3906px;"><td style="width: 68.7188px; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 42.3906px;" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 651.266px; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 42.3906px;" width="651">##### **<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">**Task 2 - Engineering** </span>**

</td></tr><tr style="height: 34.5938px;"><td style="width: 68.7188px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 34.5938px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 651.266px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 34.5938px;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">After NOC's escalation to Engineering they will verify the information provided by NOC, to confirm the status of the cellular card. </span>

</td></tr><tr style="height: 34.5938px;"><td style="width: 68.7188px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 34.5938px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 651.266px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 34.5938px;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">if requested NOC can use FEX replacement SOP for FortiGate - confirm with Senior NOC first as well - https://bookstack.cello.co.nz/books/4g-processes/page/noc-process-4g-fex-replacement-sop</span>

</td></tr></tbody></table>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-wip---external" style="border-collapse: collapse; width: 721px; border-spacing: 0px; height: 111.578px;" width="720"><tbody><tr style="height: 42.3906px;"><td style="width: 68.7188px; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 42.3906px;" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 651.266px; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 42.3906px;" width="651">##### **<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">**WIP - External Antennae**</span>**

</td></tr><tr style="height: 34.5938px;"><td style="width: 68.7188px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 34.5938px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 651.266px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 34.5938px;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">After Engineering have reviewed the 4G status the next steps are to install a higher gain antennae or move the FEX to a better position.</span>

</td></tr><tr style="height: 34.5938px;"><td style="width: 68.7188px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 34.5938px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 651.266px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 34.5938px;" valign="top" width="651">Cisco/Huawei:

We provide a Mikrotik 5Db gain outdoor antennae, the MikroTik MTAO-LTE-5D-SQ.

Hi \[Customer Name\],

Due to poor cellular signal at your location, we recommend installing an external antenna to improve connectivity.

Please approve a One-off cost of $100 to ship the antennae to you.

Additional costs apply if Cello need to provide a tech for the install.

**Installation Details:**

- The box includes a 3m cable to mount the antenna in a suitable position
- Please position the antenna where signal strength is optimal

If you have any questions about the installation process or need further assistance, please don't hesitate to reach out to the NOC on 0800 225 662.

**Ensure the box has appropriate mounting brackets and 3m cable before sending to customer**

</td></tr><tr><td style="width: 68.7188px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt;">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">  
</span>**

</td><td style="width: 651.266px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt;">Fortigate FEX:

the Fortigate can be routed through internal cabling using a ethernet cable to reach a better position.

</td></tr></tbody></table>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-end-of-sop-sop-docum-1" style="border-collapse: collapse; width: 538.4pt; border-spacing: 0px; height: 193.25px;" width="718"><tbody><tr style="height: 23.25px;"><td colspan="5" style="width: 717.842px; border: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 23.25px;" width="718">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">End Of SOP</span>**

</td></tr><tr style="height: 23.25px;"><td colspan="5" style="width: 717.842px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 23.25px;" width="718">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">SOP Document Version Control</span>**

</td></tr><tr style="height: 77px;"><td style="width: 143.562px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77px;" width="85">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Version No:</span>**

</td><td style="width: 143.562px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77px;" width="104">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Effective Date</span>**

</td><td style="width: 143.562px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77px;" width="146">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Author</span>**

</td><td style="width: 143.562px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77px;" width="146">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Approver</span>**

</td><td style="width: 143.594px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77px;" width="237">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Brief Description of Change (referring Tack and Step)</span>**

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;"> </span>**

</td></tr><tr style="height: 23.25px;"><td style="width: 143.562px;">1.0

</td><td style="width: 143.562px;">28 April 2022

</td><td style="width: 143.562px;">G Millar

</td><td style="width: 143.562px;"></td><td style="width: 143.594px;">Creation artefact

</td></tr><tr style="height: 23.25px;"><td style="width: 143.562px;">1.2

</td><td style="width: 143.562px;"></td><td style="width: 143.562px;">G Millar

</td><td style="width: 143.562px;"></td><td style="width: 143.594px;">Updates for Tier system

</td></tr><tr style="height: 23.25px;"><td style="width: 143.562px;">2.0

</td><td style="width: 143.562px;">10/06/2024

</td><td style="width: 143.562px;">G Millar

</td><td style="width: 143.562px;"></td><td style="width: 143.594px;">Update to new SOP format

</td></tr><tr><td style="width: 143.562px;">2.1

</td><td style="width: 143.562px;">18/06/2024

</td><td style="width: 143.562px;">G Millar

</td><td style="width: 143.562px;"></td><td style="width: 143.594px;">link to FEX replacement SOP

</td></tr></tbody></table>

**<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; color: white; mso-themecolor: background1;"> </span>**