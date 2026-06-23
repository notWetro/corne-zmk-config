# Corne Layout - Neo Variant

6 layers optimized for Vim/Neovim + Aerospace tiling WM on macOS.

## Layer 0: Base (Neo)

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│DEL │ K  │ .  │ O  │ ,  │ Y  │      │ V  │ G  │ C  │ L  │ ß  │ Z  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ESC │H/⇧ │A/⌃ │E/⌥ │I/⌘ │ U  │      │ D  │T/⌘ │R/⌥ │N/⌃ │S/⇧ │ F  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│TAB │ X  │ Q  │ Ä  │ Ü  │ Ö  │      │ B  │ P  │ W  │ M  │ J  │ →4 │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
               │ →3 │SP/1│BSPC│      │TAB │EN/1│ →2 │
               └────┴────┴────┘      └────┴────┴────┘
```

**Home-row mods**: Left side H/A/E/I + Right side T/R/N/S (175ms timing)

## Layer 1: Symbols (Hold Space/Enter)

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│    │ !  │ @  │ #  │ $  │ %  │      │ ^  │ &  │ *  │ \  │ ?  │ `  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ "  │ <  │ [  │ {  │ (  │ /  │      │ |  │ )  │ }  │ ]  │ >  │ '  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ °  │ €  │ ~  │ =  │ +  │ -  │      │ _  │ :  │ ;  │    │    │ ´  │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
               │ __ │    │    │      │    │ __ │    │
               └────┴────┴────┘      └────┴────┴────┘
```

**Vim essentials**: `:` `/` `?` `{}()[]` `^$%` all accessible

## Layer 2: Numbers (Hold →2)

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

**Right**: Calculator numpad | **Left**: Bluetooth controls + QWERTZ toggle (→5)

## Layer 3: Lower (Hold →3)

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│TAB │⌘X  │⌘A  │⌘C  │⌘V  │⌘Z  │      │ :  │ /  │    │    │    │BSPC│
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│BTCL│BT1 │BT2 │BT3 │BT4 │BT5 │      │ ←  │ ↓  │ ↑  │ →  │    │    │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│⇧   │    │    │    │    │    │      │ ◀◀ │ ▶‖ │ ▶▶ │ 🔇 │V-  │V+  │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
               │ __ │    │    │      │    │    │    │
               └────┴────┴────┘      └────┴────┴────┘
```

**Left**: macOS (⌘) shortcuts + BT | **Right**: Navigation + Media

## Layer 4: Raise (Hold →4)

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

**Left** (Ctrl+Alt+Shift modifier): Aerospace WM | **Right**: F-keys + utilities

**Aerospace shortcuts**:
- `Layo` = Layout toggle (tiles/accordion)
- `Rsz±` = Resize windows
- `WS1` = Workspace 1
- `Foc/Mv` = Focus/Move window (↓/↑/→/←)

## Layer 5: QWERTZ (Standard German)

Toggle: Layer 2 → `→5` | Return: Layer 5 → bottom-right corner

```
┌────┬────┬────┬────┬────┬────┐      ┌────┬────┬────┬────┬────┬────┐
│TAB │ Q  │ W  │ E  │ R  │ T  │      │ Z  │ U  │ I  │ O  │ P  │ Ü  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│ESC │ A  │ S  │ D  │ F  │ G  │      │ H  │ J  │ K  │ L  │ Ö  │ Ä  │
├────┼────┼────┼────┼────┼────┤      ├────┼────┼────┼────┼────┼────┤
│⇧   │ Y  │ X  │ C  │ V  │ B  │      │ N  │ M  │ ,  │ .  │ -  │→0  │
└────┴────┴────┼────┼────┼────┤      ├────┼────┼────┼────┴────┴────┘
               │ ⌃  │SPC │BSPC│      │ENT │SPC │⌥   │
               └────┴────┴────┘      └────┴────┴────┘
```

Standard QWERTZ layout, no home-row mods.

---

## Configuration

### Timing (in `corne.keymap`)
- **Tapping-term**: 175ms (hold duration for modifier)
- **Quick-tap**: 125ms (fast typing threshold)
- **Prior-idle**: 125ms (delay before activation)

### German Keycodes (top of keymap)
```c
#define DE_Y Z          // Y/Z swapped for Neo
#define DE_SS MINUS     // ß
#define DE_AE SQT       // Ä
#define DE_OE SEMI      // Ö
#define DE_UE LBKT      // Ü
```

### Bluetooth (Layer 2/3)
- `BTCL` = Clear all pairings
- `BT1-5` = Select profile 1-5

---

## Usage Tips

### Vim Workflow
1. `:` via Hold Space + right pinky → quick commands
2. `/` for search → Hold Space/Enter + top-right
3. `{}` navigation → Hold Space/Enter + fingers

### Aerospace (Hold →4)
- Index/middle/ring: Window focus & movement
- Right hand: F-keys

### Media Controls (Hold →3)
- Bottom-right corner: Track + Volume

---

**Created**: 2026-02-14 | **Optimized for**: Vim/Neovim, Aerospace, German layout
