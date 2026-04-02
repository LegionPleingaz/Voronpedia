# Multi-Material — MMU

> L'impression multi-matière permet de changer de filament automatiquement en cours de print : couleurs différentes, supports en matière soluble, combinaisons rigide/flexible. C'est l'étape suivante après une machine bien réglée.

---

## 💡 MMU system architecture

```
Bobines (N)
    │
    │ tubes PTFE
    ▼
 Sélecteur / MMU     ← choisit quelle bobine alimenter
    │
    │ tube PTFE unique
    ▼
 Toolhead            ← avec cutter ou système de rétraction
    │
    ▼
 Purge / Blobifier   ← évacue le filament résiduel entre les changements
```

A complete MMU system requires: the **MMU mechanics**, **spool holders**, a **compatible toolhead** (cutter or tip shaping), and **Klipper macros** (Happy Hare recommended).

---

## 🔄 MMU Systems

### ERCF v2 ⭐

**Difficulté :** 🔴 Advanced  
**Community status:** ⭐ Proven — la référence open-source

| Channels | Estimated price |
|--------|---------------|
| 8 / 12 / 16 lanes | ~$130–200 (parts + hardware) |

L'ERCF (Enraged Rabbit Carrot Feeder) est le système MMU le plus répandu dans la communauté Voron. Firmware **Happy Hare** recommandé (fork Klipper dédié MMU).

- 🔗 [GitHub — Enraged-Rabbit-Community / ERCF_v2](https://github.com/Enraged-Rabbit-Community/ERCF_v2)
- 📖 [Happy Hare firmware](https://github.com/moggieuk/Happy-Hare)

> ⚠️ ERCF requires tuning time. Plan for multiple calibration sessions before achieving reliable filament changes.

---

### TradRack (Annex Engineering)

**Difficulté :** 🔴 Advanced  
**Statut communauté :** 🧪 Experimental

Alternative à l'ERCF développée par Annex Engineering. Architecture différente (rail linéaire au lieu de roues). Compatible Happy Hare.

- 🔗 [GitHub — Annex-Engineering / TradRack](https://github.com/Annex-Engineering/TradRack)

---

## 🧵 Passive spool holders

> Les porte-bobines passifs utilisent un système de rembobinage mécanique (ressort ou gravité) pour maintenir la tension du filament sans moteur. Plus simple et silencieux que les motorisés.

### Filamentalist Classic Rewinder ⭐

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven — le standard ERCF

Le porte-bobine recommandé par la communauté ERCF. Système de rembobinage à ressort, imprimable, simple à construire.

- 🔗 [GitHub — ERCF_v2 / Filamentalist Classic](https://github.com/Enraged-Rabbit-Community/ERCF_v2/tree/master/Recommended_Options/Filamentalist_Rewinder/Filamentalist_Classic_Rewinder)

### Filamentalist F3 (FV3)

Version évoluée du Classic, meilleure gestion des bobines de diamètres variables.

- 🔗 [GitHub — Filamentalist FV3](https://github.com/Enraged-Rabbit-Community/ERCF_v2/tree/master/Recommended_Options/Filamentalist_Rewinder/Filamentalist_FV3_Rewinder)

### Filamentalist Enclosure

Version enclostée pour monter les bobines proprement dans un boîtier.

- 🔗 [GitHub — Filamentalist Enclosure](https://github.com/Enraged-Rabbit-Community/ERCF_v2/tree/master/Recommended_Options/Filamentalist_Rewinder/Filamentalist_Enclosure)

---

## ⚙️ Motorized spool holders

> Les porte-bobines motorisés actionnent un moteur pour rembobiner activement le filament. Plus complexes mais meilleure gestion des bobines légères ou partiellement vides.

### BoxTurtle ⭐

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven

Système 4 ou 8 bobines avec moteurs de rembobinage. Architecture modulaire, peut être étendu. Développé par ArmoredTurtle.

- 🔗 [GitHub — ArmoredTurtle / BoxTurtle](https://github.com/ArmoredTurtle/BoxTurtle)

### Night Owl

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

Alternative motorisée au BoxTurtle. Conçu pour s'intégrer proprement sur le dessus d'une Voron.

- 🔗 [GitHub — mjonuschat / NightOwl](https://github.com/mjonuschat/NightOwl)

---

## ✂️ MMU-compatible toolheads

> Le changement de filament en MMU nécessite un toolhead capable de couper proprement le filament (tip forming ou cutter physique). Sans ça, les changements sont peu fiables.

### Filametrix ⭐

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven — le standard pour ERCF

Lame de coupe intégrée au StealthBurner. Coupe proprement le filament à chaque changement de matière.

- 🔗 [GitHub — sorted01 / Filametrix](https://github.com/sorted01/Filametrix)

### FilamATrix

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

Fork du Filametrix avec améliorations de fiabilité et compatibilité étendue.

- 🔗 [GitHub — thunderkeys / FilamATrix](https://github.com/thunderkeys/FilamATrix)

### A4T-AFC

**Difficulté :** 🔴 Advanced  
**Statut communauté :** 🧪 Experimental

Toolhead complet multi-matière avec AFC (Automated Filament Changer) intégré.

- 🔗 [GitHub — SouthAsh1 / A4T-AFC](https://github.com/SouthAsh1/A4T-AFC)

### Jabberwocky

**Difficulté :** 🔴 Advanced  
**Statut communauté :** 🧪 Experimental

Toolhead expérimental pour MMU avancé.

- 🔗 [GitHub — kinematicdigit / Jabberwocky](https://github.com/kinematicdigit/Jabberwocky)

---

## 📊 Where to start ?

| Objectif | Recommandation |
|----------|---------------|
| Première expérience MMU | ERCF v2 + Filamentalist Classic + Filametrix |
| Budget limité, simple | ERCF v2 (pièces imprimées + peu de hardware) |
| Fiabilité maximale | ERCF v2 + BoxTurtle + FilamATrix + Happy Hare |
| Multi-matière sur V0 | TradRack (plus compact) |

> 💡 **Tip:** master your machine in single-material printing before diving into MMU. An MMU amplifies all existing issues (belt tension, retraction, poorly calibrated temperature tower).
