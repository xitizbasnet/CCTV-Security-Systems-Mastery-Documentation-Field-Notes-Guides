# CCTV TECHNICIAN & NETWORK ENGINEER

> **From Installation to Enterprise Integration**

---

## 📘 Document Information

| Item           | Details                                                                       |
| -------------- | ----------------------------------------------------------------------------- |
| Document Title | CCTV Technician & Network Engineer                               |
| Edition        | 2025 Professional Training Series                                             |
| Classification | Confidential — For Training Use Only                                          |
| Format         | Enterprise IT Training Manual                                                 |
| Audience       | CCTV Technicians, Network Engineers, IT Infrastructure Teams                  |
| Scope          | Installation, Configuration, Security, Monitoring, and Enterprise Integration |

---

# Table of Contents

# SECTION A — CCTV TECHNICIAN LABS

1. Lab 01 — Site Survey & Camera Placement Planning
2. Lab 02 — Camera Hardware Installation (IP & Analog)
3. Lab 03 — DVR/NVR Setup & Configuration
4. Lab 04 — Cabling, PoE & Power Management
5. Lab 05 — Camera Image Tuning & Advanced Settings
6. Lab 06 — Remote Viewing & Mobile App Setup
7. Lab 07 — CCTV System Troubleshooting & Maintenance

# SECTION B — NETWORK ENGINEER LABS

8. Lab 08 — Network Design & IP Addressing Plan
9. Lab 09 — Switch Configuration — VLANs & Trunking
10. Lab 10 — Router Configuration & Routing Protocols
11. Lab 11 — Firewall Setup & Security Policies
12. Lab 12 — Wireless Network (Wi-Fi) Deployment
13. Lab 13 — Network Monitoring & Performance Tuning
14. Lab 14 — Integrating CCTV Network with Corporate LAN

---

# SECTION A — CCTV TECHNICIAN LABS

---

# 🎥 CCTV TECHNICIAN — LAB 01

# Site Survey & Camera Placement Planning

## 🎯 Objective

Conduct a professional site survey to identify optimal camera positions, coverage zones, power sources, cable routes, and environmental constraints before any physical installation begins.

---

## 🧰 Tools & Equipment Required

| Item                                  | Purpose              |
| ------------------------------------- | -------------------- |
| Measuring tape / laser distance meter | Physical distances   |
| Site floor plan / CAD drawing         | Layout mapping       |
| Camera angle calculator app           | FOV planning         |
| Notepad / tablet                      | Documentation        |
| Flashlight & ladder                   | Dark/elevated areas  |
| Network cable tester                  | Existing cable check |

---

## 🛠️ Step-by-Step Procedure

### Step 1

Obtain or sketch a floor plan of the premises (indoor + outdoor areas).

### Step 2

Walk the entire site with the client/security manager. Note:

* Entry/exit points
* Blind spots
* High-risk zones:

  * Cash counters
  * Server rooms
  * Parking areas

### Step 3

Mark proposed camera locations on the floor plan with a unique ID:

* `CAM-01`
* `CAM-02`
* etc.

### Step 4

Measure distances from each camera position to the NVR/DVR room:

* Record cable run length
* Add 10% slack

### Step 5

Identify power sources:

* Nearest power outlets
* PoE switch locations
* UPS availability

### Step 6

Check lighting conditions at each location:

* Day/night variances
* Backlight issues
* Window glare

### Step 7

Determine the camera type needed for each point:

* Fixed
* PTZ
* Fisheye
* Bullet
* Dome

### Step 8

Identify cable routing paths:

* Through conduits
* Above false ceilings
* Along walls

⚠️ Avoid electrical conduits (EMI risk).

### Step 9

Document environmental hazards:

* Moisture
* Dust
* Temperature extremes
* Vibration

### Step 10

Create a final **Camera Placement Report** including:

* CAM ID
* Camera type
* Resolution
* Angle
* Cable length
* Power source

---

## 📐 Camera Coverage Zone Calculation

