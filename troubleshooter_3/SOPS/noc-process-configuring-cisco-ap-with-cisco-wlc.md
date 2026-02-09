# NOC PROCESS - Configuring Cisco AP with Cisco WLC

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

**<span style="font-size: 9.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; mso-no-proof: yes;">NOC PROCESS – Cisco WLC AP configuration</span>**

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-purpose-during-a-sit" style="border-collapse: collapse; width: 720px; height: 186.667px; border-spacing: 0px; border: initial none initial;" width="720"><tbody><tr style="height: 28px;"><td style="width: 65.7pt; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 28px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Purpose</span>**

</td><td style="width: 474.3pt; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; padding: 0cm 5.4pt; height: 28px;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">During a site install, when the site has a Cisco AP that needs to connect to a Cisco WLC.</span>

</td></tr><tr style="height: 28px;"><td style="width: 65.7pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 28px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Scope</span>**

</td><td style="width: 474.3pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 28px;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">NOC install process</span>

</td></tr><tr style="height: 46.6667px;"><td style="width: 65.7pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 46.6667px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Business Rules</span>**

</td><td style="width: 474.3pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 46.6667px;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; background: yellow; mso-highlight: yellow; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;">Process during an install when an AP needs configuration with Cisco WLC.</span>

</td></tr><tr style="height: 28px;"><td style="width: 65.7pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 28px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Inputs</span>**

</td><td style="width: 474.3pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 28px;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;"> </span>

</td></tr><tr style="height: 28px;"><td style="width: 65.7pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 28px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Outputs</span>**

</td><td style="width: 474.3pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 28px;" valign="top" width="632"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: #7f7f7f; mso-themecolor: text1; mso-themetint: 128; mso-fareast-language: EN-NZ; mso-bidi-font-weight: bold;"> </span>

</td></tr><tr style="height: 28px;"><td style="width: 65.7pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 28px;" valign="top" width="88">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Notes</span>**

</td><td style="width: 474.3pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 28px;" valign="top" width="632">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: Calibri; mso-bidi-theme-font: minor-latin; color: black; mso-themecolor: text1; mso-fareast-language: EN-NZ;"> </span>**

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

**<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;">PROCESS FLOW CHART</span>**

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-1-%E2%80%93-findi" style="border-collapse: collapse; width: 718px; border-spacing: 0px; border: initial none initial;" width="718"><tbody><tr style="mso-yfti-irow: 0; mso-yfti-firstrow: yes; height: 18.15pt;"><td style="width: 50.35pt; border: solid silver 1.0pt; mso-border-top-alt: .5pt; mso-border-left-alt: .5pt; mso-border-bottom-alt: .75pt; mso-border-right-alt: .75pt; mso-border-color-alt: silver; mso-border-style-alt: solid; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 488.45pt; border: solid silver 1.0pt; border-left: none; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-top-alt: solid silver .5pt; background: #3E4B58; padding: 0cm 5.4pt 0cm 5.4pt; height: 18.15pt;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Task 1 – Finding the WLC/s</span>**

</td></tr><tr style="mso-yfti-irow: 1;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">In this example, we are using Parli-s007. After visiting the sites as-built, we can see that they have two WLCs. 999 and 998. This was found by using the search function CTRL+F and searching the keyword ‘WLC’.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/embedded-image-0bicsxh4.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/embedded-image-qyivguwa.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Note:</span>**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> APs with an even number in their name, for example, s008, will be added to 998, and s007 will be added to 999 for the purpose of load balancing.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 2;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">The URL for the WLCs will be in the following syntax:</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">https://&lt;name of WLC here&gt;.cpe.mgmt.nz</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">For example:</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">https://parli-s999-wlc01.cpe.mgmt.nz</span>](https://parli-s999-wlc01.cpe.mgmt.nz)</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">and</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

