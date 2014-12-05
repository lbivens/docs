.. Project-FiFo documentation master file, created by
   Heinz N. Gies on Fri Aug 15 03:25:49 2014.

**********
Networking
**********

Networks
########

List
****

Lists the Networks known to *FiFo*.

.. image:: /_static/images/jingles/networks01.png


1. Allows deleting a Network.
2. Adds a new Network.

Create
******

Creating a new Network is simple. There are not many changes to be made:

.. image:: /_static/images/jingles/networks02.png

1. The name of the network.
2. Click to create a network.

Details
*******

.. image:: /_static/images/jingles/networks03.png

1. Select an iprange to add to the network.
2. Delete an iprange from a network.
3. Delete the entire iprange.

IP-Ranges
#########

List
****

*FiFo* manages all IP provisioning. It stores a pool of IP addresses for each network you create. Upon machine creation *FiFo* assigns IP addresses, when a machine is destroyed it returns the IP addresses to the pool. The address assignment works in conjunction with the security features built into *SmartOS* to ensure that only the IP address handed out can be used on the specific network you deploy on. This ensures a good neighbour policy; it prevents malicious users of machines from spoofing IP addresses and interfering with the traffic of other machines.

.. image:: /_static/images/jingles/ipranges01.png

The default network list view shows the networks that are currently configured and columns with information specific to each network:

- **Name**: You can chose any name you like.
- **Tag**: The network **Tag** must be a real network tag that exists on at least one hypervisor/compute node.
- **Network**: The network address of your network.
- **Netmask**: The subnet mask of your network.
- **Gateway**: The network gateway.
- **First**: The first provision-able IP address in the range.
- **Last**: The last provision-able IP address in the range.
- **Next**: The next IP address that will be handed out.
- **VLAN**: The network VLAN ID (optional).
- **Returned**: The number of addresses that have been returned to the pool.
- **Action**: Delete the network by clicking on the **X** delete icon.

Create
******

To create a new network click on the |add network| button: 

.. |add network| image:: /_static/images/jingles/ipranges-add.png

.. image:: /_static/images/jingles/ipranges02.png

Populate the fields with network information relevant to the network you want to setup. The system will only allow you to select a valid network **Tag** that does in fact exist on one or more hypervisor/compute nodes.

Enter the **first** and **last** IP address in the range that you want *FiFo* to allocate.

When all required fields are filled in, the |create| button will appear.

Click on the |create| button to save your new network: 

.. |create| image:: /_static/images/jingles/ipranges-create.png