| Zone             | Camera Type            | Range   | Notes                        |
| ---------------- | ---------------------- | ------- | ---------------------------- |
| Entrance/Exit    | Wide-angle dome (2MP+) | 3–5 m   | Faces inside, captures faces |
| Corridor         | Bullet / vandal dome   | 15–30 m | Long narrow FOV              |
| Parking Lot      | PTZ or IR bullet       | 30–60 m | Night vision essential       |
| Server/Cash Room | Fixed IP, 4K           | 2–4 m   | Full-room coverage           |
| Perimeter        | IR bullet (60m)        | 20–40 m | Night IR, weather-proof      |

---

## ✅ Best Practice Tips

* Always plan for **10–15% more cameras** than the minimum.
* Use camera FOV simulator tools:

  * JVSG
  * IP Video System Design Tool
* Avoid placing cameras directly facing sunlight or strong backlight.
* Use WDR cameras where unavoidable.
* Route cables at least **300 mm away** from high-voltage wiring.
* Obtain written client approval before purchasing hardware.
* Document everything with before/after photos.

---

# 🎥 CCTV TECHNICIAN — LAB 02

# Camera Hardware Installation (IP & Analog)

## 🎯 Objective

Physically install IP and analog cameras securely at planned positions, ensuring correct bracket mounting, proper cable termination, and weatherproofing where required.

---

## 🧰 Tools Required

| Tool                              | Use                             |
| --------------------------------- | ------------------------------- |
| Drill + bits (concrete/wood)      | Mounting holes                  |
| Screwdriver set (flat + Phillips) | Bracket fastening               |
| RJ45 crimp tool + plugs           | IP camera cabling               |
| BNC crimp tool + connectors       | Analog cabling                  |
| Cable stripper & cutter           | Termination                     |
| Fish tape / cable puller          | Threading cables                |
| Spirit level                      | Levelling cameras               |
| Silicone sealant                  | Weatherproofing outdoor cameras |

---

# Part A — IP Camera Installation

## 🛠️ Installation Steps

### Step 1

Unbox camera and verify the model matches the placement plan (`CAM ID`). Check warranty seal.

### Step 2

Attach the mounting bracket using appropriate anchors:

* Rawl plugs for concrete
* Wood screws for timber

Use a spirit level.

### Step 3

Thread CAT6 cable through conduit/ceiling. Leave:

* `300 mm` slack at the camera end

### Step 4

Terminate CAT6 using:

* RJ45 plug
* T568B wiring standard

Test using a cable tester.

### Step 5

For outdoor cameras:

* Apply silicone sealant
* Create drip loop for water protection

### Step 6

Connect RJ45 to PoE port.

The camera powers on via PoE switch.

### Step 7

Adjust:

* Pan
* Tilt
* Zoom

Match planned FOV.

### Step 8

Label camera with waterproof CAM ID labels at:

* Camera side
* NVR side

---

# Part B — Analog (HDTVI/AHD/CVI) Camera Installation

## 🛠️ Installation Steps

### Step 1

Mount bracket and route:

* RG59 coaxial cable
* 2-core power cable

### Step 2

Prepare RG59 cable:

* 15 mm outer jacket
* Fold back braid
* Strip 8 mm dielectric
* Expose 5 mm center conductor

### Step 3

Attach BNC connector:

* Twist-on
* Crimp type

### Step 4

Connect DC power:

* Red = +12V
* Black = GND

### Step 5

Connect:

* BNC to VIDEO OUT
* DC connector to DC IN

### Step 6

Adjust image:

* Zoom first
* Focus second

---

## 📊 Camera Cabling Reference

| Camera Type    | Cable Type   | Power          | Notes                          |
| -------------- | ------------ | -------------- | ------------------------------ |
| IP Camera      | CAT5e/CAT6   | PoE or 12V DC  | Up to 100 m per run            |
| Analog HD      | RG59 Coaxial | 12V DC         | Up to 500 m (HDTVI)            |
| Fisheye/PTZ    | CAT6 (IP)    | PoE+ (30W)     | Check PoE budget               |
| Thermal Camera | CAT6 + RS485 | 24V AC or PoE+ | Separate RS485 for PTZ control |

---

## ✅ Best Practice Tips

