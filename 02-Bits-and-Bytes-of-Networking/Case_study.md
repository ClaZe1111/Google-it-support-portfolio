# 🌐 Bits and Bytes of Computer Networking — Case Studies

This document contains multiple real-world inspired networking troubleshooting scenarios that demonstrate key networking concepts such as IP addressing, DNS resolution, DHCP, cabling, and performance optimization.

---

## 🧭 Case Study 1: Website Not Loading — DNS Resolution Issue

**Issue:**  
User reported that specific websites like `www.example.com` would not load, while other sites worked fine.

**Diagnosis Steps:**  
1. Checked connectivity using `ping www.example.com` — request failed.  
2. Tested with `ping 8.8.8.8` (Google DNS) — success confirmed, meaning internet was working but DNS was not resolving names.  
3. Identified issue as a DNS resolution failure.

**Actions Taken:**  
- Flushed DNS cache using:  
  ```bash
  ipconfig /flushdns


## ⚡ Case Study 2: Slow Internet Speed — Router Bottleneck

**Issue:**  
Users complained that Wi-Fi speed was extremely slow (20 Mbps) despite subscribing to a 100 Mbps internet plan.

**Diagnosis Steps:**  
1. Tested speed directly via wired connection — confirmed 100 Mbps.  
2. Checked Wi-Fi signal strength and router logs.  
3. Found outdated router firmware and crowded Wi-Fi channel.

**Actions Taken:**  
- Updated router firmware to the latest release.  
- Changed Wi-Fi channel to a less congested one.  
- Moved router to a central, open area for better coverage.  
- Retested using an online speed test (`speedtest.net`).

**Result:**  
Wi-Fi speed increased to 90–95 Mbps with stable connection.

**Key Skills Demonstrated:**  
- Router configuration and optimization  
- Wireless troubleshooting  
- Performance and speed diagnostics


## 🖧 Case Study 3: Network Connectivity Drop — Faulty Ethernet Cable

**Issue:**  
A desktop computer on a wired network randomly disconnected multiple times each day.

**Diagnosis Steps:**  
1. Verified that the network adapter was enabled in **Device Manager**.  
2. Ran continuous ping using:  
   ```bash
   ping -t 8.8.8.8