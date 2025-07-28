# Static\_Routing\_lab\_1



Lab 1 - Basic Static Routing using Cisco Packet Tracer: - 



\# 🧪 Lab 1: Basic Static Routing Between Two Routers



\## 🗂️ Overview

This lab demonstrates basic static routing between two routers using Cisco Packet Tracer. The goal is to manually configure routes allowing devices on two different networks to communicate.



---



\## 🌐 Topology



PC0 ── Router0 ── Router1 ── PC1



\- PC0: 192.168.1.2/24 → Router0: 192.168.1.1

\- Router0 ⇄ Router1 via 10.0.0.0/24

\- Router1: 192.168.2.1 → PC1: 192.168.2.2/24



---



\## 🔧 Configuration Summary



\### 👨‍💻 Router0

```bash

interface fa0/0

&nbsp;ip address 192.168.1.1 255.255.255.0

&nbsp;no shutdown



interface serial0/0

&nbsp;ip address 10.0.0.1 255.255.255.0

&nbsp;no shutdown



ip route 192.168.2.0 255.255.255.0 10.0.0.2



👨‍💻 Router1



interface fa0/0

&nbsp;ip address 192.168.2.1 255.255.255.0

&nbsp;no shutdown



interface serial0/0

&nbsp;ip address 10.0.0.2 255.255.255.0

&nbsp;no shutdown



ip route 192.168.1.0 255.255.255.0 10.0.0.1



✅ Verification

\- Use ping to test connectivity between PC0 and PC1.

\- Use show ip route on both routers to verify static routes.

\- Use show ip interface brief to check interface status



