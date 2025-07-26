# 13Cubed-Mini-Memory-CTF
📂 CTF Case Name: 13Cubed Mini Memory CTF
📅 Date: Saturday, 26 July 2025 — Day 26 of 700

---

🔍 Challenge Overview

🧠 Memory Dump File: memdump.mem  
🔧 Volatility Version: 3.2.26  
🖥️ OS Profile: Win10x64  

---

1️⃣ Identify Malicious Process  
- Tool: pslist / psscan  
- Suspicious PID: 360 / 8560  
- Technique: Typo-squatting (`scvhost.exe`)  
- Flag (MD5 of PID): `e7b24b112a44fdd9ee93bdf998c6ca0e`

---

2️⃣ Dump and Analyze Memory  
- Tool: memdump, strings  
- Base64 String: `M2ExOTY5N2YyOTA5NWJjMjg5YTk2ZTQ1MDQ2Nzk2ODA=`  
- Decoded Flag: `3a19697f29095bc289a96e4504679680`

---

3️⃣ Default Gateway MAC Address  
- Tool: printkey / dumpregistry  
- MAC: `00-50-56-FE-D8-07`  
- Flag (MD5): `6496d43b622a2ad241b4d08699320f4e`

---

4️⃣ Browser Cache File Path  
- Tool: mftparser  
- Path (uppercase):  
`USERS\CTF\APPDATA\LOCAL\PACKAGES\MICROS~1.MIC\AC\#!001\MICROS~1\CACHE\AHF2COV9\13CUBED[1].HTM`  
- Flag (MD5): `b5bdd048030cd26ab2d0e7f7e351224d`

---

🧩 Other Observations  
- Registry vs. System timestamp anomaly (+10s)  
- Multiple zero-thread suspicious processes: `cmd.exe`, `MicrosoftEdge`, `svchost.exe`  
- Timeline correlation suggests process hollowing or rootkit-level tampering

---

✅ Summary:  
One of the strongest memory-based CTFs yet. Memory dump contained multiple signs of anti-forensics, process injection, and rogue processes masked cleverly using naming tricks and timeline deception.

