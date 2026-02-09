# NOC Process - FortiGate VPN Geolocation

**Standard Operating Procedure**

**NOC PROCESS - Adding a Geolocation to a client's VPN**

<table id="bkmrk-purpose-to-ensure-th" style="width: 802px; height: 331.667px;" width="720"><tbody><tr style="height: 53.6806px;"><td style="width: 168px; height: 53.6806px;"><p class="callout success">**Purpose**</p>

</td><td style="width: 634px; height: 53.6806px;" width="632"><span style="color: #ff6600;">P</span><span style="color: #ff6600;">rocess to follow when a customer requests to add a Geolocation to their FortiGate VPN</span>

</td></tr><tr style="height: 53.6806px;"><td style="width: 168px; height: 53.6806px;"><p class="callout success">**Scope**</p>

</td><td style="width: 634px; height: 53.6806px;" width="632"><span style="color: #ff6600;">NOC, All clients</span>

</td></tr><tr style="height: 53.6806px;"><td style="width: 168px; height: 53.6806px;"><p class="callout success">**Business Rules**</p>

</td><td style="width: 634px; height: 53.6806px;" width="632"><span style="color: #ff6600;"> </span>

</td></tr><tr style="height: 53.6806px;"><td style="width: 168px; height: 53.6806px;"><p class="callout success">**Inputs**</p>

</td><td style="width: 634px; height: 53.6806px;" width="632"><span style="color: #ff6600;">Email</span>

</td></tr><tr style="height: 53.6806px;"><td style="width: 168px; height: 53.6806px;"><p class="callout success">**Outputs**</p>

</td><td style="width: 634px; height: 53.6806px;" width="632"><span style="color: #ff6600;">Geolocation added to client's VPN</span>

</td></tr><tr style="height: 63.2639px;"><td style="width: 168px; height: 63.2639px;"><p class="callout success">**Notes**</p>

</td><td style="width: 634px; height: 63.2639px;" width="632"><span style="color: #ff6600;">This SOP is SML specific but Task 2 can be followed for all clients</span>

<span style="color: #ff6600;">NOTE: <span style="background-color: rgb(224, 62, 45); color: rgb(0, 0, 0);">Japan must never be removed as that is where Hamish Bradshaw is based</span></span>

</td></tr></tbody></table>

**PROCESS FLOW CHART**

<table id="bkmrk-steps-task-1-%E2%80%93-noc-1" style="width: 809px;" width="720"><tbody><tr><td style="width: 128px;"><p class="callout success">**Steps**</p>

</td><td style="width: 681px;"><p class="callout success">**Task 1 – NOC - Recording Change and Creating Tasks**</p>

</td></tr><tr><td style="width: 128px;">**1**

</td><td style="width: 681px;"><p class="callout info">Check the **SML - Geolocation** Calendar doesn't already contain the requested country and time frame.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/scaled-1680-/S21image.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/S21image.png)

<p class="callout danger">SML have been known to request the same Geolocation for different people at times that overlap. The Geolocation is a blanket allow and doesn't need to be activated for specific people/devices.</p>

</td></tr><tr><td style="width: 128px;">**2**

</td><td style="width: 681px;"><p class="callout info">If location/time isn't already in the calendar create a SIMPLE MAC ticket in Freshservice containing the details of the request.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/scaled-1680-/VdMimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/VdMimage.png)

<p class="callout warning">**Information needed to create a Geolocation allow:** Country, Firewall Policy, Start date, End date.</p>

</td></tr><tr><td style="width: 128px;">**3**

</td><td style="width: 681px;"><p class="callout info">Create a task in ticket about added the Geolocation to the Firewall Policy using the "Handover - Action Required" Scenario.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/scaled-1680-/kAjimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/kAjimage.png)

<p class="callout info">Edit the task and set the due date to the morning of the requested start date. Also input details on what you want to be done.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/scaled-1680-/P7iimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/P7iimage.png)

<p class="callout warning">If the start date is today, this step doesn't need to be done. Simply add the Geolocation to the policy.</p>

