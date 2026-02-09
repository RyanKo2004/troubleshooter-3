# NOC PROCESS - Verify Huawei Device Status

- <span class="fontstyle0">**Make sure to check both IPV6 and IPV4 bgp peerings (4G included) are established.**  
    display bgp peer  
    display bgp ipv6 peer[![Huawei - Display BGP Peer.PNG](https://bookstack.cello.co.nz/uploads/images/gallery/2021-07/scaled-1680-/huawei-display-bgp-peer.PNG)](https://bookstack.cello.co.nz/uploads/images/gallery/2021-07/huawei-display-bgp-peer.PNG)</span><p class="callout info"><span class="fontstyle0">If the device doesn't have **'202.49.26.1'** listed as a peer, then the device doesn't have a 4G connection, as this is the IP Cello uses for 4G. You can check if it does or not on the As-Built. Here you're looking for the **'Established'** for each peer, and can see the time the peer has been established for in the **'Up/Down'** column.</span></p>
- <span class="fontstyle0">**Check Duplex of LAN ports are negotiated correctly (100/1000/Full).**  
    display interface eth0/0/0 (replacing eth0/0/0 with the LAN interface in the as-built)</span><span class="fontstyle0">[![Huawei -Display Interface.png](https://bookstack.cello.co.nz/uploads/images/gallery/2021-07/scaled-1680-/huawei-display-interface.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2021-07/huawei-display-interface.png)</span>
- <span class="fontstyle0">**Confirm clock is current time.**  
    display clock</span>
- <span class="fontstyle0">**If the device has a 4g card check the radio status.**  
    display cellular #4G Interface# radio  
    </span>

<p class="callout info"><span class="fontstyle0">Signal should be Good or above. If 4G is not up to standard please refer back to solutions.</span></p>

[![image-1601868229207.png](https://bookstack.cello.co.nz/uploads/images/gallery/2020-10/scaled-1680-/image-1601868229207.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2020-10/image-1601868229207.png)

<p class="callout warning"><span class="fontstyle0">Once you have the signal at a good state or as good as you and NEC can get, open a text document and copy the signal strength values from the CLI into the document and place an asterix followed by a space at the beginning of each line. (This will be added to the ticket and Netbox as a comment when you add the device later.)</span></p>

- <span class="fontstyle0">**Delete the NEC user.**  
    system-view  
    aaa  
    undo local-user nec  
    quit  
    quit</span>
- <span class="fontstyle0">**Save the configuration.**  
    save all</span>

- <span class="fontstyle0">**Remind the NEC tech to take some photos.**   
    They know this already, but a reminder never hurts. The photos need to be made available to Delivery.</span>

- <span class="fontstyle0">**<span style="background-color: #ffff00;">Connect Circuits in Netbox</span> (Emphasis added as this is frequently forgotten.)**  
    To help in understanding the business impact of outages to a site, please follow the below process to connect circuits:  
    [https://bookstack.cello.co.nz/books/netbox/page/assigning-circuits-to-device](https://bookstack.cello.co.nz/books/netbox/page/assigning-circuits-to-device-in-netbox)  
    </span>