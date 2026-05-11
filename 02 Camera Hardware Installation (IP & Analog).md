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

## 🛠️ IP Camera Installation Steps

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

## 🛠️ Analog (HDTVI/AHD/CVI) Camera Installation Steps

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
