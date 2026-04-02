# Software & Configuration

> Le stack logiciel d'une Voron tourne quasi-exclusivement sur **Klipper**. Cette page liste les composants essentiels, les outils de configuration et les ressources pour démarrer.

---

## 🏗️ Full software stack

```
Raspberry Pi / CB1 / Orange Pi
    ├── Mainsail ou Fluidd         ← Web interface (you control the machine here)
    ├── Moonraker                  ← API between the interface and Klipper
    ├── Klipper                    ← Firmware (runs on Pi + mainboard)
    └── Katapult (optionnel)       ← CAN / USB bootloader for easy flashing
```

---

## ⚙️ Klipper

**The reference firmware for all Voron builds.** Klipper tourne en partie sur le Raspberry Pi (calculs) et en partie sur la carte mère (temps réel). This architecture enables advanced features impossible on a classic firmware.

- 🔗 [klipper3d.org — Documentation officielle](https://www.klipper3d.org/)
- 🔗 [GitHub — Klipper3d/klipper](https://github.com/Klipper3d/klipper)

**Key features for Voron:**
- `RESONANCE_TEST` + `INPUT_SHAPER` — vibration calibration (ADXL345)
- `PRESSURE_ADVANCE` — filament pressure compensation
- `BED_MESH` — surface compensation
- Macros Jinja2 — automation of all print sequences

---

## 🌐 Web interfaces

### Mainsail ⭐

**Community status:** ⭐ Proven — recommended by the Voron project

Clean and lightweight web interface, optimized for Klipper. Configurable dashboard, macro management, log access.

- 🔗 [docs.mainsail.xyz](https://docs.mainsail.xyz/)
- 🔗 [GitHub — mainsail-crew/mainsail](https://github.com/mainsail-crew/mainsail)

### Fluidd

**Community status:** ⭐ Proven

Alternative to Mainsail, slightly different UI. Comparable features. Personal preference.

- 🔗 [docs.fluidd.xyz](https://docs.fluidd.xyz/)

---

## 🔌 Moonraker

REST API between the web interface (Mainsail/Fluidd) and Klipper. Also handles updates via `update_manager`.

- 🔗 [moonraker.readthedocs.io](https://moonraker.readthedocs.io/)

---

## 📦 Recommended installation

### KIAUH ⭐

**KIAUH** (Klipper Installation And Update Helper) is the installation script that handles everything in a few commands. This is the recommended method.

```bash
git clone https://github.com/dw-0/kiauh.git
./kiauh/kiauh.sh
```

- 🔗 [GitHub — dw-0/kiauh](https://github.com/dw-0/kiauh)

### MainsailOS / FluiddPi

Pre-configured Raspberry Pi images with the full stack installed. The easiest way to start.

- 🔗 [MainsailOS](https://docs-os.mainsail.xyz/)
- 🔗 [FluiddPi](https://github.com/fluidd-core/FluiddPi)

---

## 🔧 Calibration tools

### Ellis' Print Tuning Guide ⭐⭐⭐

**The absolute reference** for tuning a Voron (or any Klipper printer). Pressure advance, first layer, retraction, speed tuning… it's all there.

- 🔗 [ellis3dp.com/Print-Tuning-Guide](https://ellis3dp.com/Print-Tuning-Guide/)

### Voron Tap Calibration

Guide officiel pour calibrer le Z offset avec Tap/probes eddy.

- 🔗 [klipper3d.org — Probe Calibrate](https://www.klipper3d.org/Probe_Calibrate.html)

### Input Shaper (ADXL345)

- 🔗 [klipper3d.org — Resonance Compensation](https://www.klipper3d.org/Resonance_Compensation.html)

---

## 📁 Reference configs

### Configs officielles Voron ⭐

The Voron repo contains reference Klipper configs by model (V0, Trident, V2.4). Recommended starting point.

- 🔗 [github.com/VoronDesign/Voron-2](https://github.com/VoronDesign/Voron-2/tree/Voron2.4/firmware/klipper_configurations)
- 🔗 [github.com/VoronDesign/Voron-Trident](https://github.com/VoronDesign/Voron-Trident)

### Klicky Macros

Macros Klipper pour les probes Klicky / KlickyNG.

- 🔗 [GitHub — jlas1/Klicky-Probe / Klipper_macros](https://github.com/jlas1/Klicky-Probe/tree/main/Klipper_macros)

### Happy Hare (MMU)

Extended Klipper firmware for MMU systems (ERCF, TradRack…).

- 🔗 [GitHub — moggieuk/Happy-Hare](https://github.com/moggieuk/Happy-Hare)

---

## 📷 Caméra (Crowsnest)

Crowsnest est le gestionnaire de caméra pour Klipper. Remplace MJPEG-streamer et supporte les caméras USB et CSI.

- 🔗 [GitHub — mainsail-crew/crowsnest](https://github.com/mainsail-crew/crowsnest)

Voir la [page dédiée Crowsnest](crowsnest.md) pour les configs et modèles de caméra compatibles.

---

## 🔄 Updates

Klipper, Moonraker, Mainsail, and extensions update via the Mainsail/Fluidd interface (Update Manager section) or via KIAUH. Updating **regularly** is recommended — Klipper receives significant improvements monthly.

> ⚠️ After a Klipper update, always do a `FIRMWARE_RESTART` and verify your macros still work. Breaking changes are rare but do happen.
