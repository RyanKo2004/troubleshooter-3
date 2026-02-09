# NOC PROCESS - TSA INSTALL

####  **IMPORTANT PLEASE READ**

<p class="callout danger"> If you face any issues during the install, please take a look through the **<span style="text-decoration: underline; color: rgb(35, 111, 161);">"*[Common Issues](https://bookstack.cello.co.nz/books/the-salvation-army-tsa/page/noc-process-common-issues-at-install)*"</span>** Bookstack article as it may be something that is already known and documented. </p>

<p class="callout danger">If, after 15 minutes the connection is not established to a LAN or WAN service we need to bring up as part of the install. Then, escalate to the rostered engineer for that field who is listed in the calendar appointment.</p>

<details id="bkmrk-preparation-preparat"><summary>Preparation</summary>

##### Preparation

1. Open Calendar Appointment for the install – familiarise yourself with the attached documents used during the install. Please add your personal email to the calendar appointment alongside the general NOC email so other teams can make direct contact if urgently needed.
2. Open the As-Built for the site. When in the As-Built Ctrl + F and paste in the relevant site E.g. TSA-S002.
3. Join the Teams meeting at the specified time. You will find this at the bottom of the calendar appointment.
4. Start a timer when in call to record total job time.
5. Open the documents attached in the calendar named – ‘TSA - xxx Implementation Plan.pdf’ and "TSA - Physical Connectivity"
6. Follow the instructions in the Implementation Plan starting with the UAT pre-cutover testing

</details><details id="bkmrk-firewall-as-part-of-"><summary>Firewall</summary>

As part of the install we will need to ensure the Central Management Config is added on to the Firewall:

Log into the firewall (CLI) and enter the following:

config system central-management

 set type fortimanager

 set fmg "2406:2b00:10:100::15"

 set fmg-source-ip6 &lt;loopback\_v6&gt;

end

Ensure that the firewall is correctly Synced (Policy package - TSA-BASE-POLICY):

Once firewall is currently online and you have applied the central management config, log into FMG, and Sync the firewall:

[https://bookstack.cello.co.nz/books/accessing-and-maintaining-devices/page/noc-process-syncing-firewall-in-fortimanager](https://bookstack.cello.co.nz/books/noc-info-fortinet-accessing-and-managing-fortinet-equipment/page/noc-process-syncing-firewall-in-fortimanager)

Ensure FMG-Access in unticked on WAN1 interface.

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-05/scaled-1680-/We1image.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-05/We1image.png)

If the APs are hitting the implicit deny and the FW polcies are not updating, try 'execute update-now'

Also check that the FW is in sync or not in FMG.

</details><details id="bkmrk-fex-once%2C-firewall-i"><summary>FEX</summary>

<span style="color: rgb(224, 62, 45);">***NOTE***</span>: *This section applies, **ONLY** if site has 4G backup.*

Once, firewall is confirmed plugged in. Confirm FEX is installed correctly as well - check as-built to confirm where which ports to plug it into but standards usually are:

- Fortigate 40F - Fex to port a
- Fortigate 60F - Fex to port 5

To check FortiExtender connectivity, log into the GUI of the Forti firewall onsite &gt; on the left-side menu, under Network dropdown &gt; go to *FortiExtenders* &gt; select Fex and check for following:

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-08/scaled-1680-/7Mqimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-08/7Mqimage.png)

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-08/scaled-1680-/nh8image.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-08/nh8image.png)

After all configurations have been done for the firewall and WAN connection verified working, can move on to connecting the switch(es) and APs. But <span style="text-decoration: underline;">*<span style="color: rgb(224, 62, 45); text-decoration: underline;">please come back to this part after the AP section.</span>*</span>

**<span style="color: rgb(224, 62, 45);">*NOTE*</span>**: Once, all APs and switch's connections have been established. Make sure to do the 4G failover as well. Unplugging the primary connection WAN1 on the FortiGate FW and check to see if connection fails to 4G. Have clients check for connection on all their SSIDs.

</details><details id="bkmrk-switches-the-switche"><summary>Switches</summary>

