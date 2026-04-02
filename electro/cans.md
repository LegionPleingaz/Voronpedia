# CANbus & Toolhead Boards

> CANbus allows replacing the toolhead wire harness (20+ wires) with **a single 4-wire cable** (power + CAN data). It's the major wiring evolution of the last 2 years in Voron builds.

---

## 🚨 READ THIS FIRST

> **⚠️ CANbus requires configuration — you can't just plug it in.**  
> Before ordering anything, read the complete documentation.

📖 **[canbus.esoterical.online](https://canbus.esoterical.online/)** — La référence absolue. Guide complet Katapult + Klipper pour chaque board.

---

## 💡 Understanding l'architecture CAN

```
Raspberry Pi / CB1
      │
      │ USB
      ▼
 Bridge board        ← mainboard OR dedicated USB-CAN bridge (U2C, UTOC…)
      │
      │ CAN bus (2 data wires + 24V + GND = 4 wires total)
      ▼
 Toolhead board      ← mounted on the toolhead, handles everything locally
  (EBB36, SB2209…)
```

The **toolhead board** replaces all individual wires: thermistor, heater, fans, probe, ADXL, LEDs, endstop…

---

## 🔌 USB → CAN Bridge (if your mainboard doesn't have CAN)

If your mainboard doesn't have a native CAN port (Octopus, SKR…), you need a bridge:

| Board | Notes | Lien |
|-------|-------|------|
| BTT U2C | Le plus répandu | [GitHub BTT](https://github.com/bigtreetech/U2C) |
| UTOC | Alternative open-source | — |
| Carte mère en mode bridge | L'Octopus peut servir de pont CAN via USB | [canbus.esoterical.online](https://canbus.esoterical.online/) |

> **Tip:** configuring the Octopus as a CAN bridge avoids buying a U2C. This is the recommended solution if you already have an Octopus.

---

## ⚡ BTT (BigTreeTech)

### EBB36 ⭐

**Difficulté :** 🟡 Medium (config Katapult requise)  
**Community status:** ⭐ Proven — le plus répandu

| Modèle    | Compatible |
|-----------|-----------|
| V0 / V0.2 | ✅ (format compact) |
| Trident   | ✅         |
| V2.4      | ✅         |

Toolhead board universelle au format 36mm. Compatible avec tous les toolheads via mount adaptateur. Connecteur JST-PH.

- 🔗 [GitHub — BTT EBB36 V1.1](https://github.com/bigtreetech/EBB/tree/master/EBB%20CAN%20V1.1%20(STM32G0B1)/EBB36%20CAN%20V1.1)
- 📖 [Config Katapult + Klipper](https://canbus.esoterical.online/toolhead_flashing/common_hardware/BigTreeTech%20EBB36%20V1.2/README.html)

---

### EBB42

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven

Format 42mm. Plus de place pour les connecteurs, légèrement plus lourd. Moins courant que l'EBB36.

- 🔗 [GitHub — BTT EBB42 V1.1](https://github.com/bigtreetech/EBB/tree/master/EBB%20CAN%20V1.1%20(STM32G0B1)/EBB42%20CAN%20V1.1)
- 📖 [Config Katapult + Klipper](https://canbus.esoterical.online/toolhead_flashing/common_hardware/BigTreeTech%20EBB42%20V1.2/README.html)

---

### SB2209 (RP2040) ⭐

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven — conçu spécifiquement pour StealthBurner

| Modèle    | Compatible |
|-----------|-----------|
| Trident   | ✅         |
| V2.4      | ✅         |
| V0 / V0.2 | ❌ (SB uniquement) |

Board intégrée directement dans le corps du StealthBurner. Élimine tous les connecteurs intermédiaires. Chip RP2040.

- 🔗 [GitHub — BTT EBB SB2209](https://github.com/bigtreetech/EBB/tree/master/EBB%20SB2209%20CAN%20(RP2040))
- 📖 [Config Katapult + Klipper](https://canbus.esoterical.online/toolhead_flashing/common_hardware/BigTreeTech%20SB2209%20(RP2040)/README.html)
- 🛡️ [Magic Smoke Protector — anti-misalignment](https://www.printables.com/fr/model/642001-voron-stealthburner-sb2209-misalignment-protector) — **imprime ça avant de brancher le SB2209**

> ⚠️ The SB2209 power connector can be inserted backwards and instantly fry the board. The "Magic Smoke Protector" is a printed mechanical guide that prevents incorrect orientation. **Mandatory.**

---

### SB2240

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

Variante du SB2209 avec driver TMC2240 intégré pour l'extrudeur. Moteur extrudeur directement contrôlé depuis la toolhead board.

- 🔗 [GitHub — BTT EBB SB2240](https://github.com/bigtreetech/EBB/tree/master/EBB%20SB2240_2209%20CAN)
- 📖 [Config Katapult + Klipper](https://canbus.esoterical.online/toolhead_flashing/common_hardware/BigTreeTech%20SB2209%20and%20SB2240/README.html)

---

### MMB CAN (Multi-Material Board)

**Difficulté :** 🔴 Advanced  
**Statut communauté :** 🧪 Experimental

Board CAN dédiée au multi-matière (ERCF, Tradrack). Gère les servos, capteurs et moteurs du système de changement de filament via CAN.

- 🔗 [GitHub — BTT MMB](https://github.com/bigtreetech/MMB)
- 📖 [Config Katapult + Klipper](https://canbus.esoterical.online/toolhead_flashing/common_hardware/BigTreeTech%20MMB%20CAN%20V1.0/README.html)

---

## 🟡 Mellow (FLY)

### Fly SB2040 ⭐

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven

Equivalent Mellow du SB2209, intégré dans le StealthBurner. Chip RP2040.

- 🔗 [GitHub — Mellow Fly-SB2040](https://github.com/Mellow-3D/Fly-SB2040)
- 📖 [Config Katapult + Klipper](https://canbus.esoterical.online/toolhead_flashing/common_hardware/Mellow%20Fly%20SB2040/README.html)

---

### Fly SHT 36 & 42

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven

Équivalent Mellow des EBB36/42. Bon support communautaire.

- 🔗 [GitHub — Mellow CAN Toolboards](https://github.com/Mellow-3D/Klipper-CAN-Toolboards)
- 📖 [Config SHT36/42](https://canbus.esoterical.online/toolhead_flashing/common_hardware/Mellow%20Fly%20SHT36%20and%20SHT42/README.html)
- 📖 [Config SHT36v2](https://canbus.esoterical.online/toolhead_flashing/common_hardware/Mellow%20Fly%20SHT36v2/README.html)

---

### Fly ERCF

Board CAN dédiée à la gestion ERCF (multi-matière), alternative au MMB de BTT.

- 📖 [Config Katapult + Klipper](https://canbus.esoterical.online/toolhead_flashing/common_hardware/Mellow%20Fly%20ERCF/README.html)

---

## 🔵 LDO

### Nitehawk SB ⭐

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven — qualité de fabrication LDO

Board intégrée StealthBurner par LDO. **Utilise USB au lieu de CAN** — simplifie la configuration (pas de Katapult, pas de bridge CAN).

- 🔗 [GitHub — MotorDynamicsLab / Nitehawk-SB](https://github.com/MotorDynamicsLab/Nitehawk-SB)

> Interesting alternative if you want the benefits of an integrated toolhead board without CAN complexity. A single thin USB cable is sufficient.

---

## 🛠️ Others

### ToqueCAN

Board CAN alternative, design open-source.

- 🔗 [GitHub — xbst / ToqueCAN](https://github.com/xbst/ToqueCAN)

### CANboard Mounts

Collection de mounts imprimables pour fixer les différentes toolhead boards (EBB36, SHT36…) sur les différents toolheads.

- 🔗 [GitHub — KayosMaker / CANboard_Mounts](https://github.com/KayosMaker/CANboard_Mounts)

---

## 📊 Which board to choose ?

| Situation | Recommandation |
|-----------|---------------|
| V2.4 / Trident, SB, première CAN | BTT SB2209 (RP2040) |
| V2.4 / Trident, SB, Mellow préféré | Fly SB2040 |
| V0, toolhead custom | BTT EBB36 + CANboard Mount |
| Pas de bridge CAN dispo | Nitehawk SB (USB) |
| Multi-matière ERCF | BTT MMB ou Fly ERCF |

---

## 🔧 Essential resources

| Ressource | Description |
|-----------|-------------|
| [canbus.esoterical.online](https://canbus.esoterical.online/) | **La bible du CAN Klipper** — configs pour chaque board |
| [CANboard Mounts](https://github.com/KayosMaker/CANboard_Mounts) | Mounts imprimables universels |
| [Magic Smoke Protector](https://www.printables.com/fr/model/642001) | **Obligatoire** avant de brancher un SB2209 |
