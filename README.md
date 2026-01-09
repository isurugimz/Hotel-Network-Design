# Building a Modern Hotel Network from Scratch

This isn't just a topology; it's a fully functional network infrastructure designed for a 3-story hotel scenario. I built this using **Cisco Packet Tracer** to challenge myself and apply the networking concepts I've been learning as an undergraduate.

# The Story Behind the Project
I wanted to simulate a real-world environment where different departments (like HR, Finance, and IT) need to communicate efficiently but stay secure. The challenge was to connect three separate floors while ensuring that sensitive departments remained isolated and the network was safe from unauthorized access.

# What’s Inside?
Here is how I broke down the configuration:

* **Organized Traffic (VLANs):** I didn't want a "flat" network. I created separate VLANs for every department (Reception, Finance, IT, etc.) to keep broadcast traffic low and security high.
* **Connecting the Floors (OSPF):** To get the three routers talking to each other, I implemented **OSPF**. It was satisfying to see the routing tables update dynamically!
* **Efficient IP Management (DHCP):** Instead of assigning IPs manually (who has time for that?), I configured the routers to handle DHCP allocation automatically for all laptops and printers.
* **Security First:**
    * **Remote Access:** I set up **SSH** on all routers because Telnet is just too risky in 2026!
    * **Port Security:** I simulated a security threat in the IT department. If an unauthorized device tries to plug into the IT switch, the port effectively shuts down. 

# Network Topology Breakdown
* **Floor 1:** Reception, Store, Logistics
* **Floor 2:** Finance, HR, Sales
* **Floor 3:** Admin, IT Department

# How to Test It
1.  Clone this repo or download the `.pkt` file.
2.  Open it in **Cisco Packet Tracer**.
3.  **Try to hack it:** Go to Floor 3, unplug the `Test-PC`, and plug in a different laptop to Port `Fa0/13`. Watch the port turn red!
4.  **Check Connectivity:** Try pinging the Reception PC from the Admin PC to see Inter-VLAN routing in action.

# What I Learned
Building this helped me solidify my understanding of **Router-on-a-Stick**, **OSPF troubleshooting**, and the importance of **Layer 2 Security**. It was a great hands-on experience moving beyond just theory.


**Created by:** Isuru  
*Undergraduate | University of Sri Jayewardenepura*
