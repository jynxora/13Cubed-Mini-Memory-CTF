# 13Cubed-Mini-Memory-CTF
📂 CTF Case Name: 13Cubed Mini Memory CTF
📅 Date: Saturday, 26 July 2025 — Day 26 of 700

---

##🔍 Challenge Overview

###🧠 Memory Dump File: memdump.mem  
###🔧 Volatility Version: 3.2.26  
###🖥️ OS Profile: Win10x64  

---

1. Identify Malicious Process  
- Tool: pslist / psscan  

2. Dump and Analyze Memory  
- Tool: memdump, strings  

3. Default Gateway MAC Address  
- Tool: printkey / dumpregistry  

4. Browser Cache File Path  
- Tool: mftparser  

---

##🧩 Other Observations  
- Registry vs. System timestamp anomaly (+10s)  
- Multiple zero-thread suspicious processes: `cmd.exe`, `MicrosoftEdge`, `svchost.exe`  
- Timeline correlation suggests process hollowing or rootkit-level tampering

---

## Summary:  
One of the strongest memory-based CTFs yet. Memory dump contained multiple signs of anti-forensics, process injection, and rogue processes masked cleverly using naming tricks and timeline deception.

## READ ⤵️

My Report [PDF]:

My Report [MD]:

