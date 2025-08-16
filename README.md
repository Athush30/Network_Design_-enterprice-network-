# Subnetting Lab - Cisco Packet Tracer

This project is a basic subnetting lab created using Cisco Packet Tracer. It demonstrates subnetting on the network `198.168.10.0/24` divided into 4 subnets (using a subnet mask `255.255.255.192`).Here we need only 3 subnets

## 🌐 Network Addressing Scheme
- Subnet Mask: `255.255.255.192`
- Block Size: `64`

| Subnet | Network ID      | First Host       | Last Host        | Broadcast Address |
|--------|-----------------|------------------|------------------|-------------------|
| 1      | 198.168.10.0    | 198.168.10.1     | 198.168.10.62    | 198.168.10.63     |
| 2      | 198.168.10.64   | 198.168.10.65    | 198.168.10.126   | 198.168.10.127    |
| 3      | 198.168.10.128  | 198.168.10.129   | 198.168.10.190   | 198.168.10.191    |
| 4      | 198.168.10.192  | 198.168.10.193   | 198.168.10.254   | 198.168.10.255    |

## 🖥️ Lab Setup

- 1 Router
- 3 Switches
- Each switch connects to:
  - 3 PCs
  - 1 Printer

### 🔌 Devices and IP Assignment
You can use any IPs from the valid host range of each subnet for your PCs and printers. Example:
- **Subnet 1 (198.168.10.0/26):** Switch1 connects PCs and Printer in this range.
- **Subnet 2 (198.168.10.64/26):** Switch2 connects PCs and Printer in this range.
- **Subnet 3 (198.168.10.128/26):** Switch3 connects PCs and Printer in this range.

## 📁 Files Included
- `subnetting-lab.pkt` - The main Packet Tracer lab file.
- `configs/` - Contains configuration files for router and switches.

## ⚙️ How to Use
1. Open `subnetting-lab.pkt` in Cisco Packet Tracer.
2. Explore the topology.
3. Check IP addressing on PCs and Printers.
4. Review the router and switch configuration files for CLI commands used.

## 🛠️ Basic Commands (Router Example)

```bash
interface g0/0
 ip address 198.168.10.1 255.255.255.192
 no shutdown
