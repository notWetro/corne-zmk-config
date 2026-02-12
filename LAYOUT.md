# Corne Keyboard Layout - KOY

Konvertiert vom Moonlander KOY Layout für ZMK.

## Layer Übersicht

- **Layer 0**: Base (KOY Layout mit Home-Row Mods)
- **Layer 1**: Lower (Zahlen, Navigation, Bluetooth)
- **Layer 2**: Symbols (Programmier-Symbole, Vim-optimiert)
- **Layer 3**: Numbers (Numpad rechts)
- **Layer 4**: Raise (Symbole & Funktionen)

---

## Layer 0: Base (KOY)

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│DEL │ K  │ .  │ O  │ ,  │ Y  │      │ V  │ G  │ C  │ L  │ ß  │ Z  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ESC │H/⇧ │A/⌃ │E/⌥ │I/⌘ │ U  │      │ D  │T/⌘ │R/⌥ │N/⌃ │S/⇧ │ F  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│TAB │ X  │ Q  │ Ä  │ Ü  │ Ö  │      │ B  │ P  │ W  │ M  │ J  │NUM │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
                │LWR │SPC*│BSPC│      │TAB │ENT*│NUM │
                └────┴────┴────┘      └────┴────┴────┘
```

**Home-Row Mods:**
- Links: H/Shift, A/Ctrl, E/Alt, I/Cmd
- Rechts: T/Cmd, R/Alt, N/Ctrl, S/Shift

**Thumb Cluster:**
- `LWR` = Layer 1 (Lower)
- `SPC*` = Space (hold: Layer 2 Symbols)
- `BSPC` = Backspace
- `TAB` = Tab
- `ENT*` = Enter (hold: Layer 2 Symbols)
- `NUM` = Layer 3 (Numbers)

**Timing:**
- Home-Row Mods: 175ms halten
- Tap: < 125ms

---

## Layer 1: Lower

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│TAB │ 1  │ 2  │ 3  │ 4  │ 5  │      │ 6  │ 7  │ 8  │ 9  │ 0  │BSPC│
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│BTCL│BT1 │BT2 │BT3 │BT4 │BT5 │      │ ←  │ ↓  │ ↑  │ →  │    │    │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│SHFT│    │    │    │    │    │      │Prev│Play│Next│Mute│Vol-│Vol+│
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
                │ __ │    │    │      │    │    │    │
                └────┴────┴────┘      └────┴────┴────┘
```

**Funktionen:**
- **Zahlenreihe**: 0-9 für schnellen Zugriff
- **Bluetooth**:
  - `BTCL` = Bluetooth Clear (alle Pairings löschen)
  - `BT1-5` = Bluetooth Profile 1-5 wählen
- **Navigation**: Pfeiltasten rechts (Vim-Style: HJKL Position)
- **Media Controls**:
  - `Prev` = Previous Track
  - `Play` = Play/Pause Toggle
  - `Next` = Next Track
  - `Mute` = Mute/Unmute
  - `Vol-` = Volume Down
  - `Vol+` = Volume Up

---

## Layer 2: Symbols (Vim-optimiert)

**Zugriff:** Space oder Enter halten

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│    │ !  │ @  │ #  │ $  │ %  │      │ ^  │ &  │ *  │ /  │ ?  │ `  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ "  │ <  │ (  │ {  │ [  │ \  │      │ |  │ ]  │ }  │ )  │ >  │ '  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ ´  │ €  │ ~  │ =  │ +  │ -  │      │ _  │ :  │ ;  │ ,  │ .  │ °  │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
                │    │    │ __ │      │ __ │    │    │
                └────┴────┴────┘      └────┴────┴────┘
```

**Vim-relevante Zeichen:**
- `:` (Commands) - Homerow rechts, leicht erreichbar
- `/` `?` - Suche vorwärts/rückwärts
- `*` `#` - Wortsuche
- `{}` `()` `[]` - Text-Objekte & Navigation
- `^` `$` - Zeilenanfang/-ende
- `%` - Matching bracket jump
- `!` - Filter/Shell

**Programmier-Symbole:**
- Klammern: `()` `{}` `[]` `<>`
- Operatoren: `+` `-` `*` `/` `=` `!` `?` `&` `|` `^` `%` `~`
- Quotes: `"` `'` `` ` ``
- Sonderzeichen: `@` `#` `$` `_` `:` `;` `,` `.` `\`