The switches will already be staged and will just need to come online once plugged in. For the switchport layout, take a look at the documentation in on Bookstack - [https://bookstack.cello.co.nz/books/the-salvation-army/page/high-level-overview#bkmrk-physical-switchport-](https://bookstack.cello.co.nz/books/the-salvation-army-tsa/page/high-level-overview#bkmrk-physical-switchport-).

If the site requires some additional switchport changes, the relevant config can be found under "NOC PROCESS - TSA Switchport Configurations" - [https://bookstack.cello.co.nz/books/the-salvation-army/page/noc-process-tsa-switchport-configurations](https://bookstack.cello.co.nz/books/the-salvation-army-tsa/page/noc-process-tsa-switchport-configurations)

##### Move the Switch to the correct site  


1. Go to: Global menu &gt; Sites &gt; little cog  
    [![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/scaled-1680-/Iszimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/Iszimage.png)
2. Select Unassigned &gt; drag the relevant switches over to the relevant site.  
    [![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/scaled-1680-/BYTimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/BYTimage.png)

</details><details id="bkmrk-access-points-connec"><summary>Access Points</summary>

Connect <span style="text-decoration: underline;">one</span> AP and wait for it to do a firmware upgrade and come back online in the "Wireless" group on Aruba Central. Once the AP is back online you can connect all the remaining APs. As long as they have a valid license and a working internet connection this should be pretty seamless. The APs will restart as they download a firmware update and pull down their configuration.

##### Step 1: Rename your APs

1. Rename your APs by matching the Serial Number to the names in Netbox.
2. Go to the Wireless Group and then on the left hand side select "Devices" then hit "Config" in the top-right  
    [![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/scaled-1680-/WFlimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/WFlimage.png)
3. Open the "Access Points" tab and rename all of your new APs.

##### Step 2: Configure your Virtual Controller

1. With the "Config" section still open, click "Show Advanced" on the top right corner then open the "System" tab
2. One AP from your site will be in the Virtual Controller table, hit the Pencil next to it and configure it following the addressing in the following spreadsheet - ***K:\\1A - Migrated\\The Salvation Army\\Engineering\\LAN IPs &amp; As-Built\\TSA Aruba Management Addressing.xlsx** -* in the sheet '***VC Addressing***'.  
    Name: TSA-sitecode-VC01  
    IP Address: "10.25x.yyy.201"   
    IPv6 Address: : "IPv6mgmt::c9"   
    Country Code: NZ
3. Look at the config of one of the other VCs for reference.
4. OK and Save

<p class="callout warning"><span style="color: rgb(224, 62, 45);">**NOTE: Please ask a LAN engineer if unsure.**</span></p>

##### <span style="color: rgb(224, 62, 45);"><span style="color: rgb(0, 0, 0);">Step 3: Move the APs to the correct site</span>  
</span>

1. <span style="color: rgb(224, 62, 45);"><span style="color: rgb(0, 0, 0);">Go to: Global menu &gt; Sites &gt; little cog  
    </span></span>[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/scaled-1680-/Iszimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/Iszimage.png)
2. Select Unassigned &gt; drag the relevant APs over to the relevant site.  
    [![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/scaled-1680-/BYTimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/BYTimage.png)
3. <span style="background-color: rgb(224, 62, 45);">Post Install add the Virtual Controller in the Netbox and Update the Tags. Below is a guide:</span> **https://bookstack.cello.co.nz/books/aruba-guides/page/provisioning-aruba-access-points#bkmrk-create-the-virtual-c**

</details><details id="bkmrk-printers-when-it-com"><summary>Printers</summary>

<p class="callout info">When it comes to cutting over the printers, they are essentially "Best Effort" from Cello's perspective. Once we get them on the Cello network and they are passing the "Communications Test", anything else such as a printing issue is beyond our scope and will have to go to TSA Digital Connect.   
  
If there are any issues with cutting over the printers such as the admin credentials not working or the printer not joining the network, note down the location and serial number and provide information to Cello Project Manager (Vikki) as Canon will need to send a technician to site post-cutover. Then proceed with the rest of the cutover. </p>

##### For sites that won’t have a switch on the Cello network: 

- For printers connected to the existing network via a wired connection, it will need to be switched over to WiFi. This must be done before you disconnect the old network.
- For printers connected to the existing network via wireless, it will need to be configured for the new Cello network <span style="text-decoration: underline;">**before you disconnect the old network**</span>.

##### For sites that will have a switch on the Cello network:   


- For printers connected to the existing network via a wired connection, it can be patched over to the new Cello network at any time.
- For printers connected to the existing network via wireless, they will need to be configured to the new Cello network **<span style="text-decoration: underline;">before you disconnect the old network</span>**.

##### Configuring a Wired Printer

1. Repatch to new Cello switch or FortiGate (dependant on site hardware).
2. Restart printer.
3. Comms test: 
    1. Touch panel "counter" \[123\] button in bottom RH corner of screen
    2. Monitoring Service.
    3. Communications test &gt; Start test &gt; Yes - wait for result;
    4. Communication was successful? 
        1. Yes? Close the screens (OK x3), then:
        2. Site contact to test printing.
        3. Site contact to test scan to email, record pass of those in UAT signoff.
        4. No? Power off printer (use the switch toggle on the printer) THEN power off the MAINS at the WALL outlet for 10s, then restore mains and then power back on with printer switch toggle. Retest Communications with above steps after bootup.
        5. Comms test still failed? Record error code provide to EU, ask them to seek help: 04 802 6262 (Digital Connect) if needed EU should escalate to Canon: 0800 222 666

##### Configuring a Wireless Printer

1. Open the Printer Settings (Cog icon) &gt; Device Settings &gt; Password: %%%%%%
2. Preferences &gt; Network &gt; Down to Page 5
3. Wireless LAN &gt; Wireless LAN Settings &gt; Other (set manually)
4. Select Access Point button and wait for it to scan
5. Choose "TSA-Trusted" and enter the password "largePOSTCARD7"
6. Once connected go back to main screen (Cancel &gt; Close &gt; Close)
7. Restart printer
8. Perform comms test as above under "Configuring a Wired Printer"
9. Have the user test printing/scanning.

</details><details id="bkmrk-eftpos-some-sites-su"><summary>EFTPOS</summary>

<p class="callout warning">Please ignore this part if site install is not a cutover/new machines - EFTPOS and Jigsaw should be on DHCP</p>

<p class="callout info">Some sites such as Family Stores (FS) will have EFTPOS machines but no JigSaw POS (Point of Sale). You can skip the POS steps for those sites. </p>

<p class="callout info">In the event of a problem before escalating please ensure the Eftpos section in the implemenation plan has been folowed before moving on to the below method.</p>

<p class="callout info">In the event of an issue with Eftpos ensure that the below method is followed to the letter. If this does not resolve the issue inform the tech or the site manager to escalate to Eftpos NZ. Cello is not required to reach out to them this is TSA's responsibility. </p>

<table border="1" style="border-collapse: collapse; width: 100%;"><colgroup><col style="width: 50.0642%;"></col><col style="width: 50.0642%;"></col></colgroup><tbody><tr><td class="align-center" style="background-color: rgb(52, 73, 94);">**<span style="color: rgb(255, 255, 255);">JigSaw POS</span>**</td><td class="align-center" style="background-color: rgb(52, 73, 94);">**<span style="color: rgb(255, 255, 255);">EFTPOS Machine</span>**</td></tr><tr><td class="align-center">[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/scaled-1680-/Ghfimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/Ghfimage.png)

</td><td class="align-center">[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/scaled-1680-/WhWimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-02/WhWimage.png)

</td></tr></tbody></table>

##### Configuring the JigSaw POS

NOTE: JigSaw only applies to Family Store sites.

1. Close the JigSaw application: Menu &gt; Support &gt; Close App
2. It's running Android so just navigate through the Settings and connect the tablet to "TSA-Trusted" SSID. 
    1. For IP options select DHCP if prompted.
    2. The password is in 1Password under "TSA - WiFi Passwords (PSKs)" then "IOT-Device PSK"
3. Open the Jigsaw application again and get the site to login

##### Configure the EFTPOS machines

1. Get the on-site tech to remove the old EFTPOS units and power up the new ones.
2. Join the new EFTPOS machines to the same TSA-Trusted network as above. They also run on Android so should be easy to navigate 
    1. Do <span style="text-decoration: underline; color: rgb(224, 62, 45);">**not**</span> use DHCP, configure a static address under advanced settings
    2. IP Address: See below table
    3. Subnet Mask/Prefix: 255.255.255.0 or /24
    4. Gateway: 10.200.102.1
    5. DNS: 10.200.102.1
    6. Secondary DNS: 8.8.8.8  
         **EFTPOS IP addresses**<table border="1" style="outline-color: var(--color-primary); font-style: normal; font-variant-ligatures: normal; font-variant-caps: normal; font-weight: 400; font-size: 14px; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Oxygen, Ubuntu, Roboto, Cantarell, 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif; height: 153.984px; width: 249px;"><colgroup style="outline-color: var(--color-primary);"><col style="outline-color: var(--color-primary); width: 105.328px;"></col><col style="outline-color: var(--color-primary); width: 142.672px;"></col></colgroup><tbody style="outline-color: var(--color-primary);"><tr style="outline-color: var(--color-primary); height: 29.7969px;"><td style="outline-color: var(--color-primary); height: 29.7969px;">EFTPOS 1</td><td style="outline-color: var(--color-primary); height: 29.7969px;">10.200.102.11</td></tr><tr style="outline-color: var(--color-primary); height: 29.7969px;"><td style="outline-color: var(--color-primary); height: 29.7969px;">EFTPOS 2</td><td style="outline-color: var(--color-primary); height: 29.7969px;">10.200.102.12</td></tr><tr style="outline-color: var(--color-primary); height: 29.7969px;"><td style="outline-color: var(--color-primary); height: 29.7969px;">EFTPOS 3</td><td style="outline-color: var(--color-primary); height: 29.7969px;">10.200.102.13</td></tr><tr style="outline-color: var(--color-primary); height: 34.7969px;"><td style="outline-color: var(--color-primary); height: 34.7969px;">EFTPOS 4</td><td style="outline-color: var(--color-primary); height: 34.7969px;">10.200.102.14</td></tr><tr style="outline-color: var(--color-primary); height: 29.7969px;"><td class="align-center" colspan="2" style="outline-color: var(--color-primary); height: 29.7969px;">and so on..  
          
        </td></tr></tbody></table>

##### Verify EFTPOS Comms

To be completed by a Family Store Manager

1. On the EFTPOS unit: Swipe down &gt; Diagnostics &gt; Merchant Information
2. Note down the Terminal ID

##### Test Integration with JigSaw POS

To be completed by a Family Store Manager

1. They can find the details on the POS under Settings &gt; EFTPOS

<p class="callout info">If it's not working, have the Family Store manager contact JigSaw - the JigSaw representative may need to update the POS to point towards our new EFTPOS IP addresses, provide these to the site manager in-case.   
  
**Support contacts in order:**   
Paris at THQ: 0800 4COLLECT  
Gareth Marshall: 027 511 0349  
Cory at Jigsaw: TBC  
TSA Digital Connect Service Desk: 04 802 6262  
Bryan Adams: 027 513 5155  
</p>

</details><details id="bkmrk-mitel-phones-some-si"><summary>Mitel Phones</summary>

Note: <span class="ui-provider a b c d e f g h i j k l m n o p q r s t u v w x y z ab ac ae af ag ah ai aj ak" dir="ltr">They should be on mobile phone solution by now however if there is an analogue phone still needed it will need to remain connected to the One.nz Ultrahub. Re the One.nz Ultrahub, if there is nothing else connected to it, eg security or CCTV system, and the Store doesn't have analogue phones then it will need to be decom'd please.</span>  
  
  
For sites with Mitel phone, you'll need to turn off SIP ALG on the firewall.

How to turn off SIP ALG on a FortiGate firewall

1\. Logon to your FortiGate’s console  
2\. Type ‘config system session-helper’ and press enter  
3\. Type ‘show’  
4\. Find the entry which shows ‘set name sip’ and note the ID (it’s usually 13)  
5\. Type ‘delete 13’ (or the number shown on your firewall) and then ‘end’  
6\. Type ‘config system settings’  
7\. Type ‘set default-voip-alg-mode kernel-helper-based’ and then ‘end’  
8\. Type ‘config voip profile’ then ‘edit default’  
9\. Type ‘config sip’ then ‘set status disable’  
10\. Type ‘end’ then ‘end’  
11\. Clear the session from FortiView Sessions and test.

[![Screenshot 2024-04-15 155319.png](https://bookstack.cello.co.nz/uploads/images/gallery/2024-04/scaled-1680-/screenshot-2024-04-15-155319.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2024-04/screenshot-2024-04-15-155319.png)

</details><table border="1" cellpadding="0" cellspacing="0" class="MsoTableGrid align-center" id="bkmrk-end-of-sop-sop-docum" style="border-collapse: collapse; width: 757px; border-spacing: 0px; height: 553.91px;" width="718"><tbody><tr style="height: 23.25px;"><td colspan="5" style="width: 736.854px; border: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 23.25px;" width="718"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">End Of SOP</span>

</td></tr><tr style="height: 23.25px;"><td colspan="5" style="width: 736.854px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 23.25px;" width="718"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">SOP Document Version Control</span>

</td></tr><tr style="height: 77px;"><td style="width: 147.365px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77px;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Version No:</span>

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77px;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Effective Date</span>

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Author</span>

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Approver</span>

</td><td style="width: 147.394px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; background: rgb(62, 75, 88); padding: 0cm 5.4pt; height: 77px;" width="237"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;">Brief Description of Change (referring Tack and Step)</span>

<span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; color: white; mso-themecolor: background1; mso-fareast-language: EN-NZ;"> </span>

</td></tr><tr style="height: 24.32px;"><td style="width: 147.365px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 24.32px;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1.0</span>

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 24.32px;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">09 Feb 2024</span>

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 24.32px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">G Andreos</span>

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 24.32px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">N Owens</span>

</td><td style="width: 147.394px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 24.32px;" width="237"><span style="font-family: Verdana, sans-serif;"><span style="font-size: 10.6667px;">Document creation</span></span>

</td></tr><tr style="height: 49.93px;"><td style="width: 147.365px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 49.93px;" width="85"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">1.1</span>

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 49.93px;" width="104"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">14 Feb 2024</span>

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 49.93px;" width="146"><span style="font-size: 8.0pt; font-family: 'Verdana',sans-serif; mso-fareast-font-family: 'Times New Roman'; mso-bidi-font-family: 'Times New Roman'; mso-fareast-language: EN-NZ;">A MacDonald</span>

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 49.93px;" width="146">J Paloma

</td><td style="width: 147.394px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding-top: 0cm; padding-right: 5.4pt; padding-bottom: 0cm; height: 49.93px;" width="237"><span style="font-size: 11.0pt; font-family: 'Calibri',sans-serif; mso-fareast-font-family: Calibri; mso-fareast-theme-font: minor-latin; mso-ligatures: standardcontextual; mso-ansi-language: EN-NZ; mso-fareast-language: EN-US; mso-bidi-language: AR-SA;"><span style="font-family: Verdana, sans-serif;"><span style="font-size: 10.6667px;">Central Management Config</span></span></span>

</td></tr><tr style="height: 46.08px;"><td style="width: 147.365px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 46.08px;">1.2

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 46.08px;">16 Feb 2024

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 46.08px;">G Andreos

</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 46.08px;"> </td><td style="width: 147.394px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 46.08px;">Added EFTPOS and Printer sections

</td></tr><tr style="height: 34.88px;"><td style="width: 147.365px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 34.88px;">1.3</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 34.88px;">21 Feb 2024</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 34.88px;">J Paloma</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 34.88px;">  
</td><td style="width: 147.394px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 34.88px;">Added Mitel Phones section</td></tr><tr style="height: 34.88px;"><td style="width: 147.365px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 34.88px;">1.4</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 34.88px;">2 May 2024</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 34.88px;">T Makoni</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 34.88px;">`M Macdonald</td><td style="width: 147.394px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding-top: 0cm; padding-right: 5.4pt; padding-bottom: 0cm; height: 34.88px;">Clarified escalation thresholds</td></tr><tr style="height: 51.68px;"><td style="width: 147.365px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 51.68px;">1.5</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 51.68px;">6 May 2024</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 51.68px;">J Paloma</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 51.68px;">  
</td><td style="width: 147.394px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding-top: 0cm; padding-right: 5.4pt; padding-bottom: 0cm; height: 51.68px;">Added removal of FMG-Access on WAN1</td></tr><tr style="height: 51.68px;"><td style="width: 147.365px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 51.68px;">1.6</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 51.68px;">6 June 2024</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 51.68px;">G Millar</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 51.68px;">  
</td><td style="width: 147.394px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding-top: 0cm; padding-right: 5.4pt; padding-bottom: 0cm; height: 51.68px;">Added ensure you sync firewall correctly.</td></tr><tr style="height: 85.28px;"><td style="width: 147.365px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 85.28px;">1.7</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 85.28px;">17 July 2024</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 85.28px;">G Andreos</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 85.28px;">  
</td><td style="width: 147.394px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding-top: 0cm; padding-right: 5.4pt; padding-bottom: 0cm; height: 85.28px;">Change wording in AP section to follow workaround for Bug# AOS-256401</td></tr><tr style="height: 51.68px;"><td style="width: 147.365px; border-right: 1pt solid windowtext; border-bottom: 1pt solid windowtext; border-left: 1pt solid windowtext; border-image: initial; border-top: none; padding: 0cm 5.4pt; height: 51.68px;">1.8</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 51.68px;">16 Aug 2024</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 51.68px;">D Torreja</td><td style="width: 147.365px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding: 0cm 5.4pt; height: 51.68px;">G Millar</td><td style="width: 147.394px; border-top: none; border-left: none; border-bottom: 1pt solid windowtext; border-right: 1pt solid windowtext; padding-top: 0cm; padding-right: 5.4pt; padding-bottom: 0cm; height: 51.68px;">Added Fex section &amp; to do failover if has 4G backup</td></tr></tbody></table>