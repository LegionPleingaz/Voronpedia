---
description: Gestionnaire de webcam(s) pour Klipper / Mainsail / Fluidd
---

# 📷 Crowsnest

> Crowsnest remplace MJPEG-streamer et ustreamer comme solution de streaming caméra pour Klipper. Il gère plusieurs caméras simultanément et s'intègre nativement avec Mainsail et Fluidd.

---

## Installation

### Via KIAUH (recommandé)

Crowsnest est disponible directement dans le menu KIAUH — c'est la méthode la plus simple.

```bash
./kiauh/kiauh.sh
# → Option 1 (Install) → Crowsnest
```

### Manuel

```bash
git clone https://github.com/mainsail-crew/crowsnest.git
cd crowsnest
make install
```

- 🔗 [GitHub — mainsail-crew / crowsnest](https://github.com/mainsail-crew/crowsnest)

---

## Détecter ta/tes caméra(s)

Once installed, use the helper script to list available cameras and their paths:

```bash
cd ~/crowsnest
tools/dev-helper.sh -c
```

Le résultat te donne les chemins `/dev/video*` à utiliser dans ta config.

---

## Basic configuration (`crowsnest.conf`)

```ini
[crowsnest]
log_level: verbose
delete_log: false

[cam 1]
mode: ustreamer
port: 8080
device: /dev/video0
resolution: 1280x720
max_fps: 15
```

**Available modes:**
- `ustreamer` — recommandé, faible latence, GPU acceleration sur Pi
- `camera-streamer` — pour les caméras CSI (module caméra Pi)

---

## Recommended cameras

| Caméra | Type | Résolution | Notes |
|--------|------|-----------|-------|
| Logitech C270 | USB | 720p | La moins chère qui fonctionne bien |
| Logitech C920 | USB | 1080p | Excellent rapport qualité/prix |
| Raspberry Pi Camera v2 | CSI | 8MP | Mode `camera-streamer` requis |
| Raspberry Pi Camera v3 | CSI | 12MP | Autofocus, meilleure option Pi |

---

## Timelapse

Crowsnest integrates with the **Moonraker Timelapse** plugin to create automatic timelapses of your prints.

- 🔗 [GitHub — mainsail-crew / moonraker-timelapse](https://github.com/mainsail-crew/moonraker-timelapse)

**Install via KIAUH:** Install menu → Moonraker Timelapse

---

## Stream access

Once running, the stream is accessible at:
- `http://[IP_DE_TON_PI]:8080/?action=stream` (ustreamer)
- Directly integrated in Mainsail / Fluidd in the Dashboard tab
