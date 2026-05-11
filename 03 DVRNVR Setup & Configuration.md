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

