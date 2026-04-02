# AB Drives, XY Joints & AWD

> AB drives are the XY motors and their mounts at the rear of the gantry. XY joints (sometimes called "pins mod") improve the connection between belts and the carriage. AWD (All-Wheel Drive) adds two front motors for 4-point drive.

---

## 🔧 AB Drives

### Y Endstop Relocation ⭐

**Difficulty:** 🟢 Easy
**Community status:** ⭐ Proven

| Model     | Compatible |
|-----------|-----------|
| V2.4      | ✅         |

Moves the Y endstop to a more reliable and accessible position. Improves Y homing repeatability. Mod by Hartk1213.

- 🔗 [GitHub — hartk1213 / Voron2.4_Y_Endstop_Relocation](https://github.com/VoronDesign/VoronUsers/tree/main/printer_mods/hartk1213/Voron2.4_Y_Endstop_Relocation)

---

### Pin Mod (XY Joints) ⭐

**Difficulty:** 🟢 Easy
**Community status:** ⭐ Proven — near-standard V2.4/Trident upgrade

| Model     | Compatible |
|-----------|-----------|
| V2.4      | ✅         |
| Trident   | ✅         |

Replaces the screws holding the XY joints with precision dowel pins. Eliminates play in the XY joints, improves repeatability and positioning precision.

- 🔗 [GitHub — hartk1213 / Voron2.4_Trident_Pins_Mod](https://github.com/VoronDesign/VoronUsers/tree/main/printer_mods/hartk1213/Voron2.4_Trident_Pins_Mod)
- 🔗 [Printables — Pin Mod Cutting Jig](https://www.printables.com/fr/model/563841-voron-24-pins-mod-cutting-jig) — cutting jig for pins, by LegionPleingaz

> 💡 The cutting jig lets you cut pins to exact length cleanly and repeatably. **Very useful** for multiple builds or if you want a perfect result.

---

## ⚡ AWD — All-Wheel Drive

### AWD V2.4 ⭐

**Difficulty:** 🔴 Advanced
**Community status:** 🧪 Experimental — active community

| Model     | Compatible |
|-----------|-----------|
| V2.4      | ✅         |
| Trident   | ✅ (with adaptation) |

Adds two motors **at the front** of the gantry in addition to the two rear ones. Result: 4 XY motors for symmetric drive. Enables much higher accelerations without precision loss.

- 🔗 [GitHub — aTinyShellScript / v2.4_AWD](https://github.com/aTinyShellScript/v2.4_AWD/tree/main)

**What it requires:**
- 2 additional NEMA17 motors
- Mainboard with available drivers (Octopus Max EZ, Kraken, or Manta M8P)
- Klipper AWD config (syncing 4 motors)
- Front idlers replaced by active drives

**What it brings:**
- 30–50% higher accelerations at equal mass
- Better belt control at high speed
- Symmetric force distribution on the gantry

> ⚠️ AWD multiplies tuning complexity (4 motors to sync, 4 belts to tension). Reserved for experienced builders with an already well-tuned machine.

---

## 📊 Recommended installation order

| Priority | Mod | Impact |
|----------|-----|--------|
| 🔥 1 | Pin Mod | Immediate XY precision |
| 🔥 2 | Y Endstop Relocation | Reliable homing |
| 🟡 3 | AWD | Advanced high speed |
