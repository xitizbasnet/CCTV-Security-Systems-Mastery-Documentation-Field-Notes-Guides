# Cabling & Power Infrastructure for CCTV Systems

## 📘 Objective

Plan and execute structured cabling for a CCTV system, configure PoE switch budgets, set up power protection (UPS), and verify end-to-end connectivity.

---

# 📡 Cabling Standards

| Cable Type       | Usage                           | Maximum Run | Notes                                 |
| ---------------- | ------------------------------- | ----------- | ------------------------------------- |
| **CAT6 UTP**     | IP cameras, NVR LAN             | 100 m max   | Use shielded (STP) near EMI sources   |
| **CAT6A STP**    | High-speed backbone             | 100 m max   | Supports 10 Gbps backbone links       |
| **RG59 Coaxial** | Analog HDTVI/AHD/CVI            | 500 m max   | 75-ohm impedance                      |
| **RG6 Coaxial**  | Long-run analog                 | 700 m max   | Thicker cable with better attenuation |
| **2-core 18AWG** | 12V DC power for analog cameras | 50 m max    | Increase wire size for longer runs    |

---

# Structured Cabling Installation

## 🔧 Step 1 — Install Conduit

Install conduit (PVC or galvanized metal) along planned routes before pulling cable.

### Notes

* Ensure conduit paths are clean and unobstructed.
* Use appropriate conduit type based on environmental conditions.

---

## 🔧 Step 2 — Pull CAT6 Cable

Pull CAT6 cable through conduit using fish tape.

### Important

* Avoid sharp bends.
* Maintain minimum bend radius:

(min bend radius = 4x cable
diameter)


---

## 🔧 Step 3 — Cable Termination

Terminate cables as follows:

### Camera End

* Use **RJ45 connectors**
* Follow **T568B wiring standard**

### Equipment Room

* Terminate into the **patch panel**
* Label each port clearly for identification

### Recommended Label Format

```text
CAM-01
CAM-02
NVR-UPLINK
```

---

## 🔧 Step 4 — Cable Testing

Test every cable run using a cable certifier such as:

* Fluke CableAnalyzer

### Verify the Following

* Opens
* Shorts
* Crossed pairs
* Attenuation issues

---

## 🔧 Step 5 — EMI Protection

Route network cables at least **300 mm away** from 240V AC power cables to prevent electromagnetic interference (EMI).

### Best Practice

* Cross power cables at 90° angles where unavoidable.

---

## 🔧 Step 6 — Cable Management

Use cable ties every **300 mm** in cable trays.

### Warning

Do not overtighten cable ties, as this may deform cable geometry and reduce performance.

---

# PoE Switch Configuration

## ⚡ Step 1 — Calculate Total PoE Budget

Calculate total power requirements by summing all camera power draws.

### Example Calculation

(16 cameras x 15W = 240W)

### Recommendation

Choose a PoE switch rated for:

```text
370W or higher total PoE budget
```

---

## ⚡ Step 2 — Connect PoE Switch to NVR

Connect the PoE switch to the NVR using:

* 1 Gbps uplink
* or 10 Gbps SFP+ uplink

---

## ⚡ Step 3 — Connect IP Cameras

Connect each IP camera to a PoE port using the terminated CAT6 cable.

---

## ⚡ Step 4 — Access Switch Management Interface

Log into the switch management interface.

### Default IP Address

```text
192.168.0.1
```

### Tasks

* Enable PoE on required ports
* Verify port link status

---

## ⚡ Step 5 — Configure PoE Power Limits

Set PoE power limits per port to prevent overload.

### Example Settings

| Camera Type         | Recommended Power Limit |
| ------------------- | ----------------------- |
| PoE+ Camera         | 25.5W                   |
| Standard PoE Camera | 15W                     |

---

## ⚡ Step 6 — Configure Port Priority

Enable PoE port priority.

### Set the Following as `CRITICAL`

* NVR uplink port
* Critical camera ports

---

## ⚡ Step 7 — Monitor PoE Consumption

Monitor PoE power usage from the switch dashboard.

### Recommendation

Keep total PoE usage below:

[
80% of rated switch budget
]

---

# UPS & Power Protection

## 🔋 Step 1 — Calculate Total Load

### Example Load Calculation

| Device     | Power Consumption |
| ---------- | ----------------- |
| NVR        | 50W               |
| PoE Switch | 370W              |
| Monitor    | 30W               |

### Total Load

[
50W + 370W + 30W = 450W
]

---

## 🔋 Step 2 — Select UPS Capacity

Calculate required UPS VA rating using:

VA rating: Load(W) / Power Factor (0.7) = 450/0.7 = 643VA minimum.

### Recommendation

Choose:

```text
1000VA UPS minimum
```

for additional safety margin.

---

## 🔋 Step 3 — Connect Equipment to UPS

Connect the following devices to UPS protected outlets:

* NVR
* PoE Switch
* Monitor

---

## 🔋 Step 4 — Configure UPS Shutdown Timer

Configure automatic shutdown settings.

### Recommended Setting

* Safely shut down the NVR after:

```text
10 minutes of power failure
```

---

## 🔋 Step 5 — Test UPS Functionality

Simulate a power outage by disconnecting mains power.

### Verify

* All systems remain operational on battery power
* UPS runtime is sufficient

---

## 🔋 Step 6 — Enable UPS Monitoring

Connect the UPS management port to:

* NVR
* or Monitoring PC

### Connection Methods

* USB
* Network interface

### Purpose

* Runtime monitoring
* Event logging
* Automated shutdown management

---

# ✅ Best Practice Tips

* Always buy a PoE switch with at least 30% headroom above your calculated PoE budget —
headroom protects against camera startup surge currents.
* Run separate conduit for CCTV cabling — never mix with phone, PA, or access control in the same
conduit.
* Label both ends of every cable immediately during installation using a label printer — saves significant
time during faults.
* Use surge protectors or SPDs (Surge Protection Devices) on outdoor camera cable runs — lightning
can travel along cables.
* Test the UPS battery under load every 6 months — UPS batteries degrade silently.
* For runs over 90 m, use a PoE extender or media converter (CAT6 to fibre) rather than boosters.

---



# 🛠 Recommended Tools & Equipment

| Tool                | Purpose                     |
| ------------------- | --------------------------- |
| Fish Tape           | Cable pulling               |
| Fluke CableAnalyzer | Cable certification         |
| RJ45 Crimping Tool  | Cable termination           |
| Cable Tester        | Connectivity testing        |
| UPS System          | Power backup                |
| Managed PoE Switch  | Camera power and networking |

---

# 📌 Summary

It covers the implementation of structured cabling and power infrastructure for CCTV systems, including:

* Structured cable installation
* Cable testing and labeling
* PoE switch configuration
* Power budgeting
* UPS sizing and deployment
* End-to-end connectivity verification

The procedures outlined ensure reliable CCTV network performance, power redundancy, and maintainable infrastructure deployment.
