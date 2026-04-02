# Bed & Mounting

> The bed (heated plate) is the print surface. On Voron V2.4, it's suspended by 4 Z screws and automatically leveled (QGL). Mods here improve mounting, flatness, and print surface.

---

## 🔩 Mounting

### Kinematic Bed Mount ⭐

**Difficulty:** 🟡 Medium
**Community status:** ⭐ Proven — strongly recommended

| Model     | Compatible |
|-----------|-----------|
| V2.4      | ✅         |
| Trident   | ✅         |

The stock mounting uses 3 or 4 rigid screws that constrain the bed and create thermal stress. The kinematic mount uses ball joints that let the bed expand freely while remaining perfectly positioned.

**Concrete benefits:**
- More stable and reproducible bed mesh
- Faster and more accurate QGL
- Less deformation at high chamber temperatures

- 🔗 [GitHub — tanaes / kinematic_bed](https://github.com/tanaes/whopping_Voron_mods/blob/main/kinematic_bed/README_v2_assembly.md)

> ⭐ One of the highest-impact mods for first-layer quality, especially in a heated chamber (ABS/ASA).

---

## 🛏️ Print surfaces

### Voroff

**Difficulty:** 🟢 Easy (purchase, no printing)
**Community status:** 🧪 Experimental — niche but appreciated

Premium ceramic or technical material print plates.

- 🔗 [voroff.com](https://www.voroff.com/)

---

## 💡 Print surface notes

The Voron community commonly uses:

| Surface | Materials | Notes |
|---------|----------|-------|
| **Textured PEI** (spring steel) | ABS, ASA, PETG, PLA | The standard — adhesion without glue |
| **Smooth PEI** | PLA, PETG | Better surface finish |
| **Garolite (G10)** | Nylon, PA | Superior adhesion for technical materials |
| **Borosilicate + glue** | Everything | Stock or legacy approach |

> Most LDO kits include a textured PEI plate on a steel sheet. This is the best general starting option.

---

## 🌡️ Bed temperature by material

| Filament | Bed temp | Chamber |
|----------|----------|---------|
| PLA | 60°C | Open the front panel |
| PETG | 70–80°C | Closed OK |
| ABS | 100–110°C | 50–60°C chamber |
| ASA | 100–110°C | 50–60°C chamber |
| PA / Nylon | 70°C (G10) | 60–70°C chamber |
| PC | 100–120°C | 70°C chamber |