<p class="callout info">Create a task in ticket about removing the Geolocation from the Firewall Policy using the "Handover - Action Required" Scenario.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/scaled-1680-/kAjimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/kAjimage.png)

<p class="callout info">Edit the task and set the due date to the day after the requested end date. Also input details on what you want to be done.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/scaled-1680-/FWyimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/FWyimage.png)

</td></tr><tr><td style="width: 128px;">**4**

</td><td style="width: 681px;"><p class="callout info">Create an appointment in the "FortiGate - Geolocation" Calendar. For the title input the client code, Firewall policy and country. Input the start and end dates and check the "All day" box.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/scaled-1680-/4iPimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/4iPimage.png)

<p class="callout info">Change the category of the appointment to correspond with the colours found [here](https://celloltd.sharepoint.com/:x:/r/sites/NOC/Shared%20Documents/General/Geo%20Location%20Colours.xlsx?d=waa16fe19fba946c5a73999663633dc20&csf=1&web=1&e=aSgYic "Geolocation Colours").</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/scaled-1680-/QXBimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/QXBimage.png)

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/scaled-1680-/aYximage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/aYximage.png)

<p class="callout warning">If the country doesn't exist in the spreadsheet, add it in and select a colour. Also create a new category in Outlook and select the same colour.</p>

</td></tr></tbody></table>

<table id="bkmrk-steps-task-2-%E2%80%93-noc-1" style="width: 809px;" width="720"><tbody><tr><td style="width: 131px;"><p class="callout success">**Steps**</p>

</td><td style="width: 678px;"><p class="callout success">**Task 2 – Add Geolocation to FortiGate Policy**</p>

</td></tr><tr><td style="width: 131px;">**1**

</td><td style="width: 678px;"><p class="callout info">Login to FortiManager via the management RDP jumphost: [https://m-chc01-fmg01/](https://m-chc01-fmg01/)</p>

  
[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/5DTimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/5DTimage.png)

</td></tr><tr><td style="width: 131px;">**2**

</td><td style="width: 678px;"><p class="callout info">Select the customer's ADOM you are wanting to modify</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/wriimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/wriimage.png)

</td></tr><tr><td style="width: 131px;">**3**

</td><td style="width: 678px;"><p class="callout info">Navigate to "Policy &amp; Objects" &gt; "Policy Packages" and select the Package to update. e.g. for SML it will be 'SML-AKL05-CCF01'</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/sHNimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/sHNimage.png)

</td></tr><tr><td style="width: 131px;">**4**

</td><td style="width: 678px;"><p class="callout info">Lock the ADOM </p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/9Kcimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/9Kcimage.png)

</td></tr><tr><td style="width: 131px;">**5**

</td><td style="width: 678px;"><p class="callout info">Locate the policy the customer has provided and select "Edit"</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/x8zimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/x8zimage.png)

**OR**

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/iTbimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/iTbimage.png)

</td></tr><tr><td style="width: 131px;">**6**

</td><td style="width: 678px;"><p class="callout info">Select "Address" and search for the country you want to add</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/adkimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/adkimage.png)

<p class="callout success">You can check the abbreviation by clicking 'Edit' and reviewing the Geography section</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/fIlimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/fIlimage.png)

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/h0Uimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/h0Uimage.png)

<p class="callout warning">If the Firewall address isn't there you will need to create it (follow step 7 onwards) . Otherwise select the country, select OK and proceed to step 10</p>

</td></tr><tr><td style="width: 131px;">**7**

</td><td style="width: 678px;"><p class="callout info">Click the + and select "Address"</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/Dd8image.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/Dd8image.png)

</td></tr><tr><td style="width: 131px;">**8**

</td><td style="width: 678px;"><p class="callout info">Input the appropriate information following the correct naming convention and select OK</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/scaled-1680-/JJLimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2022-11/JJLimage.png)

</td></tr><tr><td style="width: 131px;">**9**

</td><td style="width: 678px;"><p class="callout info">Select the newly created Geolocation and add it to the policy once created </p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/2zzimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/2zzimage.png)

<p class="callout info">Please ensure the 'Negate Source' is unticked:</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/cbOimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/cbOimage.png)