* Use T568B wiring consistently.
* Prefer CAT6 over CAT5e for 4K cameras.
* Apply silicone protection even on IP66/IP67 cameras.
* Tighten brackets fully to avoid vibration blur.
* Label all cable ends immediately.
* Never exceed 90 m on CAT6 runs.

---

# 🎥 CCTV TECHNICIAN — LAB 03

# DVR / NVR Setup & Configuration

## 🎯 Objective

Install, initialise, and configure an NVR or DVR including:

* HDD formatting
* Channel assignment
* Recording schedules
* User management

---

## 📘 NVR vs DVR — Quick Reference

| Feature        | NVR                   | DVR                        |
| -------------- | --------------------- | -------------------------- |
| Input Type     | IP Cameras (RJ45)     | Analog Cameras (BNC)       |
| Video Encoding | H.265 / H.264         | H.265 / H.264 (HD-TVI/AHD) |
| Resolution     | Up to 32MP (8K ready) | Up to 8MP (4K-TVI)         |
| Cable          | CAT6 UTP              | RG59 Coaxial               |
| PoE Built-in   | Yes (most models)     | No                         |
| Scalability    | Highly scalable       | Fixed channel count        |

---

## 🛠️ Step-by-Step NVR Setup

### Step 1

Rack-mount or place NVR in equipment room. Connect to UPS.

### Step 2

Install surveillance-grade HDDs:

* WD Purple
* Seagate SkyHawk

### Step 3

Connect:

* LAN port → switch
* HDMI/VGA → monitor

### Step 4

Run setup wizard:

* Admin password
* Timezone (IST: UTC+5:30)
* Date/time

### Step 5

Format HDD:

```text
Storage > HDD Management > Format
```

### Step 6

Configure recording:

```text
Storage > Schedule
```

Enable:

* Continuous recording
* Motion detection

### Step 7

Add IP cameras:

```text
Camera > IP Camera > Add
```

### Step 8

For non-PoE cameras:

* Enter IP
* Username
* Password
* RTSP URL

### Step 9

Set:

* Resolution
* FPS

Recommended:

* 1080P / 15fps
* 25fps for critical areas

### Step 10

Enable overwrite when HDD full.

### Step 11

Configure motion detection zones.

### Step 12

Create users:

* Admin
* Operator
* Guest

### Step 13

Enable:

* Email alerts
* Push notifications

### Step 14

Verify playback functionality.

---

## 💾 HDD Capacity Planning

| Resolution    | FPS    | Storage/Day        | Use Case            |
| ------------- | ------ | ------------------ | ------------------- |
| 1080P / H.265 | 15 fps | ~40 GB/day/camera  | Standard office     |
| 1080P / H.265 | 25 fps | ~65 GB/day/camera  | High motion areas   |
| 4K / H.265    | 15 fps | ~120 GB/day/camera | Critical zones      |
| 4K / H.265+   | 25 fps | ~160 GB/day/camera | Ultra-high security |

### Formula

```text
Total HDD = Cameras × GB/day × Retention Days
```

Example:

```text
16 cameras × 40 GB × 30 days = 19.2 TB
```

---

## ✅ Best Practice Tips

* Always use surveillance-grade HDDs.
* Enable H.265+ where supported.
* Use motion recording during low traffic hours.
* Change default passwords immediately.
* Keep firmware updated.
* Securely document:

  * IP addresses
  * MAC addresses
  * Credentials

---

# 🎥 CCTV TECHNICIAN — LAB 04

# Cabling, PoE & Power Management

## 🎯 Objective

Plan and execute structured cabling, configure PoE budgets, establish UPS protection, and verify connectivity.

---

## 📘 Cabling Standards

| Cable Type   | Usage           | Max Run | Notes                         |
| ------------ | --------------- | ------- | ----------------------------- |
| CAT6 UTP     | IP cameras, LAN | 100 m   | Use STP near EMI              |
| CAT6A STP    | Backbone        | 100 m   | 10 Gbps                       |
| RG59 Coaxial | Analog HDTVI    | 500 m   | 75-ohm impedance              |
| RG6 Coaxial  | Long-run analog | 700 m   | Better attenuation            |
| 2-core 18AWG | 12V DC power    | 50 m    | Increase size for longer runs |

