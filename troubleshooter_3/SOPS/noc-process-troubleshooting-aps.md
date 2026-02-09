# NOC PROCESS - Troubleshooting APs

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

**<span style="font-size: 9.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;">Standard Operating Process- Troubleshooting APs</span>**

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-purpose-to-provide-a" style="border-collapse: collapse; width: 720px; height: 381.6px; border-spacing: 0px; border: initial none initial;" width="720"><tbody><tr style="height: 45.6px;"><td style="width: 65.7pt; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 45.6px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Purpose</span>**

</td><td style="width: 474.3pt; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; padding: 0cm 5.4pt; height: 45.6px;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">To provide a standardised troubleshooting approach to remedy Access Points (APs) that are alerting as an outage. </span>

</td></tr><tr style="height: 27.2px;"><td style="width: 65.7pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 27.2px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Scope</span>**

</td><td style="width: 474.3pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 27.2px;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">NOC, Cello Engineer, Cello clients with Cello managed APs.</span>

</td></tr><tr style="height: 45.6px;"><td style="width: 65.7pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 45.6px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Business Rules</span>**

</td><td style="width: 474.3pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 45.6px;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; background: yellow; mso-highlight: yellow; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">Applies when an access point alerts as going down. This will usually display as a ‘ping’ alert in Freshservice.</span>

</td></tr><tr style="height: 64px;"><td style="width: 65.7pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 64px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Inputs</span>**

</td><td style="width: 474.3pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 64px;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">Ticket received in Freshservice indicating that an access point has gone down. E.g. ‘ANZCO-S998-WLC01 - Access Point-AFPTAAP02’, ‘PUBT-S999-WLC01 - Access Point-PUBT-S027-AP01’ and so on. Alerts can also arrive via other alerting system such as email, phone call and so on.</span>

</td></tr><tr style="height: 45.6px;"><td style="width: 65.7pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 45.6px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Outputs</span>**

</td><td style="width: 474.3pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 45.6px;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">Device is successfully rebooted, if it is not successfully rebooted then client will need to be notified of the outage where it can be remedied on-site.</span>

</td></tr><tr style="height: 153.6px;"><td style="width: 65.7pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 153.6px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Notes</span>**

</td><td style="width: 474.3pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 153.6px;" valign="top" width="632">*<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: black; mso-themecolor: text1; mso-fareast-language: EN-NZ;">The process for access points varies slightly depending on the device make and what other networking devices it may be connected to.</span>*

*<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: black; mso-themecolor: text1; mso-fareast-language: EN-NZ;"> </span>*

*<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: black; mso-themecolor: text1; mso-fareast-language: EN-NZ;">AP = Access Point</span>*

*<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: black; mso-themecolor: text1; mso-fareast-language: EN-NZ;"> </span>*

*<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: black; mso-themecolor: text1; mso-fareast-language: EN-NZ;">XXX-SXXX-WLC01 = The WLC (Wireless Lan Controller) is used to configure and manage the APs from a remote location. The APs are not physically connected to this device.</span>*

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

**<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;">PROCESS FLOW CHART</span>**

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; mso-bidi-font-weight: bold;">Task 1 – Identifying the Network layout</span>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; mso-bidi-font-weight: bold;">Task 2 – Cycling the AP port (rebooting the AP)</span>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; mso-bidi-font-weight: bold;">Task 3 – Rebooting on non-cli systems (Aruba, Meraki, Aerohive, FortiGate)</span>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; mso-bidi-font-weight: bold;">Task 4 – Failure to bring the AP back online</span>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-1-%E2%80%93-ident" style="border-collapse: collapse; width: 718px; border-spacing: 0px; border: initial none initial;" width="718"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes; height: 18.15pt;"><td style="width: 50.35pt; border: solid silver 1.0pt; mso-border-top-alt: .5pt; mso-border-left-alt: .5pt; mso-border-bottom-alt: .75pt; mso-border-right-alt: .75pt; mso-border-color-alt: silver; mso-border-style-alt: solid; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 488.45pt; border: solid silver 1.0pt; border-left: none; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-top-alt: solid silver .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Task 1 – Identify the network layout</span>**

