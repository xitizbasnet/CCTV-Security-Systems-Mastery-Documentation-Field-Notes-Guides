# CCTV System Troubleshooting & Maintenance

## 📘 Objective

Diagnose and resolve common CCTV system faults including:

* No-signal cameras
* Poor image quality
* HDD failures
* Network connectivity issues

Establish a preventive maintenance schedule to ensure long-term system reliability and operational performance.

---

# 🛠 Common Faults & Diagnosis

| Fault                           | Likely Cause                                        | Diagnosis Steps                                    |
| ------------------------------- | --------------------------------------------------- | -------------------------------------------------- |
| **No image / black screen**     | Cable break, PoE fault, incorrect IP configuration  | Test cable, check PoE LED, ping camera IP          |
| **Blurry / out-of-focus image** | Varifocal lens not adjusted, dirty lens             | Re-focus lens; clean using lens cloth              |
| **Video noise / artefacts**     | EMI, poor cable quality, excessive cable run length | Re-route cable, inspect shielding                  |
| **Poor night vision**           | Faulty IR LEDs, dirty lens, AGC gain too low        | Clean lens, test IR output, increase AGC           |
| **HDD not detected**            | Loose SATA cable, incorrect HDD format              | Reseat HDD, reformat within NVR menu               |
| **Recording gaps**              | Motion detection misconfiguration, HDD full         | Check recording schedule, verify storage usage     |
| **Remote access failure**       | Port forwarding issue, DDNS not updated             | Verify router ports, confirm DDNS hostname         |
| **NVR offline alerts**          | IP conflict, network switch issue                   | Verify IP configuration, test with direct PC cable |

---

# 🔍 Troubleshooting Workflow

## 🔎 Step 1 — Identify Affected Cameras

Check the NVR channel view and identify which channels display faults.

### Verify

* Offline channels
* Black screens
* Missing recordings
* Distorted images

---

## 🔌 Step 2 — Perform Physical Inspection

Verify the following:

* Camera power LED is ON
* Cable connections are secure at both ends
* No visible cable damage exists

### Inspection Points

* Camera connection
* Patch panel
* PoE switch
* NVR ports

---

## 🌐 Step 3 — Test Network Connectivity

For IP cameras:

Ping the camera IP address from:

* NVR
* PC on the same network

### Result Interpretation

| Result         | Meaning                          |
| -------------- | -------------------------------- |
| Reply received | Camera reachable                 |
| No reply       | IP or network connectivity issue |

### Example Command

```bash
ping 192.168.1.64
```

---

## ⚡ Step 4 — Check PoE Switch Status

Inspect the PoE switch port LED indicators.

| LED Status | Meaning                  |
| ---------- | ------------------------ |
| Green      | Active network link      |
| Amber      | No link / fault detected |

### Action

Replace the cable if the port shows amber or unstable status.

---

## 🌍 Step 5 — Access Camera Web Interface

Open a browser and enter the camera IP address directly.

### Purpose

Determine whether the issue is:

* Camera-related
* or NVR communication-related

### If Accessible

The issue likely involves:

* NVR configuration
* ONVIF settings
* Stream compatibility
* Authentication mismatch

---

## 📜 Step 6 — Review NVR System Logs

Navigate to:

```text id="rw4d0g"
System > Log
```

### Tasks

* Filter by error type
* Identify fault timestamps
* Review event descriptions

### Common Errors

* Camera offline
* HDD error
* Network timeout
* Authentication failure

---

## 🎥 Step 7 — Troubleshoot Image Quality

For image quality issues:

* Run Auto-Adjust
* or manually tune image parameters

### Check

* Focus
* Brightness
* Contrast
* WDR
* IR settings

---

## 💽 Step 8 — Check HDD Health

Navigate to:

```text id="5n2f72"
Storage > HDD Info
```

### Verify

* HDD status
* Capacity usage
* SMART health data

### Important