---

# Part A — Structured Cabling Installation

### Step 1

Install conduit:

* PVC
* Galvanized metal

### Step 2

Pull CAT6 cable using fish tape.

⚠️ Avoid sharp bends.

### Step 3

Terminate:

* RJ45 (camera side)
* Patch panel (equipment room)

### Step 4

Test using:

* Fluke CableAnalyzer

### Step 5

Maintain 300 mm separation from AC power cables.

### Step 6

Secure with cable ties every 300 mm.

---

# Part B — PoE Switch Configuration

### Step 1

Calculate PoE budget.

Example:

```text
16 cameras × 15W = 240W
```

### Step 2

Connect switch uplink to NVR.

### Step 3

Connect IP cameras.

### Step 4

Enable PoE per port.

### Step 5

Set PoE power limits.

### Step 6

Set critical port priorities.

### Step 7

Monitor total power usage.

---

# Part C — UPS & Power Protection

### Step 1

Calculate load:

```text
NVR (50W) + Switch (370W) + Monitor (30W)
= 450W
```

### Step 2

UPS sizing:

```text
450 / 0.7 = 643VA
```

Recommended:

```text
1000VA UPS
```

### Step 3

Connect critical devices to UPS.

### Step 4

Configure shutdown timers.

### Step 5

Perform live UPS test.

### Step 6

Enable runtime monitoring.

---

## ✅ Best Practice Tips

* Maintain 30% PoE headroom.
* Separate CCTV conduits from other systems.
* Label all cabling immediately.
* Install surge protection on outdoor runs.
* Test UPS batteries every 6 months.
* Use fiber/media converters for long runs.

---

# 🎥 CCTV TECHNICIAN — LAB 05

# Camera Image Tuning & Advanced Settings

## 🎯 Objective

Configure image parameters to achieve optimal video quality under different lighting conditions.

---

## 📘 Key Image Settings Reference

| Setting       | Recommended Value | Notes                            |
| ------------- | ----------------- | -------------------------------- |
| Brightness    | 50–60%            | Avoid dark/washed images         |
| Contrast      | 50–55%            | Preserve shadow details          |
| Saturation    | 50%               | Natural colors                   |
| Sharpness     | 50–70%            | Excessive sharpness causes noise |
| WDR           | Enable (2–3)      | Bright/dark scenes               |
| Day/Night     | Auto (ICR)        | Automatic IR switching           |
| White Balance | Auto              | Correct color                    |
| Shutter Speed | 1/50 – 1/100 s    | Motion blur control              |
| Gain/AGC      | Low–Medium        | Reduces noise                    |
| 3D DNR        | Medium            | Low-light enhancement            |

---

## 🛠️ Step-by-Step Image Tuning Procedure

1. Access camera web interface.
2. Navigate to:

```text
Configuration > Image > Display Settings
```

3. Set Scene Mode.
4. Adjust brightness and contrast.
5. Enable WDR where required.
6. Set Day/Night to AUTO.
7. Enable 3D-DNR.
8. Configure OSD:

   * CAM ID
   * Timestamp
9. Configure Privacy Masks.
10. Configure PTZ presets/routes.
11. Save and reboot.

---

## ✅ Best Practice Tips

* Tune cameras during worst-case lighting.
* Use WDR only when necessary.
* Use BLC for lighter backlight conditions.
* Sync timestamps with NTP.
* Verify privacy compliance regulations.
* Test IR mode manually.

---

# 🎥 CCTV TECHNICIAN — LAB 06

# Remote Viewing & Mobile App Setup

## 🎯 Objective

Configure secure remote access via:

* P2P cloud
* Static IP/DDNS
* Mobile applications

---

## 📘 Remote Access Methods Comparison

| Method           | Pros                  | Cons               |
| ---------------- | --------------------- | ------------------ |
| P2P Cloud        | Easy setup            | Vendor dependency  |
| Static Public IP | Reliable              | ISP cost           |
| DDNS             | Works with dynamic IP | Slight latency     |
| VPN              | Most secure           | Requires VPN setup |

