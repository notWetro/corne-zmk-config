# Corne ZMK Config - KOY Layout

ZMK firmware configuration for Corne keyboard with German KOY layout, converted from Moonlander.

## Quick Start

### Option 1: GitHub Actions (Empfohlen)

1. **Erstelle ein neues GitHub Repository**
   ```bash
   cd ~/.config/Corne-Config
   git init
   git add .
   git commit -m "Initial commit: KOY layout from Moonlander"
   ```

2. **Pushe zu GitHub**
   ```bash
   # Erstelle ein neues leeres Repo auf GitHub (z.B. "corne-zmk-config")
   git remote add origin https://github.com/DEIN-USERNAME/corne-zmk-config.git
   git branch -M main
   git push -u origin main
   ```

3. **GitHub Actions aktivieren**
   - Gehe zu deinem Repository auf GitHub
   - Klicke auf "Actions" Tab
   - Aktiviere Workflows
   - Der Build startet automatisch

4. **Firmware downloaden**
   - Nach ~5-10 Minuten ist der Build fertig
   - Gehe zu "Actions" → Letzter Workflow Run
   - Download das "firmware" Artifact
   - Entpacke `corne_left.uf2` und `corne_right.uf2`

5. **Flashen**
   - Setze linke Hälfte in Bootloader-Modus (doppel-tap Reset-Knopf)
   - USB-Laufwerk erscheint
   - Kopiere `corne_left.uf2` auf das Laufwerk
   - Wiederhole für rechte Hälfte mit `corne_right.uf2`

### Option 2: Lokaler Build mit Docker

```bash
cd ~/.config/Corne-Config

# Build left
docker run --rm -v "$PWD":/workspace -w /workspace \
  zmkfirmware/zmk-build-arm:stable \
  sh -c "west init -l config && west update && west build -s zmk/app -b nice_nano_v2 -- -DSHIELD=corne_left"

# Build right  
docker run --rm -v "$PWD":/workspace -w /workspace \
  zmkfirmware/zmk-build-arm:stable \
  sh -c "west init -l config && west update && west build --pristine -s zmk/app -b nice_nano_v2 -- -DSHIELD=corne_right"

# Firmware ist in build/zephyr/zmk.uf2
```

## Layout Details

### Base Layer (0) - KOY
```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│DEL │ K  │ .  │ O  │ ,  │ Y  │      │ V  │ G  │ C  │ L  │ ß  │ Z  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ESC │H/⇧ │A/⌃ │E/⌥ │I/⌘ │ U* │      │ D  │T/⌘ │R/⌥ │N/⌃ │S/⇧ │ F  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│TAB │ X* │ Q* │ Ä* │ Ü* │ Ö* │      │ B  │ P  │ W  │ M  │ J  │ L6 │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
                │TG1 │MEH │SP/2│      │TB/4│ENT2│TG1 │
                └────┴────┴────┘      └────┴────┴────┘
```

**Tap-Dances (*):**
- U: tap=U, 2×tap=⌘Space (Spotlight)
- X: tap=X, 2×tap=⌘A (Alles markieren)
- Q: tap=Q, 2×tap=⌘X (Ausschneiden)
- Ä: tap=Ä, 2×tap=⌘C (Kopieren)
- Ü: tap=Ü, 2×tap=⌘V (Einfügen)
- Ö: tap=Ö, 2×tap=⌘⌥⇧V (Ohne Format einfügen)

### Layer 2/3: Symbole & Zahlen
- Layer 2: macOS Style (Option-Kombinationen)
- Layer 3: Linux/Win Style (Standard Brackets)
- Numpad rechts (7-9, 4-6, 1-3, 0)
- Symbole links (!@#$%&/()=)

### Layer 4: Navigation & Media
- Pfeiltasten (links/runter/hoch/rechts)
- Media-Steuerung (Prev/Play/Next)
- Lautstärke (Mute/Down/Up)
- Bootloader-Zugriff (oben rechts)

### Layer 6: F-Tasten
- F1-F12 auf der rechten Hälfte

### Layer 8: QWERTZ
- Standard deutsches QWERTZ Layout als Fallback

## Anpassungen

### Board Type ändern
Falls du nicht nice!nano v2 verwendest, ändere in `build.yaml`:
```yaml
board: nice_nano_v2  # → dein Board
```

Optionen:
- `nice_nano` (v1)
- `seeeduino_xiao_ble`
- `bluemicro840_v1`
- `nrfmicro_13`

### Home-Row Mods Tuning
In `config/corne.keymap` die `homerow_mods_*` Behaviors anpassen:
```c
tapping-term-ms = <280>;        // Haltezeit für Modifier
quick-tap-ms = <175>;           // Schnelltipp-Schwelle
require-prior-idle-ms = <150>;  // Verzögerung vor Aktivierung
```

### Tap-Dance Timing
```c
tapping-term-ms = <200>;  // Zeit zwischen Taps
```

## Dateien

- `config/corne.keymap` - Haupt-Keymap mit allen Layern
- `config/corne.conf` - Hardware-Konfiguration
- `build.yaml` - Build-Targets
- `west.yml` - ZMK Dependency Management
- `.github/workflows/build.yml` - GitHub Actions CI

## Support & Links

- **ZMK Docs**: https://zmk.dev/docs
- **ZMK Discord**: https://discord.gg/zmk
- **Visual Keymap Editor**: https://nickcoutsos.github.io/keymap-editor/

## Troubleshooting

**Build schlägt fehl?**
- Syntax in `.keymap` prüfen
- GitHub Actions Logs anschauen
- Board-Name in `build.yaml` korrekt?

**Tasten funktionieren nicht?**
- Keymap-Positionen prüfen (0-41 für 42 Tasten)
- Mit einfacher Keymap testen
- Matrix-Transform überprüfen

**Home-Row Mods zu empfindlich?**
- `tapping-term-ms` erhöhen (z.B. auf 300)
- `require-prior-idle-ms` erhöhen (z.B. auf 200)

**Bluetooth Probleme?**
- Pairing löschen und neu verbinden
- `CONFIG_BT_CTLR_TX_PWR_PLUS_8=y` in `.conf` überprüfen
