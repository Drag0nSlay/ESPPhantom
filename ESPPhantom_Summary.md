# ESPPhantom — Full Project Summary
> ABES Institute of Technology, Ghaziabad | CSE (IoT) | Session 2025-26

---

## 📋 Project Basic Info

| Field | Details |
|---|---|
| **Project Name** | ESPPhantom: Network Pentesting Tool |
| **Project ID** | 2023CSEIoT007 |
| **College** | ABES Institute of Technology, Ghaziabad |
| **Department** | CSE (IoT) |
| **Supervisor** | Mr. Vineet Kumar Singh (Assistant Professor, CSE-AI) |
| **Session** | 2025-26 |

---

## 👥 Team Members

| # | Name | Roll No |
|---|---|---|
| 1 | Raghav Sharma | 2302901550051 |
| 2 | Rudra Pandit | 2302901550054 |
| 3 | Saurabh Shukla | 2302901550055 |
| 4 | Aman Kothari | 2302901550004 |

---

## 💡 Ek Line Mein Project Kya Hai?

> ESPPhantom ek **portable wireless security auditing device** hai jo ESP32-S3 microcontroller pe bana hai aur ek saath **5 wireless protocols** — Wi-Fi, Bluetooth LE, 2.4GHz RF, Sub-GHz aur Infrared — ko test kar sakta hai.

---

## ❗ Problem Kya Hai?

Aaj kal wireless technologies jaise Wi-Fi, Bluetooth, Zigbee, Sub-GHz bahut zyada use ho rahi hain — ghar mein, offices mein, cars mein, IoT devices mein. Lekin inme se bahut saari technologies:

- Weak encryption use karti hain
- Poor authentication hoti hai
- Insecure configurations hoti hain

### Existing Tools Ki Problems:
- ❌ Bahut expensive hain (Kali Linux + SDR setup = ₹15,000+)
- ❌ Sirf ek protocol support karte hain
- ❌ Bahut bulky aur complex hain

**Isliye ek aisa tool chahiye jo — portable ho, affordable ho, aur ek saath multiple protocols test kar sake.**

---

## ✅ Humara Solution — ESPPhantom

Hum ek aisa device bana rahe hain jo:

- 📦 **Size mein small** ho (haath mein aa jaye)
- 🔋 **Battery powered** ho (kahin bhi use karo)
- 📡 **5 protocols** ek saath handle kare
- 🖥️ **Onboard display** ho real-time data dekhne ke liye
- 💾 **SD Card storage** ho captured signals save karne ke liye
- 🔧 **Modular design** ho taaki future mein expand kar sakein

---

## 📡 5 Protocols — Simple Explanation

### 1. Wi-Fi 802.11
- Sabse common wireless protocol — ghar, college, office sab jagah
- **Vulnerability:** Deauth packets encrypted nahi hote — koi bhi device ko network se disconnect kar sakta hai
- **Device kya karega:** Networks scan karna, hidden SSIDs dhundhna, deauth vulnerability demonstrate karna

### 2. Bluetooth Low Energy (BLE)
- Smartwatches, earphones, IoT sensors mein use hota hai
- **Vulnerability:** Devices continuously broadcast karte hain — tracking possible hai
- **Device kya karega:** BLE devices scan karna, unauthorized trackers detect karna

### 3. 2.4 GHz RF
- Wi-Fi, BLE, Zigbee, wireless keyboards sab isi band mein kaam karte hain
- **Vulnerability:** Bahut crowded band — interference easy hai, kuch keyboards unencrypted data bhejte hain
- **Device kya karega:** Spectrum monitor karna, interference detect karna

### 4. Sub-GHz (433MHz / 868MHz / 915MHz)
- Car key fobs, garage door openers, smart home sensors mein use hota hai
- **Vulnerability:** Most devices rolling codes use nahi karte — same signal baar baar kaam karta hai
- **Device kya karega:** Signal weakness identify karna, replay vulnerability demonstrate karna

### 5. Infrared (IR)
- TV remote, AC remote, set-top box mein use hota hai
- **Vulnerability:** Almost zero authentication hoti hai
- **Device kya karega:** IR signals analyze karna, universal remote simulate karna

---

## ⚔️ 5 Security Test Simulations

| Attack | Kya Demonstrate Hoga |
|---|---|
| **Deauthentication Attack** | Wi-Fi DoS vulnerability |
| **Spoofing Attack** | Fake network detection awareness |
| **Replay Attack** | RF/IR signal weakness |
| **Jamming Simulation** | Wireless interference testing |
| **Captive Portal Attack** | Rogue hotspot detection |

---

## 🤔 Why ESP32-S3?

- ⚡ Dual-core processor (240MHz) — fast processing
- 📶 Built-in Wi-Fi + BLE — extra module nahi chahiye
- 👁️ Promiscuous mode — passive monitoring possible
- 🔌 45 GPIO pins — external RF modules connect karne ke liye
- 💰 Cost: sirf ₹400-600 — bahut affordable

---

## 🆚 Humara Device vs Others

