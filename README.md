# Cisco Multi-Area OSPFv2 Lab
<img src="https://i.imgur.com/mbb4yUp.png" height="80%" alt="[name of screenshot]" />
## Overview
This CCNP-level lab focuses on configuring and verifying **Multi-Area OSPFv2** in a scalable Cisco router environment. It includes configuration of **stub, totally stubby**, and **default route injection**, as well as understanding and verifying **Link State Advertisements (LSAs)**.

## Lab Topology
- **Routers:** R1–R5
- **PCs:** PC1 and PC2 for connectivity testing
- **Areas:**
  - Area 0 (Backbone): R1, R2, R3
  - Area 1: R2, R4 (Stub)
  - Area 2: R3, R5 (Totally Stubby)

## Objectives
1. Configure basic router interface settings
2. Configure **multi-area OSPFv2 routing**
3. Understand and analyze **LSA Types (1–5)**
4. Implement and verify **stub** and **totally stubby** areas
5. Verify OSPF neighbor adjacencies and routing tables
6. Observe OSPF LSDB and default route propagation

## Key Configuration Highlights
- R1 originates a **default route** via a Loopback interface
- R2 & R3 act as **Area Border Routers (ABRs)**
- R1 also serves as the **Autonomous System Boundary Router (ASBR)**
- Area 1 is configured as a **stub area**
- Area 2 is configured as a **totally stubby area**
- Verification includes use of `show ip ospf database` and `show ip route ospf`

## OSPF LSA Focus
- **Type 1:** Router LSA
- **Type 2:** Network LSA
- **Type 3:** Summary LSA
- **Type 4:** ASBR Summary LSA
- **Type 5:** External LSA (default route 0.0.0.0)

## Verification Commands
```bash
show ip protocols
show ip ospf neighbor
show ip ospf database
show ip ospf interface brief
show ip route ospf
ping <remote IP>
```

## Repository Structure
```
├── configs/
│   ├── R1_Config.txt
│   ├── R2_Config.txt
│   ├── R3_Config.txt
│   ├── R4_Config.txt
│   ├── R5_Config.txt
├── README.md
├── screenshots/
└── topology.png
```

## Conclusion
This lab strengthens understanding of **OSPF hierarchical design** by implementing and troubleshooting **multi-area configurations**, OSPF **route summarization**, and **LSA types**. It is ideal for preparing for CCNP certification and real-world enterprise networking.

---
**Author:** Travis Johnson  
**Company:** 10Digit Solutions LLC  
**GitHub Repository:** [Add link when available]
