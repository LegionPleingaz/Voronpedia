# Filtration (VOC & particules)

> L'impression de plastique génère des **COV (composés organiques volatils)** et des particules ultrafines, particulièrement avec l'ABS, l'ASA et le Nylon. La filtration est essentielle dès que tu imprimes dans un espace fermé.

---

## 💡 Two distinct problems

| Problem | Solution |
|----------|----------|
| **VOC / odors** (ABS, ASA…) | Activated carbon |
| **Fine particles** (all materials) | HEPA filter |
| **Chamber heating** | Recirculation + combined filtering |

Most mods listed here combine both. The **Nevermore** lineup has become the community reference.

---

## 🖤 Nevermore — The reference

> Internal chamber air recirculation through activated carbon. Heats the chamber faster **AND** filters VOCs. Natively Klipper-compatible with the Nevermore controller.

### Nevermore StealthMax ⭐

**Difficulté :** 🟡 Medium  
**Community status:** ⭐ Proven — le haut de gamme

| Modèle    | Compatible |
|-----------|-----------|
| V2.4      | ✅         |
| Trident   | ✅         |
| V0 / V0.2 | ❌ (trop grand) |

Large activated carbon volume, two fans, high airflow. Ideal for 300mm+ chambers.

- 🔗 [GitHub — nevermore3d / StealthMax](https://github.com/nevermore3d/StealthMax)

---

### Nevermore Micro ⭐

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven — le plus répandu

| Modèle    | Compatible |
|-----------|-----------|
| V2.4      | ✅         |
| Trident   | ✅         |
| V0 / V0.2 | ✅ (version Duo) |

The classic. Mounts under the bed. **Micro Duo** version (two fans) recommended for better recirculation.

- 🔗 [GitHub — nevermore3d / Nevermore_Micro](https://github.com/nevermore3d/Nevermore_Micro)

---

### Nevermore Mini

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

Intermediate version between Micro and StealthMax.

- 🔗 [GitHub — nevermore3d / Nevermore_Mini](https://github.com/nevermore3d/Nevermore_Mini)

---

### Nevermore Controller

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

Dedicated controller for Nevermore, with integrated VOC sensor (SGP40). Allows controlling the filter via Klipper based on actual detected VOC levels.

- 🔗 [GitHub — SanaaHamel / nevermore-controller](https://github.com/SanaaHamel/nevermore-controller)

> SGP40 sensor recommended to measure actual carbon effectiveness. Activated carbon saturates over time — the sensor tells you when to replace it.

---

## 🏠 HEPA Filters (fine particles)

### Roomba 800/900 HEPA Filter Box

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

| Modèle    | Compatible |
|-----------|-----------|
| V2.4      | ✅         |

Uses Roomba 800/900 series replacement filters (cheap, widely available) mounted in a printed enclosure that replaces the V2.4 rear exhaust.

- 🔗 [Printables](https://www.printables.com/fr/model/551032-voron-24-roomba-800900-hepa-filter-box)

---

### Exhaust HEPA + Carbon Adapter

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

Adapter combining HEPA filter + activated carbon on the standard V2.4 rear exhaust. All-in-one solution.

- 🔗 [Printables](https://www.printables.com/fr/model/582998-voron-24-exhaust-and-hepa-carbon-adapter)

---

## 🟢 Small format filters

### Zero Filter (V0)

**Difficulté :** 🟢 Easy  
**Community status:** ⭐ Proven

| Modèle    | Compatible |
|-----------|-----------|
| V0 / V0.2 | ✅         |

V0-specific activated carbon filtration solution, developed by zruncho3d.

- 🔗 [GitHub — zruncho3d / zerofilter](https://github.com/zruncho3d/zerofilter)

---

### MFNano (Maple Leaf Makers)

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

Compact nano filter, suited for small formats.

- 🔗 [GitHub — MapleLeafMakers / MFNano](https://github.com/MapleLeafMakers/MFNano)

---

### The Filter

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

Minimalist activated carbon alternative.

- 🔗 [GitHub — nateb16 / THE_FILTER](https://github.com/nateb16/VoronUsers/tree/master/printer_mods/nateb16/THE_FILTER)

---

## 🌀 Bed fans (chauffage chambre)

### EVENmore Bed Fans

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

| Modèle    | Compatible |
|-----------|-----------|
| V2.4      | ✅         |

Fans mounted under the bed to homogenize chamber temperature. Speeds up temperature ramp-up and reduces thermal gradients over large surfaces.

- 🔗 [Printables — EVENmore](https://www.printables.com/fr/model/964701-evenmore-bed-fans-with-style)

> Combine with a Nevermore Micro and a chamber temperature sensor for the best possible thermal control.

---

## 📊 Which filter to choose?

| Configuration | Recommendation |
|--------------|----------------|
| V2.4 / Trident, regular ABS / ASA | Nevermore Micro Duo |
| V2.4 / Trident, intensive use | Nevermore StealthMax |
| V0, ABS / ASA | Zero Filter + Nevermore Micro |
| Fine particles priority | Roomba HEPA Box |
| Klipper automated control | Nevermore Controller + SGP40 sensor |
