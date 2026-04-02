# Extrudeurs

> The extruder pushes filament toward the hotend. The gear ratio determines torque and movement precision. A higher ratio = more torque, better retraction, better flexible material handling — at the cost of slight latency.

Tous les extrudeurs listés ici sont montés sur **StealthBurner** sauf mention contraire.

---

## 📊 Quick comparison

| Extrudeur | Gear Ratio | Poids approx. | Points forts |
|-----------|-----------|---------------|-------------|
| Clockwork 2 | 5:1 | ~200g | Officiel Voron, grande communauté |
| Orbiter v2 | 7.5:1 | ~120g | Léger, compact, haute vitesse |
| Galileo 2 SA | 9:1 | ~150g | Couple maximal, multi-matière |
| Sherpa Mini | 6.25:1 | ~90g | Ultra-léger, populaire V0 |
| Sherpa Micro | 5:1 | ~60g | Le plus léger |
| Folded Ascender | 40:1 | ~180g | Flexibles et TPU |

---

## 🟢 Official Voron

### Clockwork 2 (CW2)

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven — solution de référence

| Modèle    | Compatible |
|-----------|-----------|
| V0 / V0.2 | ❌ (trop lourd) |
| Trident   | ✅         |
| V2.4      | ✅         |

L'extrudeur officiel Voron pour StealthBurner. Gear ratio 5:1, NEMA17 standard. Excellent point de départ, très documenté.

- 🔗 [GitHub — VoronDesign / Voron-Stealthburner](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Clockwork2)

**Variantes**
- [CW2 Nema17 mod](https://www.printables.com/fr/model/454292) — utilise un Nema17 pancake plus long
- [CW2 Large Gear](https://github.com/nhchiu/VoronMods/tree/main/Extruders/Large_Gear_Clockwork2) — grande roue dentée pour meilleure précision

---

## 🔵 Orbiter

### Orbiter v2

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

Gear ratio **7.5:1** — Excellent équilibre poids/couple. Très populaire pour la haute vitesse (Klipper INPUT_SHAPER). Moteur intégré.

- 🔗 [orbiterprojects.com](https://www.orbiterprojects.com/orbiter-v2-0/)
- 🔗 [Mount SB pour Orbiter v2](https://www.printables.com/fr/model/345237-voron-stealthburner-orbiter-v20) — Printables

---

## 🟣 Galileo (JaredC01)

### Galileo 2 SA (Standalone)

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven

Gear ratio **9:1** — Le plus de couple dans cette catégorie. Idéal pour les matières difficiles et les configurations multi-matière (ERCF, Tradrack). Le "SA" = Standalone, se monte directement sur SB.

- 🔗 [GitHub — JaredC01 / Galileo2](https://github.com/JaredC01/Galileo2)

### Galileo 2E (Extruder)

Variante de la tête Galileo 2 optimisée pour l'intégration SB. Même ratio 9:1.

- 🔗 [GitHub — JaredC01 / Galileo2](https://github.com/JaredC01/Galileo2)

### Galileo (v1) SB Mount

Mount pour l'Orbiter v1 sur SB — **ratio 7.5:1**.

- 🔗 [GitHub — Mamsih / Galileo-stealthBurner](https://github.com/Mamsih/Galileo-stealthBurner)

---

## 🟡 LGX / Bondtech

### SB LGX Lite

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

Mount pour LGX Lite Bondtech sur StealthBurner.

- 🔗 [GitHub — Eytecz](https://github.com/Eytecz/LGX_Lite_Stealthburner_CW2_style_mount)

---

## 🔴 Sherpa (Annex Engineering)

Famille d'extrudeurs très légers développés par Annex, très populaires sur **V0** et les machines qui cherchent à minimiser la masse mobile.

### Sherpa Mini

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

Gear ratio **6.25:1**. Le plus populaire de la gamme. Excellent rapport poids/performance.

- 🔗 [GitHub — Annex-Engineering / Sherpa_Mini](https://github.com/Annex-Engineering/Sherpa_Mini-Extruder)

**Variante :** [Sherpa Crew Mini](https://github.com/jrlomas/Sherpa-Crew-Mini) — version renforcée avec meilleure tension de levier.

### Sherpa Micro

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

Gear ratio **5:1**. Le plus petit et le plus léger. Idéal V0.

- 🔗 [GitHub — Annex-Engineering / Sherpa_Micro](https://github.com/Annex-Engineering/Sherpa_Micro-Extruder)

---

## ⚙️ Specialized

### Hummingbird

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

Extrudeur ultra-compact à engrenages hélicoïdaux. Très silencieux.

- 🔗 [GitHub — nhchiu / Hummingbird](https://github.com/nhchiu/VoronMods/raw/main/Extruders/Hummingbird)

### SB VZ HextruDort

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

Gear ratio **6.25:1**. Port du HextruDort (connu dans l'écosystème VZBot) pour StealthBurner.

- 🔗 [Printables](https://www.printables.com/fr/model/369577-vz-hextrudort-for-stealthburner)

### ProtoXtruder

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

Gear ratio **4.4:1**. Compact, design imprimable entièrement.

- 🔗 [GitHub — nhchiu / ProtoXtruder](https://github.com/nhchiu/VoronMods/tree/main/Extruders/ProtoXtruder)

### Folded Ascender

**Difficulté :** 🔴 Advanced  
**Statut communauté :** 🧪 Experimental

Gear ratio **40:1** — ratio extrême conçu pour les **filaments flexibles (TPU, TPE)**. Le seul extrudeur de cette liste capable de pousser du flexible sans slipping.

- 🔗 [GitHub — Annex-Engineering / Folded_Ascender](https://github.com/Annex-Engineering/Folded_Ascender-Extruder)

> ⚠️ The 40:1 ratio implies very low retraction (0.5-1mm). Fully recalibrate retractions when switching from a CW2.