| Feature | Kali Linux Setup | Flipper Zero | ESPPhantom |
|---|---|---|---|
| Cost | ₹15,000+ | ₹12,000+ | ₹2,000-3,000 |
| Portable | ❌ | ✅ | ✅ |
| Wi-Fi Testing | ✅ | Limited | ✅ |
| Sub-GHz | SDR chahiye | ✅ | ✅ |
| Open Source | ✅ | Partial | ✅ |
| Beginner Friendly | ❌ | ✅ | ✅ |

---

## 🛡️ Sahi Framing — Defensive Angle (IMPORTANT!)

### ❌ Kabhi Mat Bolo:
- "Hum deauth attack kar sakte hain"
- "Hum kisi ka signal capture kar sakte hain"
- "Hum car unlock kar sakte hain"

### ✅ Hamesha Aise Bolo:
- "Hum **vulnerability demonstrate** kar sakte hain"
- "Hum **network administrators ko alert** kar sakte hain"
- "Hum **weaknesses identify** karte hain taaki unhe fix kiya ja sake"

---

## 🌍 Real World Useful Applications

### 1. 🏫 Educational Purpose
- Students ko practically wireless attacks samjhana
- Cybersecurity lab tool ki tarah use karna
- *"Jab tak attack samjhoge nahi, defend nahi kar paoge"*

### 2. 🏢 Network Security Auditing
- IT admin apne office Wi-Fi ki vulnerabilities khud test kare
- Companies apne network ki security audit karwa sakti hain

### 3. 🔬 Research Purpose
- Universities aur research labs ke liye
- New protocols ki security evaluate karna
- IEEE papers ke liye experimental data collect karna

### 4. 🏠 IoT Device Testing
- Manufacturers apne products release se pehle test kar sakein
- Smart home devices ki vulnerabilities fix karna
- *"Better we find the bug than a hacker does"*

### 5. 🚗 Automotive Security
- Car key fob systems test karna
- Rolling code implementation verify karna

---

## 🔒 Defensive Features

| Feature | Defensive Use |
|---|---|
| Network Scanning | Unauthorized devices detect karna apne network pe |
| Spectrum Monitoring | Interference aur jamming attempts detect karna |
| BLE Scanning | Unauthorized BLE trackers dhundhna |
| Signal Analysis | Weak encryption wale devices identify karna |
| Captive Portal Detection | Rogue hotspots detect karna public places mein |

---

## 💬 Strong One-Liners For Panel

> *"ESPPhantom ek diagnostic tool hai — jaise ek doctor X-Ray machine use karta hai bimari dhundhne ke liye, hum ESPPhantom use karte hain network ki kamzoriyan dhundhne ke liye — taaki unhe theek kiya ja sake."*

> *"ESPPhantom ek affordable, portable, multi-protocol wireless security auditing platform hai jo organizations, researchers aur students ko apne khud ke networks ki vulnerabilities identify karne mein help karta hai — taaki unhe exploit hone se pehle fix kiya ja sake. Yeh offensive tool nahi, balki ek defensive security instrument hai."*

---

## 🧠 Important Technical Fact (Panel Ko Impress Karega)

> IEEE 802.11 standard mein management frames ko protect karna originally optional tha — isliye **2009 se deauthentication attacks possible hain**. 2012 mein **802.11w amendment** aaya lekin aaj bhi most devices isko properly implement nahi karte. ESPPhantom isi vulnerability ko ethically demonstrate karta hai.

---

## ❓ Panel Ke Expected Questions — Quick Answers

**Q: Abhi tak kya kiya hai?**
> Research complete ki, components finalize kiye, architecture plan ready hai, implementation next phase mein start hogi.

**Q: Kya yeh legal hai?**
> Haan, sirf controlled aur ethical environment mein use ke liye designed hai — lab testing aur security research ke liye.

**Q: Flipper Zero se alag kaise hai?**
> Open-source hai, cost bahut kam hai (₹2000-3000), aur specifically IoT + educational use ke liye customize hai.

**Q: Future scope kya hai?**
> GPS logging, web-based dashboard, Zigbee support, aur cloud-based signal analysis add karna hai.

**Q: ESP32-S3 hi kyun choose kiya?**
> Built-in Wi-Fi + BLE, promiscuous mode support, 240MHz dual-core processor, aur sirf ₹400-600 cost — best value for money.

**Q: Yeh offensive tool nahi hai?**
> Bilkul nahi. Jaise Wireshark, Kali Linux, aur Metasploit legal security tools hain, ESPPhantom bhi usi category mein hai — ek defensive security instrument.

---

## 🏭 Ethical Hacking Industry Context

- **CEH** (Certified Ethical Hacker) — globally recognized certification hai
- **Google, Microsoft** bug bounty programs — companies khud hackers ko hire karti hain
- **Kali Linux, Metasploit, Wireshark** — yeh sab legal tools hain same category ke
- ESPPhantom = inhi tools ka portable + affordable version

---

> # 🔥 All the best for your presentation today!
