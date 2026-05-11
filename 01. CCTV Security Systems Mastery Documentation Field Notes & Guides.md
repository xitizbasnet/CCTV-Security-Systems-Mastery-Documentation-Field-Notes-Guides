# CCTV Infrastructure & Network Surveillance Documentation

> **From Installation to Enterprise Integration**

---

## 📘 Document Information

| Item           | Details                                                                       |
| -------------- | ----------------------------------------------------------------------------- |
| Document Title | CCTV Technician                                                               |
| Format         | Enterprise IT Training Manual                                                 |
| Audience       | CCTV Technicians, IT Infrastructure Teams                                     |
| Scope          | Installation, Configuration, Security, Monitoring, and Enterprise Integration |

---

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
