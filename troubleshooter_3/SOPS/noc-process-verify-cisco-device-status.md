# NOC PROCESS - Verify Cisco Device Status

- <span class="fontstyle0">**Make sure to check both IPV6 and IPV4 bgp peerings (4G included) are established.**  
    show bgp summary  
    show bgp ipv6 summary  
      
    [![Cisco - Show BGP Summary.png](https://bookstack.cello.co.nz/uploads/images/gallery/2021-07/scaled-1680-/cisco-show-bgp-summary.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2021-07/cisco-show-bgp-summary.png)  
    </span><p class="callout info"><span class="fontstyle0">Here you're looking to see if the peering is up or down. In the **'State/PfxRcd'** column if no state is indicated, the state is up. In the example above, the **'State'** column is empty, where as the **'PfxRcd'** is **'1400'**. Then you can see the time it has been up or down in the **'Up/Down'** column.  
    </span></p>
- <span class="fontstyle0">**Check Duplex of LAN ports are negotiated correctly (100/1000/Full).**  
    show interface eth0/0/0 (replacing eth0/0/0 with the LAN  
    interface in the as-built)  
      
    </span><span class="fontstyle0">[![Cisco - Show Interface.png](https://bookstack.cello.co.nz/uploads/images/gallery/2021-07/scaled-1680-/cisco-show-interface.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2021-07/cisco-show-interface.png)</span>
- <span class="fontstyle0">**Confirm clock is current time**  
    show clock  
    </span>
- <span class="fontstyle0">**If the device has a 4g card check the radio status.**  
    show cellular #4G Interface# radio  
      
    </span><p class="callout warning">Once you have the signal at a good state or as good as you and NEC can get, open a text document and copy the signal strength values from the CLI into the document and place an asterix followed by a space at the beginning of each line. (This will be added to the ticket and Netbox as a comment when you add the device later.)</p>

<p class="callout info"><span class="fontstyle0">Signal should be Good or above. If 4G is not up to standard please refer back to solutions.</span></p>

[![image-1601868373481.png](https://bookstack.cello.co.nz/uploads/images/gallery/2020-10/scaled-1680-/image-1601868373481.png)](https://bookstack.cello.co.nz/uploads/images/gallery/2020-10/image-1601868373481.png)

- <span class="fontstyle0">**Delete the NEC user.**  
    </span><span class="fontstyle0">configure terminal  
    no username nec  
    end</span><span class="fontstyle0">  
    </span>
- <span class="fontstyle0">**Save the configuration.**  
    copy running-configuration startup-configuration</span>

- <span class="fontstyle0">**Remind the NEC tech to take some photos.**  
    They know this already, but a reminder never hurts. The photos need to be made available to Delivery.</span>

- <span class="fontstyle0">**<span style="background-color: #ffff00;">Connect Circuits in Netbox</span> (Emphasis added as this is frequently forgotten.)**  
    To help in understanding the business impact of outages to a site, please follow the below process to connect circuits:  
    [https://bookstack.cello.co.nz/books/netbox/page/assigning-circuits-to-device](https://bookstack.cello.co.nz/books/netbox/page/assigning-circuits-to-device-in-netbox)</span>

***<span class="fontstyle0">Most information can be checked with a single paste of: </span>***

*<span class="fontstyle0">sh bgp summ | inc 59  
sh bgp summ | inc 202  
sh bgp ipv6 summ | inc 2406  
sh int status  
sh clock</span>*

*<span class="fontstyle0">sh cellu 0 radio | inc RSSI  
sh cellu 0 radio | inc RSRP  
sh cellu 0 radio | inc SNR  
**OR**  
</span><span class="fontstyle0">sh cellu 0/2/0 radio | inc RSSI  
sh cellu 0/2/0 radio | inc RSRP  
</span><span class="fontstyle0">sh cellu 0/2/0 radio | inc SNR</span><span class="fontstyle0">  
</span>*