</td></tr><tr style="mso-yfti-irow: 1;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">The first step in troubleshooting an AP is to find out what the AP is connected to. This will allow us to possibly cycle the port the AP connects to which will in turn reboot the AP. This may work as long as the AP is connected to a device Cello manages and the AP is still physically connected to that device.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">There are multiple ways in which we can determine what an AP is connected to:</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">1.<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Via LogicMonitor</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">2.<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Via the As-Built</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">3.<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Logging into the CLI of on-site devices.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 2;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1 a)</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">LogicMonitor</span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Some APs such as Cisco APs will allow you to use CDP (Cisco Discovery Protocol) to discover a connected device.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">For example:</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-khlz4ods.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">From the picture we can see that PUBT-S027-AP01 is connected to PUBT-S027-SW01.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-lrzckd26.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">In this example, LogicMonitor even shows us what port the AP physically connects to – GigabitEthernet1/0/24</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 3;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1 b)</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">As-Built </span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">On most sites with APs the As-Built will provide some context on how the APs are connected to their LAN (local area network). </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">For example:</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-w45rpcat.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">From the picture we can see that PUBT-S027-AP01 connects to PUBT-S027-SW01. However, we cant see what port the AP physically connects to. You will either need to check LogicMonitor or log into the device and run the commands in Task 2, Step 2.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 4;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1 c)</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">CLI (Command line interface)</span>**

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Vendor Neutral device information gathering</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-be4laptj.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Cisco Specific device information gathering</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-degpeszk.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Show mac address-table will show the mac address of attached devices and the relevant physical port.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-nzqabz8o.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 5;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Gathering information about the WLC (If applicable.)</span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">This step is another good piece of information to gather. Sometimes tenants will have 2 WLC’s for the purposes of redundancy. Therefore, an AP can failover to another WLC, if there is a primary and secondary WLC.<span style="mso-tab-count: 1;"> </span></span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">If the AP has failed over to the secondary WLC even though the AP is up, your alert/ticket may not clear. You can delete an instance of the AP in LogicMonitor in the primary to clear your ticket IF the AP is actually up. The following steps will assist:</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">NOC Process - How to r... | BookStack (cello.co.nz)</span>](https://bookstack.cello.co.nz/books/noc-info-logicmonitor/page/noc-process-how-to-remove-an-ap-instance-from-logicmonitor)</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">To see this, look on the As-Built and see if there is more than 1 WLC. If there is, you can URL via the MGMT domain into either to find the AP and which WLC it is associated with.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-ptuxlxba.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">For example:</span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Primary: https://pubt-s999-wlc01.cpe.mgmt.nz</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Secondary: https://pubt-s998-wlc01.cpe.mgmt.nz</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 6; mso-yfti-lastrow: yes;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">3</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">If you can’t find the above information</span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">There are times where CDP or LLDP may not be available and the connected device information as seen in LogicMonitor (step 1 a) may not work.</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">There are also As-builts which may lack detail around which switch or device the AP is connected to or the AP is connected to a device which is NOT managed by Cello.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">An example would be an ANZCO AP. The SOP can be found here:  
</span><span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">https://bookstack.cello.co.nz/books/anzco/page/noc-process-anzco-access-point-ap-troubleshooting-sop</span>](https://bookstack.cello.co.nz/books/anzco/page/noc-process-anzco-access-point-ap-troubleshooting-sop)</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-2-%E2%80%93-cycli" style="border-collapse: collapse; width: 718px; border-spacing: 0px; border: initial none initial;" width="718"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes; height: 18.15pt;"><td style="width: 50.35pt; border: solid silver 1.0pt; mso-border-top-alt: .5pt; mso-border-left-alt: .5pt; mso-border-bottom-alt: .75pt; mso-border-right-alt: .75pt; mso-border-color-alt: silver; mso-border-style-alt: solid; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 488.45pt; border: solid silver 1.0pt; border-left: none; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-top-alt: solid silver .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Task 2 – Cycling the AP port (rebooting the AP) \*\*IF APPLICABLE\*\*</span>**

</td></tr><tr style="mso-yfti-irow: 1;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Note</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: red; mso-fareast-language: EN-NZ;">This step is only applicable if:</span>**

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">You can locate the device the AP is connected to.</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">The AP is connected to a Cello managed device.</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">The AP is the **<u>only</u>** device connected to that physical port.</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Meraki, Aruba, Aerohive and FortiGate system process will differ to the one outlined below (visit Task 3).</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 2;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">In our example, we have discovered that the AP - PUBT-S027-AP01 connects to PUBT-S027-SW01, G1/0/24. We found this via LogicMonitor and the As-Built in Task 1.</span>

