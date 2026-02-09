# NOC PROCESS - Firewall INSTALL

<span class="align-left" style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

**<span style="font-size: 9.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;">NOC PROCESS – Install FortiGate Firewall</span>**

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-right" id="bkmrk-purpose-verify-forti" style="margin-left: -44pt; border-collapse: collapse; border: none; width: 721px; border-spacing: 0px;" width="720"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes;"><td style="width: 87.5938px; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Purpose</span>**

</td><td style="width: 632.396px; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; padding: 0cm 5.4pt;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">Verify FortiGate Firewall functioning as required during install</span>

</td></tr><tr style="mso-yfti-irow: 1;"><td style="width: 87.5938px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Scope</span>**

</td><td style="width: 632.396px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">NOC, NEC Technician FortiGate Firewall, FEX</span>

</td></tr><tr style="mso-yfti-irow: 2;"><td style="width: 87.5938px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Business Rules</span>**

</td><td style="width: 632.396px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; background: yellow; mso-highlight: yellow; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">Applies to NOC when there is an installation of a FortiGate Firewall</span>

</td></tr><tr style="mso-yfti-irow: 3;"><td style="width: 87.5938px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Inputs</span>**

</td><td style="width: 632.396px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">Preparation steps before install – Run the Install/Cutover scenario procedure on the provisioning ticket, connect to the management VPN, log into the RDP.</span>

</td></tr><tr style="mso-yfti-irow: 4;"><td style="width: 87.5938px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Outputs</span>**

</td><td style="width: 632.396px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">Fully functioning Firewall and peripherals as expected by client.</span>

</td></tr><tr style="mso-yfti-irow: 5; mso-yfti-lastrow: yes;"><td style="width: 87.5938px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Notes</span>**

</td><td style="width: 632.396px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt;" valign="top" width="632">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: black; mso-themecolor: text1; mso-fareast-language: EN-NZ;">Troubleshooting steps may be required. Open As Built of site</span>**

</td></tr></tbody></table>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-right" id="bkmrk-steps-task-1-%E2%80%93-basic" style="margin-left: -44pt; border-collapse: collapse; border: none; width: 720px; border-spacing: 0px; height: 3679.26px;" width="720"><tbody><tr style="height: 31.3778px;"><td style="width: 68.7216px; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 31.3778px;" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 651.25px; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 31.3778px;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Task 1 –<span style="mso-bidi-font-weight: bold;"> Basic checks and push configuration to APs and Firewall</span></span>**

</td></tr><tr><td style="width: 68.7216px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt;">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">\#</span>**

</td><td style="width: 651.25px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt;">Plug the device in as per the AS-Build in K:/ drive and NetBox, ONT port number can be found on the sites circuit page.

</td></tr><tr style="height: 249.957px;"><td style="width: 68.7216px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 249.957px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 651.25px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 249.957px;" width="651"><span style="text-decoration: underline;">**Verify Connectivity**</span>

**<u><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Ping the device</span></u>**

![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-rftulo8k.png)

**<u><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">LogicMonitor</span></u>**

![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-eyqfmf15.png)

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">  
</span>

<span class="align-left" style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="height: 838.508px;"><td style="width: 68.7216px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 838.508px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 651.25px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 838.508px;" width="651">**<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Verify 4G access</span>**

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">If the device has 4G backup or 4G primary, can you access it via 4G?</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-szm1xzrr.png)  
</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-l4zi1dik.png)  
</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Or</span><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Login to </span><span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[<span style="font-family: 'Verdana',sans-serif;">https://spark.jasperwireless.com/</span>](https://spark.jasperwireless.com/)</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-79gtwukd.png)  
</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-3ub1sugh.png)  
</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Looking for Network Connection = Passed.</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-uaxrrguk.png)  
</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="height: 595.17px;"><td style="width: 68.7216px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 595.17px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">3</span>**

</td><td style="width: 651.25px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 595.17px;" width="651">**<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Check 4G reception levels</span>**

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Get extender modem-status (FEX serial number)</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-7gnpwzwl.png)  
</span>

<p class="callout info"><span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">Signal should be Good or above. If 4G signal is not up to standard, see if the FEX can be installed in a more favourable location and connected to the FW via patch panel. If there is no way to improve the signal, please refer the issue back to solutions.</span></p>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-knjecbnl.png)</span><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="height: 206.307px;"><td style="width: 68.7216px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 206.307px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">4</span>**

</td><td style="width: 651.25px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 206.307px;" width="651">**<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Verify BGP peering</span>**

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Get router info6 bgp summary</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-57rzzgwc.png)  
</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="height: 316.903px;"><td style="width: 68.7216px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 316.903px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">5</span>**

