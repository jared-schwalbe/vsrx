---

copyright:
  years: 2018
lastupdated: "2018-10-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}

# Creating the New Interface, Zone, and Address Book Subnet
{: #creating-the-new-interface-zone-and-address-book-subnet}

First, you'll need to create an interface unit for the VLAN and add the subnet's gateway address. You'll then be able to create a security zone associated with the new unit and an `address-book` entry for the subnet.  

**NOTE:** Scroll to the right to view the entire command!

```
set interfaces reth3 unit 1523 vlan-id 1523
set interfaces reth3 unit 1523 family inet address 169.47.211.153/29
set security zones security-zone CUSTOMER-PUBLIC interfaces reth3.1523 host-inbound-traffic system-services all
set security address-book global address VSI_PUB_NET 169.47.211.152/29
```