# 📖 Glossary

> Common technical terms in the Voron community, organized by domain.

---

## 🖨️ Models & kinematics

| Term | Definition |
|------|-----------|
| **V0 / V0.2** | Voron 0.2 — compact 120mm format, 2 manual Z screws |
| **Trident** | Voron Trident — 3 automatic Z motors |
| **V2.4** | Voron 2.4 — 4 Z motors, the flagship official model |
| **Switchwire** | Voron Switchwire — Ender 3 conversion, moving bed |
| **CoreXY** | Kinematics where both XY motors move the toolhead together — high speed possible |
| **AWD** | All-Wheel Drive — 4 XY motors (2 front + 2 rear) for a very fast gantry |
| **QGL** | Quad Gantry Level — automatic 4-point leveling (V2.4) |
| **Z_TILT** | Automatic 3-point leveling (Trident) |

---

## 🔧 Mechanical

| Term | Definition |
|------|-----------|
| **Gantry** | The mechanical assembly carrying the toolhead (XY rails + crossbars) |
| **Backers** | Metal inserts in gantry extrusions to prevent thermal warping |
| **Front Idlers** | Front belt return pulleys that tension the XY belts |
| **AB Drives** | The two rear XY motors (A = left, B = right on V2.4) |
| **Kinematic mount** | Bed mount that allows thermal expansion without stress |
| **GE5C** | Type of metric ball joint used for Z joints |
| **Pin Mod** | Replacing XY joint screws with precision dowel pins |
| **BFI** | Beefy Front Idlers — stock front idler replacement |
| **Heat inserts** | Brass threaded inserts pressed into plastic with heat |

---

## 🔌 Electronics & wiring

| Term | Definition |
|------|-----------|
| **CANbus** | Communication protocol that replaces 20+ wires with 4 wires on the toolhead |
| **Toolhead board** | Small PCB mounted on the toolhead (EBB36, SB2209…) that handles everything locally via CAN |
| **CAN bridge** | Board that interfaces between the Raspberry Pi (USB) and the CAN bus (Octopus in bridge mode, U2C…) |
| **Katapult** | Open-source bootloader for flashing Klipper via CAN or USB without disassembly |
| **TMC2209 / TMC5160** | Stepper motor drivers with StealthChop (silent) and SpreadCycle control |
| **CB1** | BTT compute module (Raspberry Pi alternative) that plugs into Manta boards |
| **JST PH / XH** | Common miniature connectors on Voron (PH = 2mm pitch, XH = 2.5mm pitch) |
| **Molex** | Sturdier connector used for power and large components |
| **Ferrule** | Wire end crimp sleeve — essential for screw terminals |

---

## 🤯 Toolhead

| Term | Definition |
|------|-----------|
| **SB** | StealthBurner — official Voron toolhead (since 2022) |
| **CW2** | Clockwork 2 — the official extruder that pairs with SB |
| **Cartridge** | The hotend + printhead assembly that inserts into the SB |
| **Printhead** | The printed part holding the hotend in the SB |
| **Hotend** | The heated part that melts the filament (Dragon, Revo, Rapido…) |
| **Heatbreak** | The part between the hotend and heatsink that creates a cold zone |
| **Heat creep** | Heat traveling up into the cold zone — causes jams in the extruder |
| **Gear ratio** | Extruder reduction ratio — higher = more torque, better retraction |

---

## 🎯 Probes & leveling

| Term | Definition |
|------|-----------|
| **Probe** | Distance sensor to measure bed surface and compensate imperfections |
| **Eddy current** | High-resolution inductive probe technology (Beacon, Cartographer, IDM) |
| **Nozzle probe** | Probe that uses the nozzle itself as sensor (TAP, Boop) — no XY offset |
| **Klicky** | Magnetic mechanical probe — simple and reliable, less precise than eddy |
| **TAP** | Official Voron nozzle probe for SB |
| **Bed mesh** | Surface compensation map calculated by the probe before printing |
| **Z offset** | Distance between the probe reference point and actual nozzle position |

---

## 💾 Software

| Term | Definition |
|------|-----------|
| **Klipper** | Open-source firmware running partly on the Pi and partly on the mainboard |
| **Moonraker** | REST API between Klipper and web interfaces |
| **Mainsail** | Web interface to control Klipper (recommended by Voron) |
| **Fluidd** | Alternative to Mainsail |
| **KIAUH** | Klipper ecosystem installation script |
| **Input Shaper** | Klipper algorithm that compensates mechanical resonances for faster printing |
| **Pressure Advance** | Hotend pressure compensation for sharp corners |
| **Happy Hare** | Klipper extension dedicated to MMU systems (ERCF, TradRack) |

---

## 🔁 Multi-material

| Term | Definition |
|------|-----------|
| **MMU** | Multi-Material Unit — automatic filament change system |
| **ERCF** | Enraged Rabbit Carrot Feeder — the open-source reference MMU for Voron |
| **Filamentalist** | Passive self-rewinding spool holder, recommended with ERCF |
| **Tip forming** | Shaping the filament tip during a change — critical for reliability |
| **Cutter** | Blade integrated in the toolhead (Filametrix) to cleanly cut filament |
| **Purge** | Purge extrusion to change color/material — flushes the previous filament residue |

---

## 🌡️ Filtration & thermal

| Term | Definition |
|------|-----------|
| **VOC** | Volatile Organic Compounds — plastic fumes (mainly ABS, ASA) |
| **Nevermore** | Recirculating activated carbon filter — Voron community reference |
| **HEPA** | Fine particle filter — complements activated carbon |
| **Activated carbon** | Filtering medium that absorbs VOCs — saturates, needs regular replacement |
| **Chamber temp** | Enclosure temperature — critical for ABS/ASA |
| **CPAP** | Medical fan repurposed for high-performance part cooling |

---

## 🛒 Sourcing

| Term | Definition |
|------|-----------|
| **LDO** | LDO Motors — official Voron supplier, quality reference |
| **AliExpress / Ali** | Common source for budget parts (variable quality) |
| **BOM** | Bill Of Materials — complete list of required parts |
| **Self-sourced** | Build where you order each part individually (opposite of a kit) |
| **Kit** | Pre-packaged set of parts from a reseller |
