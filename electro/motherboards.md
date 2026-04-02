# Cartes mères (Motherboards)

> The mainboard orchestrates all components: motors, heaters, fans, sensors. The choice depends on the Voron model, number of axes, and your architecture (USB, CAN, Manta+CB1...).

---

## 💡 How to choose ?

| Situation | Recommandation |
|-----------|---------------|
| V0 simple, budget serré | BTT Manta E3EZ + CB1, ou SKR mini E3 |
| Trident / V2.4 standard | BTT Octopus 1.1 ou Manta M8P + CB1 |
| V2.4 avec AWD (4 moteurs XY) | BTT Octopus Max EZ ou Kraken |
| Architecture tout-CAN | Manta M8P + EBB36/42 sur toolhead |
| Budget serré V2.4 | FYSETC Spider v3 |

> **Tip:** BTT **Manta** boards include a socket for the **CB1** module (Raspberry Pi alternative), which greatly simplifies wiring. Highly recommended for new builds.

---

## BTT (BigTreeTech)

### SKR Series (legacy)

> ⚠️ The SKR lineup is mature but tends to be replaced by Manta boards for new builds. Still valid for upgrading an existing machine.

| Carte | Usage | Lien |
|-------|-------|------|
| SKR mini E3 | V0, Switchwire | [GitHub](https://github.com/bigtreetech/BIGTREETECH-SKR-mini-E3) |
| SKR E3 | V0, Switchwire | [GitHub](https://github.com/bigtreetech/SKR-3) |
| SKR Pro | Trident, V2.4 (legacy) | [GitHub](https://github.com/bigtreetech/BIGTREETECH-SKR-PRO-V1.1) |
| SKR 1.4 | V2.4 (legacy) | [GitHub](https://github.com/bigtreetech/BIGTREETECH-SKR-V1.3) |

---

### Manta Series ⭐ Recommended

> Includes a socket for the **CB1** (Raspberry Pi alternative). Clean architecture, ideal for new builds.

| Carte | Drivers | Usage idéal | Lien |
|-------|---------|-------------|------|
| Manta E3EZ | 5 | V0 / Switchwire | [GitHub](https://github.com/bigtreetech/Manta-E3EZ) |
| Manta M4P | 4 | V0 étendu | [GitHub](https://github.com/bigtreetech/Manta-M4P) |
| Manta M5P | 5 | Trident | [GitHub](https://github.com/bigtreetech/Manta-M5P) |
| Manta M8P | 8 | V2.4 / AWD | [GitHub](https://github.com/bigtreetech/Manta-M8P) |

---

### Octopus Series

> The safe bet for V2.4. The Octopus 1.1 is probably the most widespread board in the Voron community.

| Carte | Drivers | Notes | Lien |
|-------|---------|-------|------|
| Octopus 1.1 | 8 | Référence V2.4 | [GitHub](https://github.com/bigtreetech/BIGTREETECH-OCTOPUS-V1.0) |
| Octopus Pro | 8 | Drivers TMC5160 natifs | [GitHub](https://github.com/bigtreetech/BIGTREETECH-OCTOPUS-Pro) |
| Octopus Max EZ | 10 | AWD + extensions | [GitHub](https://github.com/bigtreetech/Octopus-Max-EZ) |

**Mod utile :** [Octopus Pro Fan Case](https://github.com/Ramalama2/Voron-2-Mods/tree/main/Octopus_Pro_FanCase) — boîtier de ventilation imprimable pour l'Octopus Pro.

---

### Kraken

**8 drivers TMC5160** natifs, conçu pour les architectures AWD et les gros moteurs. Haut de gamme BTT.

- 🔗 [GitHub — BTT Kraken](https://github.com/bigtreetech/BIGTREETECH-Kraken)

---

## FYSETC

### Spider v3

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

Bonne alternative à l'Octopus, souvent moins chère. Très utilisée dans la communauté francophone.

- 🔗 [GitHub — FYSETC Spider](https://github.com/FYSETC/FYSETC-SPIDER)

### Spider King

Version étendue du Spider avec plus de drivers. Pour les builds complexes.

- 🔗 [GitHub — FYSETC](https://github.com/FYSETC/)

### Cheetah v3 (V0)

Carte compacte spécifique pour V0.

- 🔗 [GitHub — FYSETC Cheetah v3](https://github.com/FYSETC/Cheetah_V3.0)

### E4 / S6 (legacy)

Cartes plus anciennes, encore fonctionnelles mais non recommandées pour les nouvelles builds.

- [E4](https://github.com/FYSETC/FYSETC-E4) · [S6](https://github.com/FYSETC/FYSETC-S6)

### Catalyst

Kit complet FYSETC incluant la carte + Pi + câblage.

- 🔗 [GitHub — FYSETC Catalyst](https://github.com/FYSETC/Catalyst_Kit)

---

## LDO

### Leviathan

Carte haut de gamme développée par LDO, conçue spécifiquement pour les Voron. Qualité de fabrication premium.

- 🔗 [GitHub — MotorDynamicsLab / Leviathan](https://github.com/MotorDynamicsLab/Leviathan)

---

## Makerbase

### Monster8

Compatible Voron 2.4, configuration Klipper documentée par Makerbase.

- 🔗 [GitHub — MKS Monster8 + guide Voron](https://github.com/makerbase-mks/MKS-Monster8/wiki/MKS_MONSTER8_V2_manual_based_on_Klipper_firmware_to_configure_Voron_2_4_machine)

---

## Mellow (FLY)

### FLY Super8

Carte 8 drivers de Mellow, bonne alternative à l'Octopus.

- 🔗 [GitHub — Mellow-3D / Fly-Super8](https://github.com/Mellow-3D/Fly-Super8)
