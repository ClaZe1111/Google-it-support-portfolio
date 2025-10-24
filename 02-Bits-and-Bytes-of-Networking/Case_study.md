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


## 🌐 Case Study 3: Network Connectivity Drop

### 🧠 Problem:
A user reported that the **network connection keeps dropping** every few minutes, interrupting file downloads and video calls.

---

### 🔍 Diagnosis:
- Checked the **network cable and router lights** — both were operational.  
- Verified that the **network adapter** was functioning but frequently disconnecting.  
- Ran `ping 8.8.8.8 -t` in Command Prompt — observed **packet loss and timeouts** every few seconds.  
- Logged into the **router admin panel** to review DHCP logs — found that **IP lease time was only 5 minutes**, causing constant reconnections.

---

### 🧰 Troubleshooting Steps:
1. Accessed the router via `192.168.0.1`.  
2. Navigated to **Network Settings → DHCP Configuration**.  
3. Increased **DHCP lease time** from *5 minutes* to *24 hours*.  
4. Rebooted the router and renewed IP using:  
   ```bash
   ipconfig /release
   ipconfig /renew
5.Monitered connectivity for 30 minutes-no connectivity drop