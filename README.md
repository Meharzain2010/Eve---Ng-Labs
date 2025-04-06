# OSPF Multi-Area Lab (OSPF -10)

This repository contains a multi-area OSPF configuration lab built in **EVE-NG**. The topology is divided into three areas (Area 0, Area 1, and Area 2), demonstrating inter-area routing using OSPF protocol on Cisco routers.

---

## Topology Overview

- **Area 0 (Backbone):** Core of the OSPF domain.
- **Area 1:** Contains routers A, B, F and hosts like PC1.
- **Area 2:** Contains routers E, N, and PC2.
- All areas are connected through a backbone router (G).

The goal is to simulate OSPF adjacency, routing propagation, and full connectivity across all areas.

---

## Included Files

- `OSPF -10.png`: OSPF network topology diagram.
- `OSPF -10.2.png`: Router configuration terminal view.
- `OSPF LAB.jpg`: Detailed labeled version of the topology with addressing and task instructions.

---

## Configuration Snippet Example

```bash
router ospf 10
 network 5.1.1.2 0.0.0.0 area 1
 network 8.1.1.2 0.0.0.0 area 0
 network 9.1.1.1 0.0.0.0 area 2
