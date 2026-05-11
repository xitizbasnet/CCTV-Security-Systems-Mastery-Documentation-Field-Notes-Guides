# CCTV Infrastructure & Network Surveillance Documentation

> **From Installation to Enterprise Integration**

---

## 📘 Document Information

| Item           | Details                                                                       |
| -------------- | ----------------------------------------------------------------------------- |
| Document Title | CCTV Technician                                                               |
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
