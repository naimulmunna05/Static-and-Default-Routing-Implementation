# Static-and-Default-Routing-Implementation
# Static-and-Default-Routing-Implementation

Overview: A multi-router enterprise network simulation built in Cisco Packet Tracer to implement & test both Static & Default Routing across different subnets.

## 📋 Project Summary Table

| Category | Details / Description |
| :--- | :--- |
| Network Scope | Multi-subnet network connecting Dhanmondi, Banani, and Gulshan locations |
| Hardware Architecture | • Cisco 2811 Routers<br>• Cisco 2950 Switches<br>• PCs (End-user devices) |
| Tools & Skills | • Cisco Packet Tracer<br>• Static & Default Routing (`ip route`)<br>• Serial & FastEthernet Cabling<br>• Connectivity & Ping Testing |

## 🔀 Routing Types & Explanation

| Router Name | Routing Type | Command Used | Why Used? |
| :--- | :--- | :--- | :--- |
| Router0 (Dhanmondi) | Default Routing | `ip route 0.0.0.0 0.0.0.0 10.0.0.2` | Used because this router has only one exit path. It forwards all unknown or external traffic to the central router using a default gateway (`0.0.0.0`). |
| Router1 (Bonani) | Static Routing | `ip route 192.168.1.0 255.255.255.0 10.0.0.1`<br>`ip route 192.168.3.0 255.255.255.0 11.0.0.2` | Used to manually and precisely define specific paths to reach different left and right networks. |
| Router2 (Gulshan) | Default Routing | `ip route 0.0.0.0 0.0.0.0 11.0.0.1` | Used because this router also has only one exit path. It sends all unknown traffic back through the default route. |

## 📊 IP Addressing Table

| Device / Location | Host Name | Interface | IP Address | Subnet Mask | Default Gateway |
| :--- | :--- | :--- | :--- | :--- | :--- |
| Dhanmondi | Router0 | FastEthernet0/0 | 192.168.1.100 | 255.255.255.0 | - |
| Dhanmondi | Router0 | Serial0/0/0 | 10.0.0.1 | 255.0.0.0 | - |
| Dhanmondi Dept. | PC0 | FastEthernet0 | 192.168.1.101 | 255.255.255.0 | 192.168.1.100 |
| Banani | Router1 | FastEthernet0/0 | 192.168.2.100 | 255.255.255.0 | - |
| Banani | Router1 | Serial0/0/0 | 10.0.0.2 | 255.0.0.0 | - |
| Banani | Router1 | Serial0/0/1 | 11.0.0.1 | 255.0.0.0 | - |
| Banani Dept. | PC1 | FastEthernet0 | 192.168.2.101 | 255.255.255.0 | 192.168.2.100 |
| Gulshan | Router2 | FastEthernet0/0 | 192.168.3.100 | 255.255.255.0 | - |
| Gulshan | Router2 | Serial0/0/0 | 11.0.0.2 | 255.0.0.0 | - |
| Gulshan Dept. | PC2 | FastEthernet0 | 192.168.3.101 | 255.255.255.0 | 192.168.3.100 |

## How To Run:

* Download and open the `.pkz` file in Cisco Packet Tracer.
* Run a ping test between the PCs to verify full connectivity.
