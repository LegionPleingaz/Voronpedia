# Probes & leveling

> The probe measures the distance between the nozzle and bed to compensate for surface imperfections (mesh) and automate Z offset. Probe choice directly impacts first layer precision.

---

## ⚡ Eddy Current (inductif)

> Principle: measurement by magnetic field variation. Very high resolution, fast full-bed scan, **no mechanical contact**. Becoming the standard on modern builds.

**Précision indicative : ~0.5 µm** (sur 20 secondes de scan)

| Modèle    | Compatible |
|-----------|-----------|
| V0 / V0.2 | ✅ (certains) |
| Trident   | ✅         |
| V2.4      | ✅         |
| Switchwire| ✅         |

---

### Beacon

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven — référence actuelle

Le Beacon est considéré comme le meilleur probe eddy courant du marché. Interface CAN ou USB, firmware Klipper natif, scan ultra-rapide.

- 🔗 [beacon3d.com](https://beacon3d.com/)

---

### IDM

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

Clone open-source du Beacon, légèrement moins cher. Performances comparables.

- 🔗 [GitHub — ModularPrintingSystem / IDM](https://github.com/ModularPrintingSystem/IDM)

---

### Cartographer

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

Intègre un ADXL345 (accéléromètre pour input shaper). Disponible en version CAN ou USB. Bonne alternative au Beacon.

- 🔗 [cartographer3d.com](https://cartographer3d.com/products/cartographer-probe-v3-with-adxl345-flat-pack-both-can-usb)

---

### BTT Eddy

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

Version BTT du principe eddy. Support Klipper en développement actif.

- 🔗 [biqu.equipment — BTT Eddy](https://biqu.equipment/products/bigtreetech-eddy)

---

## 🔩 Nozzle probe

> Principle: **the nozzle itself** acts as the sensor. Eliminates XY offset between probe and nozzle. Excellent precision but more complex mechanism.

**Précision indicative : ~0.6 µm**

---

### TAP (officiel Voron)

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven

| Modèle    | Compatible |
|-----------|-----------|
| V0 / V0.2 | ❌         |
| Trident   | ✅         |
| V2.4      | ✅         |
| Switchwire| ❌         |

La solution officielle Voron pour le nozzle probing. Nécessite un montage soigné. Compatible avec les toolheads SB standard.

- 🔗 [GitHub — VoronDesign / Voron-Tap](https://github.com/VoronDesign/Voron-Tap)

> ⚠️ Watch out for versions (RC8 recommended). Older optical TAP versions had reliability issues.

---

### FlexTAP

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

Variante du TAP utilisant une lame flexible au lieu d'un rail de guidage. Plus léger et plus simple mécaniquement.

- 🔗 [GitHub — andrewmcgr / FlexTAP](https://github.com/andrewmcgr/FlexTAP)

---

### Boop (V0)

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven

| Modèle    | Compatible |
|-----------|-----------|
| V0 / V0.2 | ✅         |
| Trident   | ❌         |
| V2.4      | ❌         |

L'équivalent du TAP pour le V0. Développé par PrintersForAnts.

- 🔗 [GitHub — PrintersForAnts / Boop](https://github.com/PrintersForAnts/Boop)

---

## 🎯 Mechanical probe (OMRON DF2 type)

> Principle: magnetic switch that deploys / retracts. Simple and reliable, but **XY offset** must be compensated in config, and precision is lower than eddy probes.

**Précision indicative : ~300 µm**

---

### Klicky / KlickyNG

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

| Modèle    | Compatible |
|-----------|-----------|
| V0 / V0.2 | ✅         |
| Trident   | ✅         |
| V2.4      | ✅         |
| Switchwire| ✅         |

La référence historique du probe magnétique pour Voron. Énorme communauté, macros Klipper disponibles. Le KlickyNG est la version améliorée recommandée.

- 🔗 [GitHub — jlas1 / Klicky-Probe](https://github.com/jlas1/Klicky-Probe)

---

### Klicky-00 (PCB)

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

Version PCB du Klicky, compatible Xol toolhead.

- 🔗 [GitHub — DW-Tas / Klicky-00](https://github.com/DW-Tas/Klicky-00)

---

### ZeroClick (V0)

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

| Modèle    | Compatible |
|-----------|-----------|
| V0 / V0.2 | ✅         |
| Trident   | ❌         |
| V2.4      | ❌         |

Solution magnétique minimaliste pour V0. Très populaire sur les petits formats.

- 🔗 [GitHub — zruncho3d / ZeroClick](https://github.com/zruncho3d/ZeroClick)

---

### Quickdraw (Annex)

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

Probe rétractable développé par Annex Engineering. Conçu pour les toolchangers mais utilisable en standalone.

- 🔗 [GitHub — Annex-Engineering / Quickdraw_Probe](https://github.com/Annex-Engineering/Quickdraw_Probe)

---

## 🔧 Other probes

### CR Touch Mod — Switchwire

Mount pour CR Touch adapté au StealthBurner sur Switchwire.

- 🔗 [Printables](https://www.printables.com/fr/model/260473-voron-stealthburner-cr-touch-mod-for-switchwire-to)

### EZABL Mount

- 🔗 [Printables](https://www.printables.com/fr/model/260919-voron-stealthburner-ezabl-mount-adlx-remix-for-12m)

---

## 🛠️ Accessories

### SexBolt Z Endstop

> Replaces the stock Z endstop with a magnetic ball system (Sexbolt). More reliable and repeatable than the original switch.

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven — quasi-obligatoire sur V2.4

| Modèle    | Compatible |
|-----------|-----------|
| V2.4      | ✅         |

- 🔗 [GitHub — hartk1213 / Voron2.4_SexBolt_ZEndstop](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/hartk1213/Voron2.4_SexBolt_ZEndstop)

---

## 📊 Quick comparison

| Probe | Type | Précision | Prix indicatif | Recommandé pour |
|-------|------|-----------|----------------|-----------------|
| Beacon | Eddy | ⭐⭐⭐⭐⭐ | ~80€ | Builds sérieux, haute vitesse |
| Cartographer | Eddy | ⭐⭐⭐⭐⭐ | ~60€ | Idem + ADXL intégré |
| IDM | Eddy | ⭐⭐⭐⭐⭐ | ~40€ | Budget serré, même perf |
| TAP | Buse | ⭐⭐⭐⭐ | ~0€ (imprimé) | V2.4 / Trident déjà montés |
| Klicky | Mécanique | ⭐⭐⭐ | ~5€ | V0, débutants, budget minimal |
| ZeroClick | Mécanique | ⭐⭐⭐ | ~5€ | V0 spécifique |
