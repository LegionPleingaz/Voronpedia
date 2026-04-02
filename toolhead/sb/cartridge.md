# Cartridges & Hotends (StealthBurner)

> In Voron terminology, the "cartridge" refers to the **hotend + printhead** assembly that slides into the StealthBurner. Each hotend manufacturer has an official printhead in the Voron repo.

---

## 💡 Understanding the system

```
StealthBurner body
    ├── Extrudeur (CW2, Orbiter, Galileo…)   ← voir page Extrudeurs
    └── Cartridge / Printhead
            └── Hotend (Dragon, Revo, Rapido…)
```

Le printhead est la pièce imprimée qui tient le hotend. Un hotend = un printhead spécifique (ou adaptateur).

---

## 🌡️ Comparatif rapide des hotends

| Hotend | Max Temp | Débit | Prix | Points forts |
|--------|----------|-------|------|-------------|
| Phaetus Dragon | 300°C | Moyen | ~45€ | Référence, très documenté |
| Phaetus Rapido | 320°C | Élevé | ~60€ | Haute vitesse |
| Phaetus BMO | 300°C | Moyen | ~40€ | Compact |
| Phaetus BMS | 300°C | Moyen | ~40€ | Compact sans sock |
| Revo Voron ⭐ | 300°C | Moyen | ~65€ | Changement buse sans outil |
| Revo Six / V6 | 300°C | Moyen | ~55€ | Compatibilité V6 |
| Revo Micro | 280°C | Faible | ~45€ | Ultra compact |

---

## 🟠 Phaetus

### Phaetus Dragon ⭐

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven — hotend de référence Voron

Le Dragon est le hotend le plus répandu sur Voron. Deux versions :
- **Dragon Standard Flow** — usage courant
- **Dragon High Flow** — débits élevés, haute vitesse

- 🔗 [Printhead officiel SB — Dragon](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Stealthburner/Printheads/phaetus_dragon)

---

### Phaetus Rapido ⭐

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

Haute température (320°C) et haut débit. Idéal pour les matières techniques (PA, PC, ABS haute vitesse). Deux versions : **HF** (High Flow) et **UHF** (Ultra High Flow).

- 🔗 [Printhead officiel SB — Rapido](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Stealthburner/Printheads/phaetus_rapido)

---

### Phaetus BMO

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

Hotend compact de nouvelle génération Phaetus. Buse à changement rapide intégrée.

- 🔗 [Printhead officiel SB — BMO](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Stealthburner/Printheads/phaetus_bmo)

---

### Phaetus BMS

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

Variante du BMO sans silicone sock. Profil légèrement différent.

- 🔗 [Printhead officiel SB — BMS](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Stealthburner/Printheads/phaetus_bms)

---

## 🔵 E3D / Revo

> The **Revo** lineup from E3D is distinguished by its **tool-free nozzle change system without preheating**. Nozzle + heatbreak are a single hand-screwable piece.

### Revo Voron ⭐

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

La version Revo conçue spécifiquement pour le StealthBurner. Changement de buse en 30 secondes, à froid, sans clé.

- 🔗 [Printhead officiel SB — Revo Voron](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Stealthburner/Printheads/revo_voron)

> ⚠️ Revo nozzles are proprietary and more expensive than standard V6 (~$15/nozzle). But they swap in 30 seconds — useful for switching between diameters.

---

### Revo Six / V6

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

Montage du Revo Six ou du classique V6 E3D sur StealthBurner.

- 🔗 [Printhead officiel SB — Revo Six / V6](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Stealthburner/Printheads/revo_six_and_v6)

---

### Revo Micro

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

Version ultra-compacte du Revo. Utile pour les configs à espace restreint.

- 🔗 [Printhead officiel SB — Revo Micro](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Stealthburner/Printheads/revo_micro)

---

## 🔗 Ressource importante

Tous les printheads officiels Voron sont dans le repo Voron-Stealthburner :  
📁 [github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Stealthburner/Printheads](https://github.com/VoronDesign/Voron-Stealthburner/tree/main/STLs/Stealthburner/Printheads)

Si ton hotend n'est pas listé, cherche d'abord dans ce dossier — il y a probablement un printhead officiel que cette page n'a pas encore indexé.
