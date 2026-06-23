# Corne ZMK Configuration

ZMK firmware for Corne (42 keys) with Neo-variant layout optimized for Vim/Neovim and Aerospace tiling WM.

## Quick Start

1. **Build**: Push to main → GitHub Actions builds automatically
2. **Flash**: Download `.uf2` files from Actions → Enter bootloader (double-tap reset) → Copy to USB
3. **Edit**: Modify `config/corne.keymap` or `config/corne.conf` and commit

## Layers at a Glance

| Layer | Name | Purpose | Access |
|-------|------|---------|--------|
| 0 | Base | Neo-variant + home-row mods | Always |
| 1 | Symbols | Vim operators & programming symbols | Hold Space/Enter |
| 2 | Numbers | Numpad + QWERTZ toggle | Hold right thumb |
| 3 | Lower | macOS shortcuts, Vim helpers, media | Hold left thumb |
| 4 | Raise | Aerospace WM + F1-F12 | Hold corner thumb |
| 5 | QWERTZ | Standard German layout | Toggle on Layer 2 |

## Key Features

- **Home-row mods**: H/A/E/I(←) + T/R/N/S(→) with 175ms timing
- **Vim optimized**: `:` `/` `{}` `[]` `()` easily accessible
- **Aerospace integration**: Window manager shortcuts on Layer 4
- **German layout**: Umlauts (Ä/Ö/Ü/ß) built-in
- **Wireless**: nice!nano v2 + nice!view display

## Customization

### Home-Row Mods Timing
Edit `hml`/`hmr` in `config/corne.keymap`:
```c
tapping-term-ms = <175>;        // Hold time for mod
quick-tap-ms = <125>;           // Fast typing threshold
require-prior-idle-ms = <125>;  // Delay before activation
```

### Aerospace Shortcuts
Format: `&kp LC(LA(LS(KEY)))` = Ctrl+Alt+Shift+Key
Edit Layer 4 in `config/corne.keymap`

## Files

- `config/corne.keymap` - All layer definitions
- `config/corne.conf` - Hardware config (ZMK Studio disabled)
- `build.yaml` - GitHub Actions build config

## Hardware

- **MCU**: nice!nano v2
- **Display**: nice!view (layer names)
- **Wireless**: Bluetooth 5.0
- **Keys**: 3x6 matrix + 3 thumb per side

## Resources

- [ZMK Docs](https://zmk.dev) | [Keycodes](https://zmk.dev/docs/codes)
- [Aerospace](https://nikitabobko.github.io/AeroSpace/)
- [Detailed layouts](LAYOUT.md)

---

**Last updated**: 2026-06-23 | **Optimized for**: Vim/Neovim, Aerospace, German typing