<span style="font-size: 10.0pt; font-family: 'Times New Roman',serif; mso-fareast-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">[<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">https://parli-s998-wlc01.cpe.mgmt.nz</span>](https://parli-s998-wlc01.cpe.mgmt.nz)</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 3; mso-yfti-lastrow: yes;"><td style="width: 50.35pt; border: solid silver 1.0pt; border-top: none; mso-border-top-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; mso-border-left-alt: solid silver .5pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="67">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">3</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: solid silver 1.0pt; border-right: solid silver 1.0pt; mso-border-top-alt: solid silver .75pt; mso-border-left-alt: solid silver .75pt; mso-border-alt: solid silver .75pt; padding: 0cm 5.4pt 0cm 5.4pt;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

<table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-steps-task-2-%E2%80%93-disco" style="border-collapse: collapse; width: 720px; border-spacing: 0px; height: 2634.48px;" width="720"><tbody><tr style="height: 31.3958px;"><td style="width: 51.55pt; border: 1pt solid silver; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 31.3958px;" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-fareast-language: EN-NZ;">Steps</span>**

</td><td style="width: 488.45pt; border-top: 1pt solid silver; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-image: initial; border-left: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 31.3958px;" width="651">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Task 2 – Discovering the AP in the WLC</span>**

</td></tr><tr style="height: 389.208px;"><td style="width: 51.55pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 389.208px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 389.208px;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">In your MGMT domain jump host, visit the URL of the relevant WLC.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

<span style="mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/embedded-image-axhicvzc.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

</td></tr><tr style="height: 483.646px;"><td style="width: 51.55pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 483.646px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">2</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 483.646px;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">On the left menu, select ‘Configuration’ and then ‘Wireless’ &gt; ‘Access Points’</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-no-proof: yes;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/embedded-image-zcacazbz.png)  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

</td></tr><tr style="height: 527.438px;"><td style="width: 51.55pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 527.438px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">3</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 527.438px;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">Select the heading ‘Ethernet Mac’ &gt; ‘Filter’ and then enter in the MAC address of the relevant AP.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">![](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/embedded-image-kdqms3le.png)</span><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-no-proof: yes;"></span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">Note:</span>**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> Be mindful that the format of the MAC address on Netbox may differ from that in the WLC. For example 5C-71-0D-E5-FA-F8 needs to change to 5C71.0DE5.FAF8</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

</td></tr><tr style="height: 1146.79px;"><td style="width: 51.55pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 1146.79px;" valign="top" width="69">**<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">4</span>**

</td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 1146.79px;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">Once the AP has been located, it needs a few changes made to its configuration.</span>

<span style="font-size: 8.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;"><span style="mso-list: Ignore;">·<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">AP name will need to be changed from the MAC addresss to the name on Netbox</span>

<span style="font-size: 8.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;"><span style="mso-list: Ignore;">·<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">AP mode: Flex</span>

<span style="font-size: 8.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;"><span style="mso-list: Ignore;">·<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">Policy and site needs to match the site name of the device.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; color: red;">Sometimes site and polciy might be missing talk to senior noc then LAN to get added. </span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

<span style="mso-ignore: vglayout; position: absolute; z-index: 251664384; margin-left: -10px; margin-top: 1px; width: 63px; height: 58px;">  
</span><span style="mso-ignore: vglayout; position: absolute; z-index: 251663360; margin-left: 88px; margin-top: 175px; width: 129px; height: 58px;">![](file:///C:/Users/CODEY~1.WIL/AppData/Local/Temp/msohtmlclip1/01/clip_image014.png)</span><span style="mso-ignore: vglayout; position: absolute; z-index: 251662336; margin-left: 332px; margin-top: 82px; width: 123px; height: 57px;">  
</span><span style="mso-ignore: vglayout; position: absolute; z-index: 251661312; margin-left: 329px; margin-top: 56px; width: 115px; height: 59px;">  
</span><span style="mso-ignore: vglayout; position: absolute; z-index: 251660288; margin-left: 99px; margin-top: 53px; width: 114px; height: 61px;">  
</span>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/scaled-1680-/7f3image.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/7f3image.png)

<span style="mso-no-proof: yes;">  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/scaled-1680-/XtPimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-01/XtPimage.png)

<span style="mso-ignore: vglayout; position: absolute; z-index: 251669504; margin-left: 233px; margin-top: 55px; width: 89px; height: 57px;">  
</span><span style="mso-ignore: vglayout; position: absolute; z-index: 251668480; margin-left: 231px; margin-top: 78px; width: 97px; height: 58px;">![](file:///C:/Users/CODEY~1.WIL/AppData/Local/Temp/msohtmlclip1/01/clip_image020.png)</span><span style="mso-ignore: vglayout; position: absolute; z-index: 251667456; margin-left: 76px; margin-top: 80px; width: 123px; height: 59px;">  
</span><span style="mso-ignore: vglayout; position: absolute; z-index: 251666432; margin-left: 81px; margin-top: 54px; width: 126px; height: 58px;">  
</span><span style="mso-no-proof: yes;">  
</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

<span style="font-size: 8.0pt; font-family: Symbol; mso-fareast-font-family: Symbol; mso-bidi-font-family: Symbol;"><span style="mso-list: Ignore;">·<span style="font: 7.0pt 'Times New Roman';"> </span></span></span><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;">Ensuring the primary controller is correct – For example: 999WLC for odd numbered sites and 998 for even numbered sites.</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

</td></tr><tr style="height: 28px;"><td style="width: 51.55pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 28px;" valign="top" width="69"></td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 28px;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

</td></tr><tr style="height: 28px;"><td style="width: 51.55pt; border-right: 1pt solid silver; border-bottom: 1pt solid silver; border-left: 1pt solid silver; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 28px;" valign="top" width="69"></td><td style="width: 488.45pt; border-top: none; border-left: none; border-bottom: 1pt solid silver; border-right: 1pt solid silver; padding: 0cm 5.4pt; height: 28px;" valign="top" width="651"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif;"> </span>

</td></tr></tbody></table>

<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif;"> </span>

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

</td><td style="width: 77.95pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">23/01/2024</span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">C.Wildman</span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">G.Millar </span>

</td><td style="width: 178.0pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">Creation artefact</span>

</td></tr><tr style="mso-yfti-irow: 4; height: 17.45pt;"><td style="width: 63.55pt; border: solid windowtext 1.0pt; border-top: none; mso-border-top-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 77.95pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 178.0pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="mso-yfti-irow: 5; mso-yfti-lastrow: yes; height: 17.45pt;"><td style="width: 63.55pt; border: solid windowtext 1.0pt; border-top: none; mso-border-top-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 77.95pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 109.45pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td><td style="width: 178.0pt; border-top: none; border-left: none; border-bottom: solid windowtext 1.0pt; border-right: solid windowtext 1.0pt; mso-border-top-alt: solid windowtext .5pt; mso-border-left-alt: solid windowtext .5pt; mso-border-alt: solid windowtext .5pt; padding: 0cm 5.4pt 0cm 5.4pt; height: 17.45pt;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;"> </span>

</td></tr></tbody></table>

**<span style="font-size: 8.0pt; line-height: 115%; font-family: 'Verdana',sans-serif; color: white; mso-themecolor: background1;"></span>**