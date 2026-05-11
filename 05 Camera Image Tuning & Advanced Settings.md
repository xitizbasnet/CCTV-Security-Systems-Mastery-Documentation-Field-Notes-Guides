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

# 📷 Step-by-Step Image Tuning Procedure

## 🔐 Step 1 — Access Camera Web Interface

Open a web browser and enter the camera IP address.

### Example

```text
192.168.1.64
```

### Login Requirements

* Username: Admin account
* Password: Administrator credentials

### Purpose

Access the camera management interface for configuration and tuning.

---

## ⚙️ Step 2 — Navigate to Image Settings

Navigate to the following menu path:

```text
Configuration > Image > Display Settings
```

### Available Controls

* Brightness
* Contrast
* Saturation
* WDR
* Day/Night mode
* Noise reduction

---

## 🌐 Step 3 — Configure Scene Mode

Select the appropriate scene mode based on the camera environment.

| Scene Mode | Recommended Environment            |
| ---------- | ---------------------------------- |
| Indoor     | Offices, hallways, reception areas |
| Outdoor    | Parking lots, building exteriors   |
| Low Light  | Warehouses, storage rooms          |
| Custom     | Advanced/manual tuning             |

### Recommendation

Use predefined scene profiles whenever possible for faster deployment.

---

## 🎚 Step 4 — Adjust Brightness & Contrast

Adjust brightness and contrast while monitoring the live camera feed.

### Goal

Achieve:

* Clear shadow detail
* Balanced highlights
* Natural image exposure

### Best Practice

Avoid:

* Overexposed bright areas
* Excessive darkness
* Washed-out colors

---

## 🌞 Step 5 — Enable WDR (Wide Dynamic Range)

Enable WDR for cameras facing:

* Entrances
* Windows
* Bright outdoor areas

### Recommended Initial Setting

```text
Level 2–3
```

### Purpose

Improves visibility in scenes containing both very bright and very dark areas.

---

## 🌙 Step 6 — Configure Day/Night Mode

Set Day/Night mode to:

```text
AUTO (ICR)
```

### Function

The camera automatically switches to:

* Day mode during daylight
* IR night vision at dusk or low-light conditions

### Benefit

Ensures continuous 24/7 image clarity.

---

## 🧠 Step 7 — Enable 3D-DNR (Digital Noise Reduction)

Enable:

```text
3D-DNR
```

### Purpose

Reduces:

* Graininess
* Low-light image noise

### Benefit

Maintains image clarity without excessive motion blur.

---

## 🏷 Step 8 — Configure OSD (On-Screen Display)

Navigate to:

```text
Camera > OSD
```

### Enable the Following

* Camera name
* Timestamp

### Naming Recommendation

Use the assigned CAM ID.

### Positioning

Place OSD elements in a screen corner to avoid obstructing important video content.

---

## 🔒 Step 9 — Configure Privacy Masks

Navigate to:

```text
Camera > Privacy Mask
```

### Task

Draw privacy mask zones over areas that must not be recorded.

### Example Areas

* Neighbouring property
* Public windows
* Restricted/private spaces

### Purpose

Ensure legal and privacy compliance.

---

## 🎥 Step 10 — Configure PTZ Settings

For PTZ cameras, configure the following under:

```text
PTZ Configuration
```

### Configure

* Presets
* Patrol routes
* Home position

### Purpose

Enable automated monitoring coverage and rapid camera positioning.

---

## 💾 Step 11 — Save & Reboot

Save all configuration settings and reboot the camera.

### Verification

Review recording quality from the NVR during:

* Daytime
* Nighttime
* Variable lighting conditions

---

# ✅ Best Practice Tips

## 📌 Lighting Optimization

* Always tune camera settings during the worst lighting condition for that zone.

### Example

Tune entrance cameras during bright noon conditions to optimize high-contrast scenes.

---

## 📌 WDR Usage

* Enable WDR only where required.
* WDR slightly reduces frame rate and increases processing load.

### Recommendation

Use WDR selectively for high-contrast environments only.

---

## 📌 Backlight Compensation (BLC)

* BLC is suitable for less extreme lighting conditions than WDR.
* BLC has lower performance overhead.

### Use Case

Ideal for:

* Indoor entrances
* Moderately backlit environments

---

## 📌 Time Synchronization

Set the OSD timestamp to synchronize using:

```text
NTP (Network Time Protocol)
```

### Reason

Manual clocks drift over time and may create evidentiary issues with recorded footage.

---

## 📌 Privacy Compliance

* Privacy masks are often legally required when cameras view:

  * Public areas
  * Neighbouring properties

### Important

Always verify compliance with local regulations and privacy laws.

---

## 📌 Night Vision Testing

Test IR night vision by briefly covering the camera lens.

### Verify

* IR mode activates correctly
* Illumination coverage distance matches manufacturer specifications

---

# 🛠 Recommended Configuration Checklist

| Feature        | Recommended Setting       |
| -------------- | ------------------------- |
| Day/Night Mode | AUTO (ICR)                |
| WDR            | Level 2–3                 |
| 3D-DNR         | Enabled                   |
| OSD Timestamp  | Enabled                   |
| Camera Name    | Enabled                   |
| Privacy Mask   | Configure as required     |
| PTZ Presets    | Configure for PTZ cameras |
| Time Sync      | NTP                       |

---

# 📌 Summary

This procedure outlines the complete process for tuning CCTV camera image quality and optimizing video performance.

The guide includes:

* Camera image adjustment
* WDR configuration
* Night vision setup
* Noise reduction tuning
* Privacy mask configuration
* PTZ setup
* OSD and timestamp management

Proper image tuning ensures:

* Improved recording quality
* Better low-light performance
* Accurate forensic evidence
* Enhanced surveillance reliability
* Regulatory compliance for monitored areas

 ---
