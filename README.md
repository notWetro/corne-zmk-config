# Corne ZMK Configuration

ZMK firmware configuration for Corne (42 keys) with Neo-variant base layout, optimized for Vim/Neovim and tiling window managers (Aerospace).

## Files

- **corne.keymap** - Main keymap configuration with 6 layers
- **corne.conf** - Hardware and feature configuration (ZMK Studio disabled)

## Layout Overview

### Base Layer (Layer 0) - Neo Variant
Your main typing layer with:
- **Home-row mods**: H/Shift, A/Ctrl, E/Alt, I/Cmd on left | T/Cmd, R/Alt, N/Ctrl, S/Shift on right
- **Optimized for German keyboard layout** with Umlauts (Ä, Ö, Ü, ß)
- **Quick access**: ESC on top-left homerow, DEL on corner

### Layer Structure
- **Layer 0**: Base - Neo-variant layout with home-row mods
- **Layer 1**: Symbols - Vim-optimized with `:` and `/` easily accessible
- **Layer 2**: Numbers - Numpad on right side + Toggle to QWERTZ
- **Layer 3**: Lower - macOS shortcuts (⌘+X/A/C/V/Z), Vim helpers (`:` `/`), arrow keys, media controls
- **Layer 4**: Raise - Aerospace window manager shortcuts (left), F-Keys F1-F12 (right)
- **Layer 5**: QWERTZ - Standard German QWERTZ layout (toggle via Layer 2)

## Key Features

### Vim/Neovim Optimization
- **Quick command access**: `:` and `/` on Layer 3 (Lower) for fast Vim commands
- **Symbol layer**: All Vim operators easily accessible (`{}`, `()`, `[]`, `*`, `#`, `%`, etc.)
- **Home-row mods**: Ctrl on A/N for `Ctrl+W`, `Ctrl+]` navigation

### Tiling Window Manager (Aerospace)
Layer 4 (Raise) includes Aerospace shortcuts with `Ctrl+Alt+Shift` modifier:
- **Layout control**: Toggle tiles/accordion, resize windows
- **Focus navigation**: Move focus between windows (left/down/up/right)
- **Move windows**: Relocate windows in workspace
- **Workspace switching**: Quick workspace access (WS1-4)

### Ergonomic Design
- **Home-row mods**: 175ms timing optimized for fast typing without false triggers
- **Numpad**: Right-side numpad on Layer 2 for calculator-style number entry
- **QWERTZ fallback**: Full QWERTZ layer for compatibility (Layer 5)
- **Media controls**: Volume, play/pause, track navigation on Layer 3

## Key Differences from Standard Layouts

The Corne has **42 keys** (3x6 + 3 thumb keys per side). Optimizations:

1. **Layered approach**: Numbers and symbols on layers instead of dedicated rows
2. **Home-row mods**: Modifiers accessible without leaving home position
3. **Thumb cluster utilization**: Layer switching and important keys on thumbs
4. **No ZMK Studio**: Disabled for predictable firmware behavior from keymap file

## Installation

### Building Firmware

1. Push changes to this repository
2. GitHub Actions will automatically build firmware
3. Download `.uf2` files from the Actions tab (artifacts)
4. Flash to your keyboard:
   - Enter bootloader mode (double-tap reset button)
   - Copy `corne_left-nice_nano_v2-zmk.uf2` to left half
   - Copy `corne_right-nice_nano_v2-zmk.uf2` to right half

### First-Time Setup

1. Fork or clone this repository
2. Enable GitHub Actions in your repository settings
3. Make changes to `config/corne.keymap` or `config/corne.conf`
4. Commit and push - firmware builds automatically

## Customization

### Adjusting Home-Row Mods
If the home-row mods feel too sensitive or not sensitive enough, adjust these values in the `hml`/`hmr` behaviors:
- `tapping-term-ms`: How long to hold for mod activation (default: 175ms)
- `quick-tap-ms`: Rapid typing threshold (default: 125ms)
- `require-prior-idle-ms`: Delay before activation (default: 125ms)

### Adjusting Aerospace Shortcuts
Edit Layer 4 (raise_layer) in `config/corne.keymap`. Current bindings use `LC(LA(LS(X)))` = Ctrl+Alt+Shift+X.

### German Keycodes
German keycodes (ä, ö, ü, ß) are mapped for macOS German keyboard layout. Definitions at top of keymap:
```c
#define DE_Y Z
#define DE_Z Y
#define DE_SS MINUS
#define DE_UE LBKT
#define DE_OE SEMI
#define DE_AE SQT
```

## Notes

- **Bootloader access**: Double-tap reset button on nice!nano
- **Layer switching**: 
  - Hold thumb keys for momentary layer access
  - `&to 5` on Layer 2 (Numbers) switches to QWERTZ
  - `&to 0` on Layer 5 (QWERTZ) returns to base layer
- **Bluetooth pairing**: Layer 2 & 3 have Bluetooth controls (BT_CLR, BT_SEL 0-4)
- **Display**: Supports nice!view - shows active layer name

## Hardware

- **MCU**: nice!nano v2
- **Display**: nice!view (optional)
- **Battery**: Built for wireless operation
- **Switches**: Compatible with MX or Choc switches

## Useful Resources

- [ZMK Documentation](https://zmk.dev/)
- [Keycodes Reference](https://zmk.dev/docs/codes)
- [Aerospace Documentation](https://nikitabobko.github.io/AeroSpace/)
- [Detailed layout diagrams](LAYOUT.md)

---

**Created**: 2026-02-14  
**Optimized for**: Vim/Neovim development, Aerospace tiling WM, German language typing
