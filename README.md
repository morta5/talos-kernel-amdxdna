# Automated Talos Kernel Builder with AMD XDNA (Ryzen AI NPU) Support

Dieses Repository baut automatisiert den offiziellen Talos Linux Kernel mit aktiviertem **`CONFIG_DRM_ACCEL_AMDXDNA=m`** für AMD Ryzen AI NPUs (XDNA/Krackan/Strix Point).

## Features
- **Effizient & Ressourcenschonend:** Läuft maximal 1x pro Woche (Sonntags um 03:00 UTC) per Cron.
- **Release-Check:** Prüft vor jedem Build, ob für das neueste Talos-Release bereits ein Image auf `ghcr.io` existiert. Wenn ja, wird der Build sofort übersprungen (keine unnötige Rechenzeit).
- **Manuell triggerbar:** Über GitHub Actions -> *Run workflow* kann jederzeit gezielt eine bestimmte Talos-Version gebaut werden (z. B. `v1.13.9`).
- **Ausgabe:** OCI-Image unter `ghcr.io/<owner>/kernel:<tag>` (kompatibel mit Talos Image Factory).
