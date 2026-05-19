# Corne Keyboard Layout - Neo Variant

ZMK configuration optimized for Vim/Neovim and Aerospace tiling window manager.

## Layer Overview

- **Layer 0**: Base (Neo-variant with Home-Row Mods)
- **Layer 1**: Symbols (Vim-optimized programming symbols)
- **Layer 2**: Numbers (Numpad + QWERTZ toggle)
- **Layer 3**: Lower (macOS shortcuts, Vim helpers, navigation, media)
- **Layer 4**: Raise (Aerospace WM shortcuts + F1-F12)
- **Layer 5**: QWERTZ (Standard German layout)

---

## Layer 0: Base (Neo-Variant)

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│DEL │ K  │ .  │ O  │ ,  │ Y  │      │ V  │ G  │ C  │ L  │ ß  │ Z  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ESC │H/⇧ │A/⌃ │E/⌥ │I/⌘ │ U  │      │ D  │T/⌘ │R/⌥ │N/⌃ │S/⇧ │ F  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│TAB │ X  │ Q  │ Ä  │ Ü  │ Ö  │      │ B  │ P  │ W  │ M  │ J  │ →4 │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
               │ →3 │SPC¹│BSPC│      │TAB │ENT¹│ →2 │
               └────┴────┴────┘      └────┴────┴────┘
```

**Home-Row Mods:**
- Links: H/Shift, A/Ctrl, E/Alt, I/Cmd
- Rechts: T/Cmd, R/Alt, N/Ctrl, S/Shift

**Thumb Cluster:**
- `→3` = Momentary Layer 3 (Lower)
- `SPC¹` = Space (hold: Layer 1 Symbols)
- `BSPC` = Backspace
- `TAB` = Tab
- `ENT¹` = Enter (hold: Layer 1 Symbols)
- `→2` = Momentary Layer 2 (Numbers)
- `→4` = Momentary Layer 4 (Raise)

**Timing:**
- Home-Row Mods: Hold 175ms for modifier
- Quick-tap: < 125ms prevents false triggers

---

## Layer 1: Symbols (Vim-Optimized)

**Access:** Hold Space or Enter

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│    │ !  │ @  │ #  │ $  │ %  │      │ ^  │ &  │ *  │ \  │ ?  │ `  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ "  │ <  │ [  │ {  │ (  │ /  │      │ |  │ )  │ }  │ ]  │ >  │ '  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ °  │ €  │ ~  │ =  │ +  │ -  │      │ _  │ :  │ ;  │    │    │ ´  │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
               │    │ __ │    │      │    │ __ │    │
               └────┴────┴────┘      └────┴────┴────┘
```

**Vim-Essential Characters:**
- `:` - Commands (easy reach!)
- `/` `?` - Forward/backward search
- `*` `#` - Word search
- `{}` `()` `[]` - Text objects & navigation
- `^` `$` - Line start/end
- `%` - Matching bracket jump
- `!` - Filter/shell commands

**Programming Symbols:**
- Brackets: `()` `{}` `[]` `<>`
- Operators: `+` `-` `*` `/` `=` `!` `?` `&` `|` `^` `%` `~`
- Quotes: `"` `'` `` ` ``
- Special: `@` `#` `$` `_` `:` `;` `,` `.` `\`

---

## Layer 2: Numbers (Numpad + Toggle)

**Access:** Hold right thumb (→2)

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│    │    │    │    │    │    │      │ /  │ 7  │ 8  │ 9  │ -  │    │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│BTCL│BT1 │BT2 │BT3 │BT4 │BT5 │      │ *  │ 4  │ 5  │ 6  │ +  │    │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│    │    │    │    │→5  │    │      │ =  │ 1  │ 2  │ 3  │ .  │    │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
               │    │    │    │      │    │ 0  │ __ │
               └────┴────┴────┘      └────┴────┴────┘