---

# Method A — P2P Cloud Setup

### Steps

1. Enable platform access.
2. Record serial number.
3. Install vendor app:

   * Hik-Connect
   * DMSS
4. Create account with MFA.
5. Scan QR code.
6. Enter verification code.
7. Test via mobile data.

---

# Method B — DDNS + Port Forwarding

### Steps

1. Register DDNS domain.
2. Configure DDNS on NVR.
3. Configure router port forwarding:

   * 8000 TCP/UDP
   * 80 / 8080
   * 554 RTSP
4. Verify hostname resolution.
5. Add device using DDNS hostname.

---

## ⚠️ Important Warnings

* Never expose HTTP directly to the internet.
* Change default passwords immediately.
* Disable UPnP.
* Use VPNs for enterprise deployments.

---

## ✅ Best Practice Tips

* Apply least privilege user access.
* Test over mobile data.
* Document DDNS and ports.
* Enable motion notifications.

---

# 🎥 CCTV TECHNICIAN — LAB 07

# CCTV System Troubleshooting & Maintenance

## 🎯 Objective

Diagnose and resolve CCTV faults and establish preventive maintenance procedures.

---

## 📘 Common Faults & Diagnosis

| Fault               | Likely Cause        | Diagnosis Steps     |
| ------------------- | ------------------- | ------------------- |
| No image            | Cable/PoE/IP issue  | Test cable, ping IP |
| Blurry image        | Lens/focus issue    | Refocus, clean      |
| Video noise         | EMI/poor cable      | Check shielding     |
| Night vision poor   | Dirty lens/IR fault | Test IR             |
| HDD not detected    | SATA issue          | Reseat/reformat     |
| Recording gaps      | Schedule/storage    | Verify schedule     |
| Remote access fails | Port/DDNS issue     | Verify ports        |
| NVR offline         | IP conflict         | Check network       |

---

## 🛠️ Troubleshooting Workflow

1. Identify affected channels.
2. Perform physical inspection.
3. Ping camera IP.
4. Check PoE LEDs.
5. Access camera directly.
6. Review logs.
7. Tune image settings.
8. Check HDD health.
9. Verify recording schedule.
10. Document root cause and resolution.

---

## 📅 Preventive Maintenance Schedule

| Frequency | Task                               |
| --------- | ---------------------------------- |
| Weekly    | Check recording and storage        |
| Monthly   | Clean cameras and verify IR        |
| Quarterly | UPS and HDD health checks          |
| Bi-Annual | Cable and bracket inspection       |
| Annual    | Full audit and battery replacement |

---

## ✅ Best Practice Tips

* Maintain detailed service logs.
* Configure alerts for failures.
* Keep spare components available.
* Verify recordings weekly.
* Test firmware before production rollout.

---

# SECTION B — NETWORK ENGINEER LABS

---

# 🌐 NETWORK ENGINEER — LAB 08

# Network Design & IP Addressing Plan

## 🎯 Objective

Design a scalable segmented network topology and IP addressing scheme.

---

## 📘 Sample Site Topology

| Layer        | Device Role          |
| ------------ | -------------------- |
| Internet     | ISP Router / Modem   |
| Core/Edge    | Firewall             |
| Distribution | Core L3 Switch       |
| Access Layer | L2 PoE Switches      |
| Wireless     | Wireless APs         |
| CCTV Segment | Dedicated PoE Switch |

---

## 📘 VLAN Segmentation Plan

| VLAN | Name        | Subnet          | Purpose         |
| ---- | ----------- | --------------- | --------------- |
| 10   | Management  | 192.168.10.0/24 | Network devices |
| 20   | Staff LAN   | 192.168.20.0/24 | Users           |
| 30   | Guest Wi-Fi | 192.168.30.0/24 | Guests          |
| 40   | CCTV        | 192.168.40.0/24 | Cameras/NVR     |
| 50   | Servers     | 192.168.50.0/24 | Servers         |
| 60   | VoIP        | 192.168.60.0/24 | Phones          |