</td><td style="width: 651.25px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 316.903px;" width="651">**<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Verify FW exists in Forti Manager</span>**

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Log into Forti Manager via the MGMT RDP – Christchurch: </span><span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[<span style="font-family: 'Verdana',sans-serif;">https://m-chc01-fmg01/p/login/</span>](https://m-chc01-fmg01/p/login/)</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-bvufcbtq.png)  
</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="height: 340.327px;"><td style="width: 68.7216px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 340.327px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">6</span>**

</td><td style="width: 651.25px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 340.327px;" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Select &lt;relevant VDOM&gt; </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span><span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;"></span>![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-fgrhzbat.png)

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="height: 881.065px;"><td style="width: 68.7216px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 881.065px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">7</span>**

</td><td style="width: 651.25px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 881.065px;" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Select Device Manager</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span><span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;"></span>![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-xhrfk9u0.png)<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-zzzagwng.png)  
</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

**If the device is up but showing as down in Forti Manager:**

Log into the firewall (CLI) and enter the following:

config system central-management

 set type fortimanager

 set fmg "2406:2b00:10:100::15"

 set fmg-source-ip6 &lt;loopback\_v6&gt;

end

(Loopbacks can be found in netbox, AS-Builts, DNS and on the device)

**Similar for Forti Analyzer:**

Log into the firewall (CLI) and enter the following:

config log fortianalyzer setting  
 set status enable  
 set server "2406:2b00:10:100::16"  
 set source-ip "$(loopback0\_ipv6)"  
 set upload-option realtime  
 set reliable enable  
end

</td></tr><tr style="height: 191.662px;"><td style="width: 68.7216px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 191.662px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">8 </span>**

</td><td style="width: 651.25px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 191.662px;" width="651">**<u><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Check policy package:</span></u>**

**<u><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"><span style="text-decoration: none;"> </span></span></u>**<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;"></span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Once firewall is online and you have applied the central management config, log into FMG, and Sync the firewall:</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[https://bookstack.cello.co.nz/books/accessing-and-maintaining-devices/page/noc-process-syncing-firewall-in-fortimanager](https://bookstack.cello.co.nz/books/noc-info-fortinet-accessing-and-managing-fortinet-equipment/page/noc-process-syncing-firewall-in-fortimanager)</span>

</td></tr><tr style="height: 27.983px;"><td style="width: 68.7216px; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 27.983px;">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">9</span>**

</td><td style="width: 651.25px; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 27.983px;">Ensure FMG-Access in unticked on WAN1 interface.

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-05/scaled-1680-/We1image.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-05/We1image.png)

**<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">  
</span>**

</td></tr></tbody></table>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-right" id="bkmrk-steps-optional-task%C2%A0" style="margin-left: -42.8pt; border-collapse: collapse; border: none; width: 718px; border-spacing: 0px;" width="718"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes; height: 18.15pt;"><td style="width: 50.35pt; border: solid silver 1.0pt; mso-border-top-alt: .5pt; mso-border-left-alt: .5pt; mso-border-bottom-alt: .75pt; mso-border-right-alt: .75pt; mso-border-color-alt: silver; mso-border-style-alt: solid; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 488.45pt; border: solid silver 1.0pt; border-left: none; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-top-alt: solid silver .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Optional Task<span style="mso-spacerun: yes;"> </span>– Forti APs</span>**

</td></tr><tr style="mso-yfti-irow: 1;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Go to AP MANAGER</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-yifktlez.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 2;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Confirm Aps are connected</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-eoszaofx.png)  
</span>

**<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

</td></tr><tr style="mso-yfti-irow: 3;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">4</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Rename each of the APs if not already:</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Double click on an AP:</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-wyaubwaw.png)  
</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span lang="EN-AU" style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">1.<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Copy the serial number into Netbox</span>

<span lang="EN-AU" style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: Verdana; mso-bidi-font-family: Verdana; mso-fareast-language: EN-NZ;"><span style="mso-list: Ignore;">2.<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span lang="EN-AU" style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-language: EN-NZ;">Copy name from netbox e.g. ELECT-S055-AP03 into the name text box above.</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 4;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">5</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Scroll down to FortiAP Profile:</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-yguajkqq.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Select the relevant profile. Please speak with relevant engineer if unsure.</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Confirm and Save.</span>

</td></tr><tr style="mso-yfti-irow: 5;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">6</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 6; mso-yfti-lastrow: yes;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr></tbody></table>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-right" id="bkmrk-steps-optional-task%C2%A0-1" style="margin-left: -42.8pt; border-collapse: collapse; border: none; width: 718px; border-spacing: 0px;" width="718"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes; height: 18.15pt;"><td style="width: 50.35pt; border: solid silver 1.0pt; mso-border-top-alt: .5pt; mso-border-left-alt: .5pt; mso-border-bottom-alt: .75pt; mso-border-right-alt: .75pt; mso-border-color-alt: silver; mso-border-style-alt: solid; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 488.45pt; border: solid silver 1.0pt; border-left: none; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-top-alt: solid silver .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Optional Task<span style="mso-spacerun: yes;"> </span>– No Policy Package </span>**

</td></tr><tr style="mso-yfti-irow: 1;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Ensure you are in Device Manager</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-oopjphjm.png)  
</span>

