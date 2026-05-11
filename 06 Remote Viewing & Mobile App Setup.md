# Remote Viewing & Mobile App Setup

## 📘 Objective

Configure the NVR for secure remote access via P2P cloud, static IP/DDNS, and mobile app access, enabling authorised users to view live and recorded footage from anywhere.

---

# 🌐 Remote Access Methods Comparison

| Method                  | Pros                                    | Cons                                                           |
| ----------------------- | --------------------------------------- | -------------------------------------------------------------- |
| **P2P Cloud (QR Code)** | Easy setup, no port forwarding required | Dependent on vendor cloud services; potential privacy concerns |
| **Static Public IP**    | Reliable, direct access                 | Requires ISP-provided static IP address (additional cost)      |
| **DDNS**                | Works with dynamic public IP addresses  | Requires domain configuration; slight latency possible         |
| **VPN**                 | Most secure, enterprise-grade solution  | Requires VPN server/router configuration                       |

---

# Method A — P2P Cloud Setup (Recommended for SMB)

## ☁️ Overview

P2P cloud access is the simplest and most commonly used remote viewing method for small and medium business (SMB) CCTV deployments.

### Supported Platforms

* Hik-Connect
* Dahua P2P
* Equivalent vendor cloud platforms

---

## 🔧 Step 1 — Enable Platform Access

On the NVR, navigate to:

```text id="tbvs2s"
Network > Advanced > Platform Access
```

### Enable

* Hik-Connect
* Dahua P2P
* or brand equivalent service

---

## 🆔 Step 2 — Record Device Serial Number

Locate and note the device:

```text id="tkd0tv"
Serial Number (S/N)
```

### Purpose

The serial number is required for mobile app device registration.

---

## 📱 Step 3 — Install Mobile Application

Download and install the vendor application on:

* iOS
* Android

### Common Applications

| Brand         | Mobile App       |
| ------------- | ---------------- |
| Hikvision     | Hik-Connect      |
| Dahua         | DMSS             |
| Other Vendors | Brand equivalent |

---

## 👤 Step 4 — Create User Account

Create an account within the mobile application.

### Requirements

* Valid email address
* Strong password

### Security Recommendation

Enable:

```text id="1zt9d6"
Two-Factor Authentication (2FA)
```

for enhanced account security.

---

## ➕ Step 5 — Add Device to Mobile App

Within the mobile app:

```text id="8nv7u2"
Add Device > Scan QR Code
```

### Alternative Method

* Manually enter the device Serial Number (S/N)

### QR Code Source

* Displayed on the NVR screen
* or printed on device label

---

## 🔐 Step 6 — Enter Verification Code

Enter the device verification code printed on the NVR label.

### Result

The device should successfully register within the app.

---

## 📡 Step 7 — Verify Remote Access

Test the following functions remotely:

* Live View
* Playback
* PTZ Control (if supported)

### Important Test Procedure

Disable Wi-Fi on the mobile device to ensure testing occurs over:

```text id="5qxy7s"
Mobile Data (4G/5G)
```

This confirms successful external remote access.

---

# Method B — DDNS + Port Forwarding Setup

## 🌍 Overview

DDNS allows remote access when using a dynamic public IP address from the ISP.

---

## 🌐 Step 1 — Register DDNS Domain

Register a DDNS hostname using one of the following providers:

| Provider | Example          |
| -------- | ---------------- |
| HiDDNS   | Hikvision        |
| NO-IP    | Third-party DDNS |
| DynDNS   | Third-party DDNS |

### Record

Your assigned DDNS hostname.

---

## ⚙️ Step 2 — Configure DDNS on NVR

Navigate to:

```text id="4w2c8n"
Network > DDNS
```

### Configure

* Enable DDNS
* Select provider
* Enter hostname
* Enter account credentials

### Final Step

Save configuration settings.

---

## 🔀 Step 3 — Configure Port Forwarding

On the router or firewall, configure port forwarding rules.

### Required Rule

| External Port | Protocol | Destination |
| ------------- | -------- | ----------- |
| 8000          | TCP/UDP  | NVR LAN IP  |

### Purpose

Provides remote device communication access.

---

## 🎥 Step 4 — Forward Additional Ports

Forward the following ports for remote access services.

| Service     | Default Port |
| ----------- | ------------ |
| HTTP        | 80           |
| Custom HTTP | 8080         |
| RTSP        | 554          |

### Purpose

* Web access
* Video streaming
* Remote playback

---

## 🌐 Step 5 — Verify DDNS Resolution

Open a web browser and test the DDNS hostname.

### Example

```text id="j8nv61"
http://yourhostname.ddns.net:8080
```

### Expected Result

The NVR login page should appear.

---

## 📲 Step 6 — Add Device Using DDNS

Add the device to the mobile app using:

```text id="l8d7gv"
DDNS Hostname
```

instead of the device Serial Number.

### Purpose

Provides direct remote access without vendor P2P cloud services.

---

# ⚠️ Important Warnings

## 🚫 Avoid Exposing HTTP Directly

Never expose:

```text id="8mx72s"
Port 80 (HTTP)
```

directly to the internet without:

* HTTPS encryption
* Firewall protection rules

### Risk

HTTP services are frequently scanned and exploited by attackers.

---

## 🔑 Change Default Passwords

Always change:

* Default NVR passwords
* Default camera passwords

before enabling remote access.

---

## 🚫 Disable UPnP

Disable:

```text id="v3y4wy"
UPnP (Universal Plug and Play)
```

on:

* NVR
* Router

### Reason

UPnP may automatically open internet-facing ports without administrator awareness.

---

## 🛡 Use VPN for Enterprise Deployments

For enterprise environments:

```text id="f34vyn"
Use VPN instead of direct port forwarding
```

### Benefit

Significantly improved security and encrypted remote access.

---

# ✅ Best Practice Tips

## 👥 Use Role-Based Accounts

Create user accounts with minimum required permissions.

### Example

Operators should:

* View footage
* Access playback

Operators should NOT:

* Modify configuration settings

---

## 📶 Test Using Mobile Data

Always test remote viewing over:

* 4G
* 5G

### Reason

Testing only on local Wi-Fi does not confirm internet accessibility.

---

## 📝 Document Configuration Details

Record the following information in the client handover documentation:

* DDNS hostname
* Port numbers
* App login information
* Verification codes
* User permissions

---

## 🔔 Enable Push Notifications

Enable push notifications within the mobile application for:

* Motion detection alerts
* Intrusion alarms
* Event notifications

### Benefit

Provides real-time security event awareness for clients.

---

# 🛠 Recommended Security Checklist

| Security Item               | Status |
| --------------------------- | ------ |
| Default passwords changed   | ☐      |
| HTTPS enabled               | ☐      |
| UPnP disabled               | ☐      |
| 2FA enabled                 | ☐      |
| VPN configured (enterprise) | ☐      |
| DDNS documented             | ☐      |
| Mobile access tested        | ☐      |
| User permissions restricted | ☐      |

---

# 📌 Summary

This guide covers the secure configuration of remote CCTV system access using:

* P2P cloud connectivity
* DDNS and port forwarding
* Mobile applications
* VPN security methods

The procedures outlined ensure:

* Secure remote surveillance access
* Reliable mobile connectivity
* Proper network security practices
* Safe deployment of internet-accessible CCTV systems
* Improved client usability and monitoring capabilities

  ---