</td></tr><tr><td style="width: 131px;">**10**

</td><td style="width: 678px;"><p class="callout danger">Save the policy and have it reviewed by either Senior NOC or a Security Engineer if you see unfamiliar config. Otherwise peer-review with your shift partner.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/TOJimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/TOJimage.png)

</td></tr><tr><td style="width: 131px;">**11**

</td><td style="width: 678px;"><p class="callout info">Push the new policy to the Firewall using the Install Wizard</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/WiJimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/WiJimage.png)

</td></tr><tr><td style="width: 131px;">**12**

</td><td style="width: 678px;"><p class="callout info">Select **Install Policy Package &amp; Device Settings,** input the ticket number in the comment field and click next</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/Xnaimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/Xnaimage.png)

</td></tr><tr><td style="width: 131px;">**13**

</td><td style="width: 678px;"><p class="callout info">Ensure only the device you want to push the policy to is selected and click next</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/q7uimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/q7uimage.png)

</td></tr><tr><td style="width: 131px;">**14**

</td><td style="width: 678px;"><p class="callout danger">Once the validation has been completed, view the install preview </p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/Qloimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/Qloimage.png)

<p class="callout danger">Ensure you are not overwriting any configuration and you do not see any configuration you are unfamiliar with. If unsure please raise to Senior NOC or Engineering (nse@cello.co.nz). Copy and Paste the config into the ticket and also download the configuration and put it in the ticket.</p>

<p class="callout info">Below is one example of a configuration good to push.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/gmfimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/gmfimage.png)

</td></tr><tr><td style="width: 131px;">**15**

</td><td style="width: 678px;"><p class="callout info">Close install preview and click install. Confirm the policy has been pushed to the device successfully</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/mEzimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/mEzimage.png)

</td></tr><tr><td style="width: 131px;">**16**

</td><td style="width: 678px;"><p class="callout info">**Unlock** the ADOM, **Update** the ticket and A**dvise** the customer which countries have been added.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/6EUimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/6EUimage.png)

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/U2Fimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/U2Fimage.png)

</td></tr></tbody></table>

<table id="bkmrk-steps-task-2-%E2%80%93-remov" style="width: 809px;" width="720"><tbody><tr><td style="width: 131px;"><p class="callout success">**Steps**</p>

</td><td style="width: 678px;"><p class="callout success">**Task 3 – Remove Geolocation from FortiGate Policy**</p>

</td></tr><tr><td style="width: 131px;">**1**

</td><td style="width: 678px;"><p class="callout info">Login to FortiManager via the management RDP jumphost: [https://m-chc01-fmg01/](https://m-chc01-fmg01/)</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/5DTimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/5DTimage.png)  
</td></tr><tr><td style="width: 131px;">**2**

</td><td style="width: 678px;"><p class="callout info">Select the customer's ADOM you are wanting to modify</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/wriimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/wriimage.png)  
</td></tr><tr><td style="width: 131px;">**3**

</td><td style="width: 678px;"><p class="callout info">Navigate to "Policy &amp; Objects" &gt; "Policy Packages" and select the Package to update. e.g. for SML it will be 'SML-AKL05-CCF01'</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/sHNimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/sHNimage.png)  
</td></tr><tr><td style="width: 131px;">**4**

</td><td style="width: 678px;"><p class="callout info">Lock the ADOM </p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/9Kcimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/9Kcimage.png)  
</td></tr><tr><td style="width: 131px;">**5**

</td><td style="width: 678px;"><p class="callout info">Locate the policy the customer has provided and select "Edit"</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/x8zimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/x8zimage.png)

**OR**

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/iTbimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/iTbimage.png)  
</td></tr><tr><td style="width: 131px;">**6**

</td><td style="width: 678px;"><p class="callout info">Under "Source" and click the "X" button on the country you want to remove and click 'OK'</p>

  
[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/zZBimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/zZBimage.png)

<p class="callout info">Please ensure the 'Negate Source' is unticked:</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/S5pimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/S5pimage.png)

</td></tr><tr><td style="width: 131px;">**7**

