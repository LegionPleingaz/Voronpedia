# Moteurs

> Stepper motors determine the speed, torque, and noise of your machine. The choice depends on usage (high-speed XY axes vs precision Z vs extruder).

---

## 💡 Quel moteur pour quoi ?

| Position | Format | Notes |
|----------|--------|-------|
| XY (gantry) | NEMA17 standard ou HV | Plus de couple = plus de vitesse |
| Z (Trident) | NEMA17 pancake | Course faible, couple moyen suffit |
| Extruder (CW2) | NEMA17 short pancake | Weight is priority |
| Extruder (Orbiter / Sherpa) | NEMA14 round | Very light, high torque |

---

## Bondtech

Premium quality motors, often bundled with Bondtech kits (LGX, etc.).

| Reference | Format | Use | Datasheet |
|-----------|--------|-------|-------|
| 13013A | NEMA14 Round Ø36mm 20mm | Extrudeur (Orbiter, Sherpa) | [PDF](https://www.bondtech.se/downloads/TDS/Bondtech-13013A-classH-36H020H-1004A-001.pdf) |
| 13002A | NEMA17 Pancake 22mm | Extrudeur léger | [PDF](https://www.bondtech.se/downloads/TDS/Bondtech_13002A-classB-17HS0401L1-18B.pdf) |
| 13003A | NEMA17 Pancake 25mm | Extrudeur CW2 | [PDF](https://www.bondtech.se/downloads/TDS/Bondtech_13003A-classB-42H025H-0704-002.pdf) |
| 13007A | LGX Pancake 25mm | Extrudeur LGX | [PDF](https://www.bondtech.se/downloads/TDS/Bondtech_13007A-classH-42H025H-0704A-005.pdf) |

---

## LDO ⭐ Recommended

**Community status:** ⭐ Proven — LDO is the official reference supplier for Voron kits.

| Reference | Format | Use | Datasheet |
|-----------|--------|-------|-------|
| 36STH20-1004AHG(XH) | NEMA14 Round | Extrudeur compact | [Info](https://cdn.shopifycdn.net/s/files/1/1619/4791/files/HT_LDO-36STH20-1004AHG_XH_RevA_00.png) |
| LDO-42STH*** | NEMA17 (plusieurs longueurs) | XY, Z | [PDF](https://ldomotors.com/uploads/product_attachment/path/6/LDO-42STH_Info_Sheet.pdf) |
| LDO-57STH*** | NEMA23 | XY haute performance | [PDF](https://ldomotors.com/uploads/product_attachment/path/8/LDO-57STH_Info_Sheet.pdf) |

> Les moteurs LDO sont vendus directement via leur site et les revendeurs officiels (Fabreeko, West3D, KB-3D…).

---

## OMC (StepperOnline)

Budget option. Decent quality, widely available on Amazon/AliExpress.

| Reference | Format | Use | Datasheet |
|-----------|--------|-------|-------|
| 17HE08-1004S | NEMA17 22mm | Extrudeur | [PDF](https://www.omc-stepperonline.com/index.php?route=product/product/get_file&file=2726/17HE08-1004S.pdf) |

---

## Mods moteurs

### KIC Water-Cooled Block (WC Block)

**Difficulté :** 🔴 Advanced  
**Statut communauté :** 🧪 Experimental

Water cooling block for XY motors, for intensive high-speed configurations (>300mm/s continuous). Requires a watercooling loop.

- 🔗 [GitHub — 3DPrintingMods / KIC_Steppers_Motors](https://github.com/3DPrintingMods/KIC_Steppers_Motors)