</td></tr><tr style="mso-yfti-irow: 3;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Shut the interface and bring it back up.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-t0hyzjmn.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-xek053yo.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Some useful commands are:</span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Show ip interface brief – This will show port status</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Show interface description – This will describe what’s on each port (Don’t always trust this)</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Show cdp neighbours – used to discover devices on cisco</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Show lldp neighbours – same but vendor neutral</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Further commands found here:</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">NOC Info - Commands | BookStack (cello.co.nz)</span>](https://bookstack.cello.co.nz/books/noc-info-commands)</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 4; mso-yfti-lastrow: yes;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">3</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-3-%E2%80%93-reboo" style="border-collapse: collapse; width: 718px; border-spacing: 0px; border: initial none initial;" width="718"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes; height: 18.15pt;"><td style="width: 50.35pt; border: solid silver 1.0pt; mso-border-top-alt: .5pt; mso-border-left-alt: .5pt; mso-border-bottom-alt: .75pt; mso-border-right-alt: .75pt; mso-border-color-alt: silver; mso-border-style-alt: solid; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 488.45pt; border: solid silver 1.0pt; border-left: none; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-top-alt: solid silver .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Task 3 – Rebooting on non CLI systems</span>**

</td></tr><tr style="mso-yfti-irow: 1;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">0</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">The following systems are similar but utilise a GUI rather than a CLI:</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Aruba</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Meraki</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Aerohive</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">FortiGate</span>

</td></tr><tr style="mso-yfti-irow: 2;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Aerohive (The Warehouse)</span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">To troubleshoot an AP used at The Warehouse Group, please use the following SOP:</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">https://bookstack.cello.co.nz/books/the-warehouse-group/page/noc-process-rebooting-an-ap-via-aerohive</span>](https://bookstack.cello.co.nz/books/the-warehouse-group/page/noc-process-rebooting-an-ap-via-aerohive)</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 3;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Meraki</span>**

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Example ticket: </span>**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Meraki Network: Mega Papanui - Access Points-</span><span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">PPIAP19  
  
</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Log into Meraki</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">On the left side of the screen select the Organisation you require e.g. Mitre 10</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Again on the left side of the screen, under ‘Network’ select the site you are after e.g. ‘Mega Papanui’.</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Wireless &gt; Access Points</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-xtsfde5t.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Find the AP you are after and click on it e.g. PPIAAP19</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-opsm2qpr.png)  
</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Scroll down on the left side and look for the following:</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-k7ssaxqk.png)  
</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">From this information found in the AP summary page, we can see that this AP connects to switch: PPISW04-2 and is physically connected to Port 1.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Click on the name of the switch e.g. PPISQW04-2</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Once on the switches summary page, click on the required port. In our example, this is Port 1.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-a3ceqhg9.png)  
</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Disable and re-enable the port. This will cause the AP to lose power and reboot.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-jdevb0vw.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Note: </span>**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Give the AP around 5-10mins to reboot and establish with Meraki.</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

</td></tr><tr style="mso-yfti-irow: 4;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">4</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Aruba</span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Login to Aruba Central and Launch.</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Select the relevant site. In this example, we are going to use EAL.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-pcpgv5qd.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Global &gt; wireless</span>

<span style="mso-ignore: vglayout; position: absolute; z-index: 251660288; margin-left: 6px; margin-top: 151px; width: 48px; height: 11px;">![](file:///C:/Users/CODEY~1.WIL/AppData/Local/Temp/msohtmlclip1/01/clip_image033.png)</span><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-vlwfczfh.png)  
</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Click on ‘Devices’ on the left, click on the relevant AP that has gone down.</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-7mz8bexd.png)  
</span>**

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Once inside the AP look on the right hand side and look for ‘UPLINK CONNECTED TO’. This indicates us what the AP is physically connected to.</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-w41plmjg.png)  
</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Scroll down the page to DATA PATH and hover the mouse of the switch. We can see it’s on Port 1/1/10.</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-9qsgcy5q.png)  
</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">You can now click on the switch as mentioned above under ‘UPLINK CONNECTED TO’.</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Go to ‘Device’ &gt; Ports &amp; Link Aggregation</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-ccroi5qv.png)  
</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Go to the pencil on the relevant port</span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-ehl8yzlm.png)  
</span>**

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"><span style="text-decoration: underline;">Logically resetting the port</span> </span>**

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Unclick ‘Admin Up’ wait 5-10 seconds and again click ‘Admin Up’</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-gkzbwkp9.png)  
</span>

<span style="text-decoration: underline;">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Bouncing PoE</span>**</span>