```

**Numpad (Right Side):**
- Standard layout: 789, 456, 123, 0
- Operators: `/` `*` `-` `+` `=`
- Decimal point: `.`

**Bluetooth Controls (Left Side):**
- `BTCL` = Clear all pairings
- `BT1-5` = Select profile 1-5

**Layer Toggle:**
- `→5` = Switch to QWERTZ layer (toggle)

---

## Layer 3: Lower (Shortcuts + Navigation)

**Access:** Hold left thumb (→3)

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│TAB │⌘+X │⌘+A │⌘+C │⌘+V │⌘+Z │      │ :  │ /  │ 8  │ 9  │ 0  │BSPC│
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│BTCL│BT1 │BT2 │BT3 │BT4 │BT5 │      │ ←  │ ↓  │ ↑  │ →  │    │    │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│SHFT│    │    │    │    │    │      │ ◀◀ │ ▶‖ │ ▶▶ │ 🔇 │Vol-│Vol+│
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
               │ __ │    │    │      │    │    │    │
               └────┴────┴────┘      └────┴────┴────┘
```

**macOS Shortcuts:**
- `⌘+X` = Cut
- `⌘+A` = Select All
- `⌘+C` = Copy
- `⌘+V` = Paste
- `⌘+Z` = Undo

**Vim Helpers:**
- `:` = Command mode (quick access!)
- `/` = Search

**Navigation:**
- Arrow keys: ← ↓ ↑ →

**Media Controls:**
- `◀◀` = Previous track
- `▶‖` = Play/Pause
- `▶▶` = Next track
- `🔇` = Mute
- `Vol-/Vol+` = Volume control

---

## Layer 4: Raise (Aerospace + F-Keys)

**Access:** Hold top-right corner (→4)

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│    │    │Layo│Rsz+│Rsz-│    │      │ F1 │ F2 │ F3 │ F4 │ F5 │ F6 │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│    │    │WS1 │Foc↓│Foc↑│Foc→│      │ F7 │ F8 │ F9 │F10 │F11 │F12 │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│    │    │MvL │Mv↓ │Mv↑ │Mv→ │      │⌘⇧4 │Bri-│Bri+│    │    │ __ │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
               │    │    │    │      │    │    │    │
               └────┴────┴────┘      └────┴────┴────┘
```

**Aerospace Shortcuts (Left - requires Ctrl+Alt+Shift+key):**
- `Layo` = Toggle layout (tiles/accordion)
- `Rsz+` = Increase window size
- `Rsz-` = Decrease window size
- `WS1` = Switch to workspace 1
- `Foc↓↑→` = Focus window (down/up/right)
- `MvL↓↑→` = Move window (left/down/up/right)

**Function Keys (Right):**
- F1-F12 in standard layout

**Utilities:**
- `⌘⇧4` = macOS screenshot tool
- `Bri-/Bri+` = Display brightness

---

## Layer 5: QWERTZ (Standard German)

**Access:** Press `→5` on Layer 2 (Numbers)
**Return:** Press bottom-right corner (→0)

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│TAB │ Q  │ W  │ E  │ R  │ T  │      │ Z  │ U  │ I  │ O  │ P  │ Ü  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ESC │ A  │ S  │ D  │ F  │ G  │      │ H  │ J  │ K  │ L  │ Ö  │ Ä  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│SHFT│ Y  │ X  │ C  │ V  │ B  │      │ N  │ M  │ ,  │ .  │ -  │→0  │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┼────┴────┘
               │CTRL│SPC │BSPC│      │RET │SPC │ALT │    │
               └────┴────┴────┘      └────┴────┴────┴────┘
```

**Standard QWERTZ:**
- German Umlauts: Ü, Ö, Ä
- Y/Z in QWERTZ positions
- No home-row mods (standard layout)

**Return to Base:**
- `→0` = Switch back to Layer 0 (Neo-variant)

---

## Shortcuts & Usage Tips

