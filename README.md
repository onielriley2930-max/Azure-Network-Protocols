<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />


<h2>Video Demonstration</h2>

- ### [YouTube: Azure Virtual Machines, Wireshark, and Network Security Groups](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, RDH, DNS, HTTP/S, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>



<h2>Actions and Observations</h2>

<p>
<img src="https://imgur.com/tCiT82F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
A Network Security Group (or NSG) in Azure works like a virtual security guard for your cloud network.
It controls which traffic is allowed in or out of your Virtual Machines (VMs).

Think of it like the security checkpoint at the front gate of your Azure network.
Only approved “cars” (data) are allowed to enter or leave.
Imagine you built a small neighborhood in Azure:
		Each house = one Virtual Machine (VM)
		The road between houses = the Virtual Network (VNet)
		The security guard at the gate = the NSG

The NSG checks every car (network packet) that wants to enter or exit.
If it’s on the approved list (rules) → it passes.
If not → it’s blocked..
</p>
<br />

<p>
<img src="https://imgur.com/tFD1nNM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
What Does “Inspecting Network Protocols” Mean?

When we say “inspecting network protocols,” it means checking and analyzing the data that’s moving between computers to understand what kind of communication is happening and how it’s behaving.

Think of it as looking inside the envelope (the data packet) to see:
		Who sent it
		Who it’s going to
		What type of message it carries (like a web page, an email, or a video stream).
	 Simple Example

Imagine the internet as a big highway 🛣️ where cars = data packets.
Each car carries information following a certain rule (protocol).

Examples of protocols:
		HTTP/HTTPS → Web traffic (websites)
		SMTP → Email
		FTP → File transfer
		DNS → Translating website names to IP addresses

“Inspecting network protocols” means watching those cars on the road and checking:
		What kind of cars are passing (which protocol)
		Where they’re going
		Whether they’re allowed to pass (security check)

⸻

 Why It’s Important

Inspecting protocols helps IT systems and firewalls:
		Keep networks safe — by detecting suspicious or harmful traffic.
		Ensure rules are followed — for example, only web traffic (HTTP) is allowed, not file-sharing (FTP).
		Troubleshoot problems — like finding out why a connection isn’t working.

⸻

 In Azure or Firewalls

When Azure tools (like NSG or firewalls) inspect network protocols, they:
		Look at each packet’s header (where it’s from, where it’s going, and what type it is).
		Decide whether to allow or block it based on protocol and port rules.

⸻

 In Simple Words

“Inspecting network protocols” means looking closely at the traffic moving between computers to see what type it is and whether it’s safe or allowed to pass through.

</p>
<br />

<p>