---

## 🛠️ Network Design Process

1. Gather requirements.
2. Choose private IP range.
3. Assign VLANs/subnets.
4. Define gateways.
5. Configure DHCP scopes.
6. Design uplinks.
7. Document all devices.
8. Create diagrams.
9. Perform peer review.

---

## ✅ Best Practice Tips

* Isolate CCTV traffic.
* Plan for 20% growth.
* Maintain IPAM documentation.
* Standardize on /24 subnets.
* Separate management VLAN.

---

# 🌐 NETWORK ENGINEER — LAB 09

# Switch Configuration — VLANs & Trunking

## 🎯 Objective

Configure VLANs, access ports, and trunk links.

---

## 📘 Prerequisites

* Cisco IOS switch
* Console cable / SSH
* IP addressing plan

---

# Part A — Basic Switch Initialisation

```bash
hostname SW-ACCESS-01

interface Vlan10
 ip address 192.168.10.11 255.255.255.0

ip default-gateway 192.168.10.1

crypto key generate rsa modulus 2048
```

---

# Part B — VLAN Creation

```bash
vlan 10
 name Management

vlan 20
 name Staff-LAN

vlan 30
 name Guest-WiFi

vlan 40
 name CCTV

vlan 50
 name Servers

vlan 60
 name VoIP
```

---

# Part C — Access Port Configuration

```bash
interface GigabitEthernet0/1
 switchport mode access
 switchport access vlan 20
 spanning-tree portfast
 no shutdown
```

---

# Part D — Trunk Port Configuration

```bash
interface GigabitEthernet0/24
 switchport mode trunk
 switchport trunk encapsulation dot1q
 switchport trunk allowed vlan 10,20,30,40,50,60
 switchport trunk native vlan 10
 no shutdown
```

---

## 🔍 Verification Commands

| Command                    | Purpose       |
| -------------------------- | ------------- |
| show vlan brief            | Verify VLANs  |
| show interfaces trunk      | Verify trunks |
| show spanning-tree vlan 40 | STP status    |
| show ip interface brief    | Verify IP     |
| ping 192.168.10.1          | Gateway test  |

---

## ✅ Best Practice Tips

* Never allow all VLANs on trunks.
* Use unused native VLANs.
* Enable PortFast only on access ports.
* Enable BPDU Guard.
* Verify VLAN assignments before production.

---

# 🌐 NETWORK ENGINEER — LAB 10

# Router Configuration & Routing Protocols

## 🎯 Objective

Configure WAN, routing, NAT/PAT, and OSPF.

---

# Part A — WAN Setup

```bash
hostname ROUTER-01
no ip domain-lookup
```

---

# Part B — NAT/PAT

```bash
access-list 1 permit 192.168.0.0 0.0.255.255

interface GigabitEthernet0/0
 ip nat outside

interface GigabitEthernet0/1
 ip nat inside

ip nat inside source list 1 interface GigabitEthernet0/0 overload
```

---

# Part C — Inter-VLAN Routing

```bash
ip routing

interface Vlan20
 ip address 192.168.20.1 255.255.255.0
 no shutdown

interface Vlan40
 ip address 192.168.40.1 255.255.255.0
 no shutdown
```

---

# Part D — OSPF

```bash
router ospf 1
 router-id 1.1.1.1
 network 192.168.10.0 0.0.0.255 area 0
 network 192.168.20.0 0.0.0.255 area 0
 network 192.168.40.0 0.0.0.255 area 0
 passive-interface GigabitEthernet0/0
```

---

## 🔍 Verification Commands

| Command                  | Purpose          |
| ------------------------ | ---------------- |
| show ip route            | Routing table    |
| show ip nat translations | NAT verification |
| show ip ospf neighbor    | OSPF adjacency   |
| ping 8.8.8.8             | Internet test    |
| traceroute 8.8.8.8       | Path analysis    |

---

## ✅ Best Practice Tips

* Set manual OSPF router IDs.
* Use passive interfaces.
* Avoid unrestricted NAT rules.
* Test from real endpoints.
* Save configurations frequently.