---

## Layer 3: Numbers (Numpad)

**Zugriff:** Rechts unten (R21) halten oder drücken

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│    │    │    │    │    │    │      │ /  │ 7  │ 8  │ 9  │ -  │    │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│    │    │    │    │    │    │      │ *  │ 4  │ 5  │ 6  │ +  │    │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│    │    │    │    │    │    │      │ =  │ 1  │ 2  │ 3  │ .  │    │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
                │    │    │    │      │    │ 0  │ __ │
                └────┴────┴────┘      └────┴────┴────┘
```

**Numpad rechts:**
- Standard Numpad-Layout: 789, 456, 123, 0
- Operatoren: `/` (Division), `*` (Multiplikation), `-` (Minus), `+` (Plus), `=` (Gleich)
- Dezimalpunkt: `.`

---

## Layer 4: Raise

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│TAB │ !  │ @  │ #  │ $  │ %  │      │ ^  │ &  │ *  │ (  │ )  │BSPC│
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│CTRL│    │    │    │    │    │      │ -  │ =  │ [  │ ]  │ \  │ `  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│SHFT│    │    │    │    │    │      │ _  │ +  │ {  │ }  │ |  │ ~  │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
                │    │    │    │      │    │ __ │    │
                └────┴────┴────┘      └────┴────┴────┘
```

---

## Tastatur-Positionen Referenz

```
Links:                          Rechts:
 1   4   7  10  13  16           1   4   7  10  13  16
 2   5   8  11  14  17           2   5   8  11  14  17
 3   6   9  12  15  18           3   6   9  12  15  18
            19  20  21                  19  20  21
```

---

## Shortcuts & Features

### Bluetooth Pairing
1. Drücke `LWR` (L19) für Layer 1
2. Drücke `BTCL` (L2) um alle Pairings zu löschen
3. Drücke `BT1-5` (L4-L8) um Profil zu wählen
4. Keyboard geht in Pairing-Modus

### Bootloader
- Layer 4 oder 5 aktivieren → oben rechts Taste drücken

### Home-Row Mods richtig nutzen
- **Tippen**: Schnell < 125ms → normaler Buchstabe
- **Halten**: > 175ms → Modifier aktiv
- **Schnelles Tippen**: Zwischen Tasten < 125ms → kein Modifier

### Vim Workflow
1. `:` via Space+Homerow-rechts-2 (sehr schnell!)
2. `/` für Suche: Space+Homerow-rechts-6
3. `{}` Navigation: Space+L10/L13
4. Zeichen wiederholen mit `.`: Space+R15

### Media Controls
1. Halte `LWR` (L19)
2. Nutze rechte untere Reihe:
   - `Prev` = Vorheriger Track
   - `Play` = Play/Pause
   - `Next` = Nächster Track
   - `Mute` = Stumm schalten
   - `Vol-/Vol+` = Lautstärke

---

## Technische Details

- **Firmware**: ZMK
- **Board**: nice!nano v2 (oder kompatibel)
- **Layout**: Corne 42 Keys (3x6 + 3 Thumb)
- **Wireless**: Bluetooth 5.0
- **Display**: nice!view (optional)

### Build
Automatischer Build via GitHub Actions:
https://github.com/notWetro/corne-zmk-config/actions

### Flash
1. Download `.uf2` Files von GitHub Actions
2. Keyboard in Bootloader-Modus (doppel-tap Reset)
3. `corne_left.uf2` → linke Hälfte
4. `corne_right.uf2` → rechte Hälfte

---

## Anpassungen

### Home-Row Mods zu langsam/schnell?
In `config/corne.keymap`:
```c
tapping-term-ms = <175>;        // Haltezeit (aktuell 175ms)
quick-tap-ms = <125>;           // Schnelltipp-Schwelle
require-prior-idle-ms = <125>;  // Verzögerung vor Aktivierung
```

### Andere Symbole/Zeichen benötigt?
Layer 2 in `config/corne.keymap` anpassen.

---

**Layout erstellt**: 2026-02-12
**Letzte Änderung**: Media Controls zu Lower Layer hinzugefügt