Replace any HDD displaying:

```text id="0u7f8k"
BAD Status
```

---

## ⏺ Step 9 — Verify Recording Schedule

Navigate to:

```text id="7sn7xg"
Storage > Recording Schedule
```

### Confirm

* All channels are enabled
* Full 24-hour recording coverage exists
* Motion schedules are configured correctly

---

## 📝 Step 10 — Document Repairs

After completing repairs, record:

* Fault description
* Root cause
* Corrective action taken
* Date and technician information

### Purpose

Maintain accurate maintenance history and support warranty claims.

---

# 📅 Preventive Maintenance Schedule

| Frequency     | Task                                                                                     |
| ------------- | ---------------------------------------------------------------------------------------- |
| **Weekly**    | Check NVR recording status, storage space, and system alerts                             |
| **Monthly**   | Clean camera lenses and housings. Verify night vision operation on all cameras           |
| **Quarterly** | Test UPS battery backup. Check HDD health (SMART data). Review firmware                  |
| **Bi-Annual** | Full cable inspection. Re-tighten bracket bolts. Test all motion detection zones         |
| **Annual**    | Replace UPS battery if runtime has degraded. Perform full system audit and client report |

---

# 🧰 Recommended Troubleshooting Toolkit

| Tool              | Purpose                        |
| ----------------- | ------------------------------ |
| RJ45 Cable Tester | Cable continuity testing       |
| Multimeter        | Voltage and power verification |
| Laptop/PC         | Network diagnostics            |
| Spare Patch Cable | Rapid cable replacement        |
| Lens Cleaning Kit | Camera maintenance             |
| PoE Tester        | PoE verification               |
| USB Flash Drive   | Firmware updates and backups   |

---

# ⚠️ Important Maintenance Notes

## 🔒 Maintain Documentation

Keep a maintenance log for every site.

### Record

* Service visits
* Faults identified
* Corrective actions
* Hardware replacements

### Benefit

Essential for:

* Warranty claims
* Service history
* Troubleshooting trends

---

## 🔔 Configure System Alerts

Enable:

* Email alerts
* Push notifications

### Recommended Alerts

* HDD failure
* Camera offline
* Storage full
* Network disconnect

### Benefit

Identify issues before clients report them.

---

## 🧳 Maintain Spare Parts Kit

Recommended onsite spare parts:

| Item             | Quantity |
| ---------------- | -------- |
| RJ45 plugs       | 2x       |
| Patch cable (5m) | 1x       |
| Spare PoE camera | 1x       |

### Purpose

Reduce downtime during emergency replacements.

---

## 📹 Verify Recording Playback Weekly

Regularly verify recordings from the client side.

### Reason

Many recording failures go unnoticed until footage is urgently required.

### Verify

* Playback functionality
* Recording continuity
* Timestamp accuracy
* Motion recording triggers

---

# ✅ Best Practice Tips

* Always troubleshoot physical layer issues first before changing software settings.
* Label all cables and ports clearly to reduce troubleshooting time.
* Maintain firmware updates for cameras, switches, and NVR systems.
* Use surveillance-grade HDDs designed for continuous recording workloads.
* Ensure UPS battery backup is tested regularly.
* Maintain environmental protection for outdoor cameras and enclosures.

---

# 📋 Maintenance Log Template

```text id="8cw1uh"
Date:
Site Name:
Technician:
Issue Reported:
Root Cause:
Corrective Action:
Parts Replaced:
System Tested:
Client Sign-Off:
```

---

# 📌 Summary

This guide provides a structured approach for troubleshooting and maintaining CCTV systems.

The procedures cover:

* Camera faults
* Network issues
* PoE troubleshooting
* HDD diagnostics
* Recording failures
* Preventive maintenance planning

Following these practices ensures:

* Reduced downtime
* Improved system reliability
* Faster fault resolution
* Better evidence retention
* Long-term operational stability of CCTV deployments

---