---

# 🌐 NETWORK ENGINEER — LAB 11

# Firewall Setup & Security Policies

## 🎯 Objective

Configure firewall policies, VLAN security, IDS/IPS, and CCTV access rules.

---

## 📘 Firewall Zones

| Zone  | Segment         | Default Policy    |
| ----- | --------------- | ----------------- |
| WAN   | Internet        | Block inbound     |
| LAN   | Staff/Servers   | Controlled access |
| CCTV  | Cameras/NVR     | Isolated          |
| DMZ   | Public services | Limited access    |
| Guest | Guest Wi-Fi     | Internet only     |

---

## 🛠️ pfSense Configuration Steps

1. Access pfSense UI.
2. Configure DNS/timezone.
3. Assign interfaces.
4. Create VLANs.
5. Configure WAN rules.
6. Configure CCTV isolation.
7. Configure Guest isolation.
8. Configure LAN rules.
9. Enable IDS/IPS.
10. Enable pfBlockerNG.
11. Test firewall rules.
12. Create aliases.

---

## ⚠️ Important Warnings

* Default deny inbound traffic.
* Never expose cameras publicly.
* Isolate guest Wi-Fi completely.
* Keep firmware updated.

---

## ✅ Best Practice Tips

* Use aliases for cleaner rules.
* Enable logging on deny rules.
* Schedule backups.
* Test using endpoint devices.

---

# 🌐 NETWORK ENGINEER — LAB 12

# Wireless Network (Wi-Fi) Deployment

## 🎯 Objective

Deploy enterprise-grade Wi-Fi with secure SSIDs and VLAN separation.

---

## 📘 Wi-Fi Planning

| Band    | Channels       | Characteristics  | Use Case           |
| ------- | -------------- | ---------------- | ------------------ |
| 2.4 GHz | 1, 6, 11       | Better range     | IoT                |
| 5 GHz   | 36–48, 149–161 | High speed       | Staff              |
| 6 GHz   | PSC            | Ultra-high speed | Dense environments |

---

## 📘 SSID Design Plan

| SSID       | Security             | Auth       | VLAN    | Users    |
| ---------- | -------------------- | ---------- | ------- | -------- |
| Corp-Staff | WPA3/WPA2-Enterprise | 802.1X     | VLAN 20 | Staff    |
| Corp-Guest | WPA2-Personal        | PSK        | VLAN 30 | Visitors |
| Corp-IoT   | WPA2-Personal        | Strong PSK | VLAN 40 | IoT/CCTV |

---

## 🛠️ Deployment Steps

1. Install UniFi Controller.
2. Mount APs properly.
3. Connect to VLAN 10.
4. Adopt APs.
5. Create SSIDs.
6. Run RF scan.
7. Adjust TX power.
8. Enable Band Steering.
9. Enable Fast Roaming.
10. Configure RADIUS.
11. Validate VLAN assignments.
12. Run coverage survey.

---

## ✅ Best Practice Tips

* Maintain 15–20% AP overlap.
* Rotate guest passwords regularly.
* Prefer WPA3.
* Isolate guest traffic.
* Disable legacy 802.11b rates.
* Avoid RF interference sources.

---

# 🌐 NETWORK ENGINEER — LAB 13

# Network Monitoring & Performance Tuning

## 🎯 Objective

Deploy monitoring systems and optimize performance using QoS and alerts.

---

## 📘 Monitoring Stack Overview

| Tool                 | Type              | Best For       | Platform     |
| -------------------- | ----------------- | -------------- | ------------ |
| PRTG                 | GUI monitoring    | SMB/Enterprise | Windows      |
| Zabbix               | Open source       | Enterprise     | Linux        |
| Grafana + Prometheus | Modern dashboards | DevOps         | Linux/Docker |
| LibreNMS             | Auto-discovery    | SMB            | Linux        |
| Nagios               | Plugin-rich       | Enterprise     | Linux        |

---

# Part A — SNMP Configuration

```bash
snmp-server community PUBLIC_READ ro
snmp-server community PRIVATE_WRITE rw
snmp-server host 192.168.50.10 version 2c PUBLIC_READ
snmp-server enable traps
snmp-server location Server-Room-Rack-A
snmp-server contact netadmin@company.com
```

