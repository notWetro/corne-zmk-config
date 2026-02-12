# Corne ZMK Configuration

This directory contains the ZMK configuration files converted from your Moonlander KOY layout.

## Files

- **corne.keymap** - Main keymap configuration with all 9 layers
- **corne.conf** - Hardware and feature configuration

## Layout Overview

### Base Layer (Layer 0) - KOY
Your main typing layer with:
- **Home-row mods**: H/Shift, A/Ctrl, E/Alt, I/Cmd on left | T/Cmd, R/Alt, N/Ctrl, S/Shift on right
- **Tap-dances**:
  - U: tap=U, double-tap=Cmd+Space (Spotlight)
  - X: tap=X, double-tap=Cmd+A (Select All)
  - Q: tap=Q, double-tap=Cmd+X (Cut)
  - Ä: tap=Ä, double-tap=Cmd+C (Copy)
  - Ü: tap=Ü, double-tap=Cmd+V (Paste)
  - Ö: tap=Ö, double-tap=Cmd+Opt+Shift+V (Paste without formatting)

### Other Layers
- **Layer 1**: Alternative base (Emacs-style, Ctrl instead of Cmd for modifiers)
- **Layer 2**: Symbols & Numbers (macOS style with Option key combinations)
- **Layer 3**: Symbols & Numbers (Linux/Windows style with standard brackets)
- **Layer 4**: Navigation & Media (arrows, media controls, volume)
- **Layer 5**: Reserved/Empty
- **Layer 6**: Function keys (F1-F12)
- **Layer 7**: Gaming/QWERTY (partial)
- **Layer 8**: QWERTZ German standard layout

## Key Differences from Moonlander

The Corne has **42 keys** (3x6 + 3 thumb keys per side) vs Moonlander's **72 keys**. Some keys were adapted:

1. **Missing thumb keys**: Moonlander has 7 thumb keys per side, Corne has only 3
2. **No number row**: Symbols/numbers are on layers 2 & 3
3. **Tap-dances simplified**: ZMK doesn't support complex tap-dance sequences like QMK
4. **Home-row mods**: Optimized timing for ZMK with hand-specific hold-trigger positions

## Installation

### For TyperActive Corne (or generic Corne)

1. Fork the official ZMK config repo: https://github.com/zmkfirmware/zmk-config-corne-template
2. Copy `corne.keymap` to `config/corne.keymap` in your fork
3. Copy `corne.conf` to `config/corne.conf` in your fork
4. Push to GitHub - firmware will build automatically via GitHub Actions
5. Download the `.uf2` file from the Actions tab
6. Flash to your keyboard by copying to the USB drive that appears in bootloader mode

### For TyperActive custom boards

If your TyperActive keyboard isn't a standard Corne, you'll need to:
1. Create a custom board definition in ZMK
2. Adjust the keymap for your specific layout
3. Let me know the model and I can help adapt this config!

## Customization

### Adjusting Home-Row Mods
If the home-row mods feel too sensitive or not sensitive enough, adjust these values in the `homerow_mods_*` behaviors:
- `tapping-term-ms`: How long to hold for mod activation (default: 280ms)
- `quick-tap-ms`: Rapid typing threshold (default: 175ms)
- `require-prior-idle-ms`: Delay before activation (default: 150ms)

### Adjusting Tap-Dances
Change `tapping-term-ms` in the `td_*` behaviors (default: 200ms)

### German Keycodes
The German keycodes (ä, ö, ü, ß, etc.) are mapped assuming macOS German keyboard layout. For Linux/Windows, you may need to adjust the definitions at the top of the keymap.

## Notes

- **Bootloader access**: Hold top-left key (Tab) while plugging in, or press bootloader key on Layer 4 or 5
- **Layer toggle**: Use the thumb cluster to toggle between layers
- **MEH key**: Ctrl+Shift+Alt
- **HYPR key**: Ctrl+Shift+Alt+Cmd

## Support

If you need help customizing or have issues, please let me know:
- Which TyperActive board model you have
- What changes you'd like to make
- Any errors you encounter during building/flashing
