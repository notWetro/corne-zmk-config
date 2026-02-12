# Build Instructions for ZMK Firmware

## Method 1: Using GitHub Actions (Recommended)

1. **Fork the ZMK config template**
   - Go to: https://github.com/zmkfirmware/zmk-config-corne-template
   - Click "Use this template" or fork it

2. **Add your config files**
   ```bash
   # Clone your fork
   git clone https://github.com/YOUR-USERNAME/zmk-config.git
   cd zmk-config
   
   # Copy the config files
   cp ~/.config/Corne-Config/config/corne.keymap config/corne.keymap
   cp ~/.config/Corne-Config/config/corne.conf config/corne.conf
   
   # Commit and push
   git add config/
   git commit -m "Add KOY layout from Moonlander"
   git push
   ```

3. **Download firmware**
   - Go to your repo's "Actions" tab
   - Click on the latest workflow run
   - Download the firmware artifact
   - Extract the `.uf2` files

4. **Flash the keyboard**
   - Put left half in bootloader mode (double-tap reset or hold top-left key while plugging in)
   - Copy `corne_left.uf2` to the USB drive that appears
   - Repeat for right half with `corne_right.uf2`

## Method 2: Local Build (Advanced)

### Prerequisites
- Docker or Podman
- Python 3
- West build tool

### Steps

1. **Setup ZMK workspace**
   ```bash
   cd ~/
   python3 -m pip install --user -U west
   west init -l ~/.config/Corne-Config/
   cd zmk
   west update
   ```

2. **Build firmware**
   ```bash
   # Build left half
   west build -p -b nice_nano_v2 -d build/left -- -DSHIELD=corne_left -DZMK_CONFIG="$HOME/.config/Corne-Config/config"
   
   # Build right half
   west build -p -b nice_nano_v2 -d build/right -- -DSHIELD=corne_right -DZMK_CONFIG="$HOME/.config/Corne-Config/config"
   ```

3. **Flash**
   - Firmware will be in `build/left/zephyr/zmk.uf2` and `build/right/zephyr/zmk.uf2`
   - Copy to keyboard in bootloader mode

## Method 3: Using Docker (Easiest for local builds)

```bash
cd ~/.config/Corne-Config

# Build left
docker run --rm -v "$PWD":/zmk-config -w /zmk-config \
  zmkfirmware/zmk-build-arm:stable \
  west build -p -b nice_nano_v2 -d build/left -- -DSHIELD=corne_left

# Build right  
docker run --rm -v "$PWD":/zmk-config -w /zmk-config \
  zmkfirmware/zmk-build-arm:stable \
  west build -p -b nice_nano_v2 -d build/right -- -DSHIELD=corne_right
```

## Troubleshooting

### Build errors
- Make sure all syntax in `.keymap` is correct
- Check that board definition matches your hardware
- Review ZMK docs: https://zmk.dev

### Keys not working
- Verify the keymap positions match your physical layout
- Check if you need to adjust the matrix transform
- Test with a simple keymap first

### Bluetooth issues
- Clear bonding: Hold a specific key combination or use reset
- Re-pair the keyboard
- Check if `CONFIG_BT_CTLR_TX_PWR_PLUS_8=y` helps

### Home-row mods too sensitive
- Increase `tapping-term-ms` in the behavior definitions
- Adjust `require-prior-idle-ms` for more delay

## Board Selection

If you're not using a nice!nano v2, change `-b nice_nano_v2` to your board:
- `nice_nano` - nice!nano v1
- `bluemicro840_v1` - BlueMicro840
- `nrfmicro_13` - nRFMicro 1.3/1.4
- `seeeduino_xiao_ble` - Seeed XIAO BLE

For TyperActive-specific boards, check their documentation or let me know the model!

## Resources

- ZMK Documentation: https://zmk.dev/docs
- ZMK Discord: https://zmk.dev/community/discord/invite
- Keymap Editor: https://nickcoutsos.github.io/keymap-editor/