---

# Part B — Zabbix Setup

1. Install Zabbix.
2. Access web UI.
3. Create hosts.
4. Add SNMP interfaces.
5. Apply templates.
6. Verify polling.
7. Configure alerts.

---

# Part C — QoS Configuration

```bash
class-map match-any VOIP-TRAFFIC
 match ip dscp ef

class-map match-any CCTV-TRAFFIC
 match ip dscp af31

policy-map WAN-QOS
 class VOIP-TRAFFIC
  priority 20000

 class CCTV-TRAFFIC
  bandwidth 50000

 class class-default
  fair-queue

interface GigabitEthernet0/0
 service-policy output WAN-QOS
```

---

## 📊 Key Metrics to Monitor

| Metric                | Threshold    |
| --------------------- | ------------ |
| CPU/Memory            | >80% warning |
| Interface Utilization | >70%         |
| Packet Loss           | >0.1%        |
| Latency               | >20ms LAN    |
| PoE Power             | >85%         |
| HDD Space             | >85%         |

---

## ✅ Best Practice Tips

* Use SNMPv3 in production.
* Set proactive alert thresholds.
* Monitor PoE budgets continuously.
* Establish performance baselines.
* Automate config backups.

---

# 🌐 NETWORK ENGINEER — LAB 14

# Integrating CCTV Network with Corporate LAN

## 🎯 Objective

Securely integrate CCTV infrastructure with the corporate LAN while maintaining isolation and controlled access.

---

## 📘 Integration Architecture

| Segment            | IP Range        | Role             |
| ------------------ | --------------- | ---------------- |
| CCTV VLAN 40       | 192.168.40.0/24 | Cameras + NVR    |
| Staff VLAN 20      | 192.168.20.0/24 | Office PCs       |
| Management VLAN 10 | 192.168.10.0/24 | Network devices  |
| Firewall           | 192.168.x.1     | Traffic control  |
| NVR                | 192.168.40.100  | Recording server |

---

## 🛠️ Integration Steps

1. Verify VLAN trunking.
2. Block staff access to CCTV VLAN.
3. Allow Security Team access to NVR.
4. Block cameras from LAN.
5. Allow NTP access.
6. Allow SMTP/push notifications.
7. Configure DHCP reservation.
8. Test authorized access.
9. Verify blocked office access.
10. Verify camera isolation.
11. Verify internet access for NVR.
12. Document all configurations.

---

## 📋 Integration Checklist

| Checklist Item                       | Done |
| ------------------------------------ | ---- |
| CCTV VLAN configured and trunked     | [ ]  |
| NVR has static IP / DHCP reservation | [ ]  |
| Office PCs blocked from CCTV         | [ ]  |
| Security team access verified        | [ ]  |
| NVR internet access verified         | [ ]  |
| NTP synchronization working          | [ ]  |
| Mobile remote access tested          | [ ]  |
| Firewall rules documented            | [ ]  |
| Client sign-off completed            | [ ]  |

---

## ✅ Best Practice Tips

* Apply least privilege access.
* Enable logging on blocked access attempts.
* Label CCTV switch ports physically.
* Conduct quarterly access reviews.
* Enforce HTTPS access only.
* Maintain compliance documentation.

---

# 🎉 Congratulations — All 14 Labs Completed!

You have successfully covered the complete lifecycle of:

```text
Site Survey
→ Installation
→ Configuration
→ Integration
→ Monitoring
→ Security
```

---

# 📌 Training Outcome Summary

After completing this lab guide, technicians and engineers should be able to:

* Design enterprise CCTV infrastructure
* Deploy structured network environments
* Configure VLANs, routing, and firewalls
* Securely integrate surveillance systems
* Implement monitoring and maintenance processes
* Apply enterprise-grade best practices

---

# 🔒 Confidentiality Notice

> This document is classified as:
>
> **Confidential — For Training Use Only**
>
> Distribution outside authorized training or operational environments is prohibited without approval.

---