### Bluetooth Pairing
1. Hold →2 (Numbers layer)
2. Press `BTCL` to clear all pairings
3. Press `BT1-5` to select profile
4. Keyboard enters pairing mode

### Vim Workflow
1. `:` via Hold Space/Enter + right pinky (fast!)
2. `/` for search: Hold Space/Enter + top-right area
3. `{}` navigation: Hold Space/Enter + middle fingers
4. Repeat with `.`: Hold Space/Enter + bottom-right

### Aerospace Window Management
1. Hold →4 (Raise layer)
2. Use index/middle/ring fingers on left for:
   - Layout switching
   - Window focus
   - Window movement
3. Right hand free for F-keys or utilities

### Media Controls
1. Hold →3 (Lower layer)
2. Right bottom row:
   - Previous/Play/Next tracks
   - Mute/Volume controls

### QWERTZ Toggle
1. Hold →2 (Numbers layer)
2. Press position under BT4 (→5)
3. Returns to Neo-variant with →0 on QWERTZ layer

---

## Home-Row Mods Usage

**Typing Normally:**
- Tap quickly (< 125ms) → letter
- Fast consecutive typing → no false modifiers

**Using as Modifier:**
- Hold key (> 175ms) → modifier active
- Example: Hold A (Ctrl) + tap other keys

**Best Practices:**
- Type naturally, don't overthink
- 125ms idle time prevents false triggers
- Separate hand positions for hold-trigger

---

## Technical Details

- **Firmware**: ZMK
- **MCU**: nice!nano v2
- **Layout**: Corne 42 Keys (3x6 + 3 thumb per side)
- **Wireless**: Bluetooth 5.0
- **Display**: nice!view (shows layer names)
- **Battery**: Optimized for wireless operation

### Configuration Files
- `config/corne.keymap` - Layer definitions and behaviors
- `config/corne.conf` - Hardware features (ZMK Studio disabled)

### Build Process
Automatic via GitHub Actions:
1. Push changes to repository
2. Firmware builds automatically
3. Download `.uf2` files from Actions artifacts
4. Flash to keyboard in bootloader mode

---

## Customization Guide

### Adjusting Home-Row Mods
Edit `hml`/`hmr` behaviors in `config/corne.keymap`:
```c
tapping-term-ms = <175>;        // Hold time for modifier
quick-tap-ms = <125>;           // Fast-tap threshold
require-prior-idle-ms = <125>;  // Delay before activation
```

### Adding Custom Shortcuts
Layer 3 (Lower) or Layer 4 (Raise) can be extended with more shortcuts.
Use format: `&kp MODIFIER(KEY)` for combos.

Example:
```c
&kp LG(LS(N5))  // Cmd+Shift+5 (macOS screenshot)
&kp LC(LA(LS(KEY)))  // Ctrl+Alt+Shift+Key (Aerospace)
```

### Aerospace Configuration
Edit `~/.config/aerospace/aerospace.toml` to match Layer 4 shortcuts.
Current bindings use `ctrl-alt-shift` as base modifier.

---

## Keyboard Position Reference

```
Left Hand:                      Right Hand:
Col: 1   2   3   4   5   6      Col: 1   2   3   4   5   6
Row1 •   •   •   •   •   •      Row1 •   •   •   •   •   •
Row2 •   •   •   •   •   •      Row2 •   •   •   •   •   •
Row3 •   •   •   •   •   •      Row3 •   •   •   •   •   •
Thumb        •   •   •          Thumb    •   •   •
```

---

**Layout Created**: 2026-02-14
**Optimized For**:
- Vim/Neovim development
- Aerospace tiling window manager (macOS)
- German language typing (DE layout)
- Wireless operation (nice!nano v2 + nice!view)

**References**:
- [Aerospace Keybindings](~/.config/aerospace/aerospace.toml)
- [ZMK Documentation](https://zmk.dev/)
- [Full README](README.md)
