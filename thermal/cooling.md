# Refroidissement (Cooling)

> Le refroidissement intervient à deux endroits distincts sur une Voron : le **part cooling** (refroidissement de la pièce imprimée) et le **refroidissement de la chambre** (nécessaire pour le PLA/PETG en enceinte fermée, ou pour évacuer la chaleur en fin de print).

---

## 💡 Two types of cooling — don't confuse them

| Type | Rôle | Quand c'est critique |
|------|------|---------------------|
| **Part cooling** | Refroidit le plastique fondu à la sortie buse | PLA, PETG, ponts, overhangs |
| **Chamber cooling** | Évacue la chaleur de la chambre | PLA en chambre chauffée, fin de print |

---

## 💨 Part Cooling

> Le part cooling standard est intégré au StealthBurner. Les mods ici améliorent le débit ou permettent d'utiliser des soufflantes plus puissantes.

### CPAP Cooling — WS7040

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

| Modèle    | Compatible |
|-----------|-----------|
| V2.4      | ✅         |
| Trident   | ✅         |
| V0 / V0.2 | ❌ (trop encombrant) |

Le **WS7040** est un turboventilateur CPAP (utilisé en médical) repurposé pour le part cooling. Il génère un débit d'air considérablement supérieur aux soufflantes 5015 classiques.

- 🔗 [Printables — WS7040 mount pour extrusion alu](https://www.printables.com/fr/model/521393-ws7040-cpap-fan-mount-for-aluminum-extrusion-voron)

> ⚠️ Le WS7040 est bruyant à haut régime. Prévoir une gestion PWM fine via Klipper. Le gain est réel sur les overhangs extrêmes mais peut-être surdimensionné pour une utilisation générale.

---

### CPAP Tophat Exhaust

**Difficulté :** 🟡 Medium  
**Statut communauté :** 🧪 Experimental

| Modèle    | Compatible |
|-----------|-----------|
| V2.4      | ✅         |

Mod tophat qui intègre la ventilation CPAP + l'exhaust dans le même module supérieur.

- 🔗 [Printables — Tophat CPAP + Exhaust](https://www.printables.com/fr/model/975981-voron-24-tophat-mod-for-cpap-and-exhaust)

---

## 🌀 Chamber Cooling (V0)

### V0 Auxiliary Cooling Fan

**Difficulté :** 🟢 Easy  
**Statut communauté :** 🧪 Experimental

| Modèle    | Compatible |
|-----------|-----------|
| V0 / V0.2 | ✅         |

Ventilateur auxiliaire monté sur le V0 pour refroidir la chambre. Indispensable si tu veux imprimer du **PLA** sur un V0 sans ouvrir le panneau avant.

- 🔗 [GitHub — JackJack3231 / V0-Auxiliary-Fan](https://github.com/JackJack3231/V0-Auxilliary-Fan)

---

## 🌡️ Chamber heating & temperature uniformity

> See also the [Filtration](filter.md) section for **Bed Fans** (EVENmore) which serve both to heat and homogenize the chamber.

### Recommended strategy by filament

| Filament | Target chamber temp | Part cooling | Notes |
|----------|--------------------|--------------|----|
| PLA | ≤ 25°C (open panel) | High | Do not heat chamber |
| PETG | ≤ 40°C | Medium | Closed chamber OK |
| ABS / ASA | 50–65°C | Low or off | Heated chamber required |
| PA / PC | 60–70°C | Off | Heated chamber + Nevermore |

> **Tip:** on V2.4, activate bed fans (EVENmore ou similaire) with a Klipper macro to homogenize temperature before starting the print. Saves 15–20 min per ABS session.