Make sure the switch you want to bounce PoE is selected. Next head to the 'Tools' option on the left menu bar.

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-09/scaled-1680-/lJaimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-09/lJaimage.png)

 Select 'Device Check' from the top menu bar. Ensure the switch you want is selected. Under 'Test', choose 'PoE Bounce'. Next choose the port you want to bounce PoE on. Double check everything is correct then press 'Run'. This will cause PoE to turn off and then turn back on.

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-09/scaled-1680-/J6Kimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-09/J6Kimage.png)

<p class="callout danger">Please be aware that sometimes an AP can show as down on our monitoring systems, including Aruba Central. Please make sure you are logging into the switch it is attached to. The switch should be picking up its L2 MAC address and L3 IP addressing.</p>

</td></tr><tr style="mso-yfti-irow: 5;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">5</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">FortiGate</span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">The APs directly connected to a FortiGate Firewall, will either be FortiGate APs or APs by another provider.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Log into the Firewall directly</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Navigate to Network &gt; Interfaces</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Identify which port the AP is connected to on the FW. This can be seen in the FW or the As-Built.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">In this example, we can see that Internal 1, is delivering POE to an AP. It is the port listed in blue.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-1non9rqf.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">To cycle the port, double click on ‘Internal’ In the ‘Hardware Switch’ section.</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Scroll down to the bottom and look for ‘Enable Power over Ethernet (PoE)</span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Click on ‘Specific Ports’</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-tchcardr.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">‘X’ off the port you want to disable POE on. For example, Internal 1.</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-nohhcwy7.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">-<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Once you have done this, change the option back to ‘All’ and this will enable POE back on all the ports.</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2023-08/embedded-image-kdldzufz.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: red; mso-fareast-language: EN-NZ;">Warning: Make sure you switch this back to ‘All’</span>**

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 6; mso-yfti-lastrow: yes;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-4-%E2%80%93-failu" style="border-collapse: collapse; width: 720px; border-spacing: 0px; border: initial none initial;" width="720"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes; height: 23.55pt;"><td style="width: 51.55pt; border: solid silver 1.0pt; mso-border-top-alt: .5pt; mso-border-left-alt: .5pt; mso-border-bottom-alt: .75pt; mso-border-right-alt: .75pt; mso-border-color-alt: silver; mso-border-style-alt: solid; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 23.55pt;" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 488.45pt; border: solid silver 1.0pt; border-left: none; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-top-alt: solid silver .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 23.55pt;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Task 4 – Failure to bring the AP back online</span>**

</td></tr><tr style="mso-yfti-irow: 1; mso-yfti-lastrow: yes;"><td style="width: 51.55pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">If you are unable to do the steps above and remedy the AP or the AP is connected to a non-Cello managed device. Contact the client using a modified version of the FLC process.</span>

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-end-of-sop-sop-docum" style="border-collapse: collapse; width: 538.4pt; border-spacing: 0px; border: initial none initial;" width="718"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes; height: 17.45pt;"><td colspan="5" style="width: 538.4pt; border: solid windowtext 1.0pt; mso-border-alt: solid windowtext .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="718">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">End Of SOP</span>**

</td></tr><tr style="mso-yfti-irow: 1; height: 17.45pt;"><td colspan="5" style="width: 538.4pt; border: solid windowtext 1.0pt; border-top: none; mso-border-top-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="718">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">SOP Document Version Control</span>**

</td></tr><tr style="mso-yfti-irow: 2; height: 17.45pt;"><td style="width: 63.55pt; border: solid windowtext 1.0pt; border-top: none; mso-border-top-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="85">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Version No:</span>**

</td><td style="width: 77.95pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="104">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Effective Date</span>**

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Author</span>**

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Approver</span>**

</td><td style="width: 178.0pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="237">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Brief Description of Change (referring Tack and Step)</span>**

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;"> </span>**

</td></tr><tr style="mso-yfti-irow: 3; height: 17.45pt;"><td style="width: 63.55pt; border: solid windowtext 1.0pt; border-top: none; mso-border-top-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1.0</span>

</td><td style="width: 77.95pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">25 August 2023</span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">C Wildman</span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> S.Henderson</span>

</td><td style="width: 178.0pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Creation artefact</span>

</td></tr><tr style="mso-yfti-irow: 4; mso-yfti-lastrow: yes; height: 17.45pt;"><td style="width: 63.55pt; border: solid windowtext 1.0pt; border-top: none; mso-border-top-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 77.95pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 178.0pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr></tbody></table>

**<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; color: white; mso-themecolor: background1;"></span>**