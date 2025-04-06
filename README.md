# OSPF 10 – Multi-Area OSPF Lab (EVE-NG)

Welcome to the **OSPF 10 Lab**, a hands-on advanced OSPF (Open Shortest Path First) simulation designed and inspired by **Sir Tauqeer Shah SB**. This project focuses on building multi-area routing configurations using Cisco devices inside the **EVE-NG network emulator**.

---

## 🧩 Topology Overview

This OSPF lab is structured into **three areas**:

- **Area 0 (Backbone)** – Core connectivity zone with multiple routers and hosts
- **Area 01** – A branch-like segment containing PC_1 and internal routers A, B, C, F, J, K
- **Area 02** – Another logical network containing PC_2 and routers D, E, N, I, M

### 🌐 Key Lab Objective:

> **Ping from PC_1 (192.168.200.10) in Area 01 to PC_4 (192.168.100.3) in Area 0.**  
> This validates complete OSPF route propagation across all areas.

---

## 🛠️ Devices & Configuration Highlights

- **Routers (A to N)** – Configured with OSPF Process ID 99
- **Switches (SW_1, SW_2, SW_3)** – Layer 2 connectivity
- **PCs (PC_1 to PC_6)** – End devices used for ping tests and endpoint validation
- **Serial Interfaces** – For inter-router communication (e.g., S1/0, S1/1)
- **Ethernet Interfaces** – For connecting PCs to switches

---

## 🔗 Addressing Scheme (Examples)

| Device | Interface | IP Address       | Notes               |
|--------|-----------|------------------|---------------------|
| PC_1   | e0        | 192.168.200.10   | Area 01 (Router A)  |
| PC_2   | e0        | 192.168.1.10     | Area 02 (Router N)  |
| PC_4   | e0/1      | 192.168.100.3    | Area 0 (Router K)   |
| A      | e0/0      | 192.168.200.100  | Connected to PC_1   |

For full IP plan, refer to the topology diagram.

---

## 🔁 Task Workflow

1. Configure each router with the correct OSPF area ID (Area 0, 1, or 2).
2. Enable OSPF using:
   ```bash
   router ospf 10
   network <network_ip> <wildcard_mask> area <area_id>