</td><td style="width: 678px;"><p class="callout danger">Save the policy and have it reviewed by either Senior NOC or a Security Engineer if you see unfamiliar config. Otherwise peer-review with your shift partner.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/TOJimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/TOJimage.png)  
</td></tr><tr><td style="width: 131px;">**8**

</td><td style="width: 678px;"><p class="callout info">Push the new policy to the Firewall using the Install Wizard</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/UZfimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/UZfimage.png)

</td></tr><tr><td style="width: 131px;">**9**

</td><td style="width: 678px;"><p class="callout info">Select **Install Policy Package &amp; Device Settings,** input the ticket number in the comment field and click next</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/cm0image.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/cm0image.png)

</td></tr><tr><td style="width: 131px;">**10**

</td><td style="width: 678px;"><p class="callout info">Ensure only the device you want to push the policy to is selected and click next</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/E5timage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/E5timage.png)

</td></tr><tr><td style="width: 131px;">**11**

</td><td style="width: 678px;"><p class="callout danger">Ensure you are not overwriting any configuration and you do not see any configuration you are unfamiliar with. If unsure please raise to Senior NOC or Engineering (nse@cello.co.nz). **Copy and Paste** the config into the ticket and also download the configuration and put it in the ticket.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/aGXimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/aGXimage.png)

</td></tr><tr><td style="width: 131px;">**12**

</td><td style="width: 678px;"><p class="callout info">Close install preview and click install. Confirm the policy has been pushed to the device successfully</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/UEWimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/UEWimage.png)

</td></tr><tr><td style="width: 131px;">**13**

</td><td style="width: 678px;"><p class="callout info">**Unlock** the ADOM, **Update** the ticket and A**dvise** the customer which countries have been removed.</p>

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/lYkimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/lYkimage.png)

[![image.png](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/scaled-1680-/BjYimage.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2025-12/BjYimage.png)

</td></tr></tbody></table>

<table id="bkmrk-end-of-sop-sop-docum" style="width: 810px; height: 335.191px;" width="718"><tbody><tr style="height: 53.8715px;"><td colspan="5" style="width: 810px; height: 53.8715px;"><p class="callout success">**End Of SOP**</p>

</td></tr><tr style="height: 53.8715px;"><td colspan="5" style="width: 810px; height: 53.8715px;"><p class="callout success">**SOP Document Version Control**</p>

</td></tr><tr style="height: 121.024px;"><td style="width: 162px; height: 121.024px;"><p class="callout success">**Version No:**</p>

</td><td style="width: 162px; height: 121.024px;"><p class="callout success">**Effective Date**</p>

</td><td style="width: 162px; height: 121.024px;"><p class="callout success">**Author**</p>

</td><td style="width: 162px; height: 121.024px;"><p class="callout success">**Approver**</p>

</td><td style="width: 162px; height: 121.024px;"><p class="callout success">**Brief Description of Change (referring Tack and Step)**</p>

</td></tr><tr style="height: 29.8785px;"><td style="width: 162px; height: 29.8785px;">1.0</td><td style="width: 162px; height: 29.8785px;">  
</td><td style="width: 162px; height: 29.8785px;">Nick Owens</td><td style="width: 162px; height: 29.8785px;">Kate James</td><td style="width: 162px; height: 29.8785px;">Creation artefact

</td></tr><tr style="height: 46.6667px;"><td style="width: 162px; height: 46.6667px;">1.1

</td><td style="width: 162px; height: 46.6667px;"></td><td style="width: 162px; height: 46.6667px;">Gareth Millar

</td><td style="width: 162px; height: 46.6667px;"></td><td style="width: 162px; height: 46.6667px;">**Task 3 – Remove Geolocation added**

</td></tr><tr style="height: 29.8785px;"><td style="width: 162px; height: 29.8785px;">2.0

</td><td style="width: 162px; height: 29.8785px;"></td><td style="width: 162px; height: 29.8785px;">Michelle Lee

</td><td style="width: 162px; height: 29.8785px;">G. Millar

</td><td style="width: 162px; height: 29.8785px;">Updating Images / Text to new FAM UI

</td></tr></tbody></table>