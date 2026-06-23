# Build Instructions

## Automatic (GitHub Actions) ⭐ Recommended

1. **Push to main** → Workflow triggers automatically
2. **Wait ~5 min** → Actions tab shows status
3. **Download** → Artifacts → `.uf2` files
4. **Flash**: Double-tap reset → Copy to USB

**Firmware files**: `corne_left.uf2` (left half) + `corne_right.uf2` (right half)

## Local Build with Docker

```bash
cd /path/to/config

# Build left
docker run --rm -v "$PWD":/zmk-config -w /zmk-config \
  zmkfirmware/zmk-build-arm:stable \
  sh -c "west init -l . && west update && west build -s zmk/app -b nice_nano_v2 -d build/left -- -DSHIELD=corne_left"

# Build right  
docker run --rm -v "$PWD":/zmk-config -w /zmk-config \
  zmkfirmware/zmk-build-arm:stable \
  sh -c "west init -l . && west update && west build -s zmk/app -b nice_nano_v2 -d build/right -- -DSHIELD=corne_right"

# Firmware: build/{left,right}/zephyr/zmk.uf2
```

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Build fails | Check `.keymap` syntax, review GitHub Actions logs |
| Keys don't work | Verify keymap positions (0-41), test with simple config |
| Bluetooth issues | Clear bonding (Layer 2: BT_CLR), re-pair |
| Home-row mods too sensitive | Increase `tapping-term-ms` or `require-prior-idle-ms` |

## Resources

- [ZMK Docs](https://zmk.dev) | [Codes Reference](https://zmk.dev/docs/codes)
- [Keymap Editor](https://nickcoutsos.github.io/keymap-editor/) | [Discord](https://discord.gg/zmk)