</td></tr><tr style="mso-yfti-irow: 2;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Select ‘Install Wizard’ on the top blue bar. Lock if this is not visible.</span>

**<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-iahwhgeb.png)  
</span>

</td></tr><tr style="mso-yfti-irow: 3;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">4</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Select the correct ‘Policy Package’ in the drop down menu. If unsure, ask relevant engineer.</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">In the comment section, place the ticket number and press next.</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-rn6bsrnc.png)  
</span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 4;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">5</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Un-check all of the FW’s except the relevant FW you are installing and click next.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-03/embedded-image-kisr6uk2.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Click Install and wait for it to process.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 5;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 6; mso-yfti-lastrow: yes;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr></tbody></table>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-right" id="bkmrk-steps-optional-task%C2%A0-2" style="margin-left: -42.8pt; border-collapse: collapse; border: none; width: 718px; border-spacing: 0px; height: 335.729px;" width="718"><tbody><tr style="height: 28px;"><td style="width: 50.35pt; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 28px;" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 488.45pt; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 28px;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Optional Task<span style="mso-spacerun: yes;"> </span>– Verify Software version</span>**

</td></tr><tr style="height: 145.062px;"><td style="width: 50.35pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 145.062px;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 145.062px;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Check current software version and compare to the golden image</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Golden image:</span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">https://bookstack.cello.co.nz/books/fortinet-guides/page/fortinet-golden-images</span>](https://bookstack.cello.co.nz/books/fortinet-guides/page/fortinet-golden-images)</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> Upgrading the FW</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[NOC PROCESS - Upgradin... | BookStack (cello.co.nz)](https://bookstack.cello.co.nz/books/noc-info-fortinet-accessing-and-managing-fortinet-equipment/page/noc-process-upgrading-a-firewall-from-fortimanager)</span>

</td></tr><tr style="height: 28px;"><td style="width: 50.35pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 28px;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 28px;" valign="top" width="651"><span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span><span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;"></span>

</td></tr></tbody></table>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-right" id="bkmrk-steps-optional-task%C2%A0-4" style="margin-left: -42.8pt; border-collapse: collapse; border: none; width: 718px; border-spacing: 0px;" width="718"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes; height: 18.15pt;"><td style="width: 50.35pt; border: solid silver 1.0pt; mso-border-top-alt: .5pt; mso-border-left-alt: .5pt; mso-border-bottom-alt: .75pt; mso-border-right-alt: .75pt; mso-border-color-alt: silver; mso-border-style-alt: solid; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 488.45pt; border: solid silver 1.0pt; border-left: none; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-top-alt: solid silver .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Optional Task<span style="mso-spacerun: yes;"> </span>– New customer – Importing a policy </span>**

</td></tr><tr style="mso-yfti-irow: 1;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">https://docs.fortinet.com/document/fortimanager/7.0.11/administration-guide/337348</span>

</td></tr><tr style="mso-yfti-irow: 2; mso-yfti-lastrow: yes;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651">**<span style="font-size: 10.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>**

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-right" id="bkmrk-end-of-sop-sop-docum" style="width: 538.4pt; margin-left: -42.5pt; border-collapse: collapse; border: none; border-spacing: 0px; height: 186.122px;" width="718"><tbody><tr style="height: 23.2528px;"><td colspan="5" style="width: 717.84px; border: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 23.2528px;" width="718">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">End Of SOP</span>**

</td></tr><tr style="height: 23.2528px;"><td colspan="5" style="width: 717.84px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 23.2528px;" width="718">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">SOP Document Version Control</span>**

</td></tr><tr style="height: 77.2727px;"><td style="width: 143.565px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77.2727px;" width="85">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Version No:</span>**

</td><td style="width: 143.565px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77.2727px;" width="104">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Effective Date</span>**

</td><td style="width: 143.565px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77.2727px;" width="146">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Author</span>**

</td><td style="width: 143.565px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77.2727px;" width="146">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Approver</span>**

</td><td style="width: 143.58px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77.2727px;" width="237">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Brief Description of Change (referring Tack and Step)</span>**

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;"> </span>**

</td></tr><tr style="height: 23.2528px;"><td style="width: 143.565px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 23.2528px;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1.0</span>

</td><td style="width: 143.565px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2528px;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">10 May 2023</span>

</td><td style="width: 143.565px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2528px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">C Wildman</span>

</td><td style="width: 143.565px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2528px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 143.58px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 23.2528px;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Creation artefact</span>

</td></tr><tr style="height: 39.0909px;"><td style="width: 143.565px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 39.0909px;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1.1</span>

</td><td style="width: 143.565px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 39.0909px;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">30 April 2025 </span>

</td><td style="width: 143.565px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 39.0909px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">A Sixtus </span>

</td><td style="width: 143.565px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 39.0909px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 143.58px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 39.0909px;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Add signal check reference </span>

</td></tr></tbody></table>

<span style="font-family: 'Verdana',sans-serif;"> </span>

**<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; color: #006666;">Note</span>**

**<span class="align-left" style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; color: white; mso-themecolor: background1;"></span>**