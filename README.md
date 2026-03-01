Firmware for: [Urchin Keyboard](https://github.com/duckyb/urchin)

## Getting started

**Are you trying to make your own ZMK firmware?**
[Here are the steps you need to take.](./GETTING_STARTED.md)

**Do you want to download my keymap?**
[Download the firmware zip from the latest action run.](https://github.com/duckyb/zmk-urchin/actions/workflows/build.yml?query=is%3Asuccess+branch%3Amaster) Check [the ZMK docs](https://zmk.dev/docs/user-setup#installing-the-firmware) for instructions on how to flash it.

## Keymap

34-key layout with [timeless homerow mods](https://github.com/urob/zmk-config#timeless-homerow-mods) in GACS order (GUI-Alt-Ctrl-Shift, pinky to index). HRMs are only on the base layer; all other layers use plain `&kp` bindings.

### Layer 0 — Default

```
╭──────┬──────┬──────┬──────┬──────╮   ╭──────┬──────┬──────┬──────┬──────╮
│  Q   │  W   │  E   │  R   │  T   │   │  Y   │  U   │  I   │  O   │  P   │
├──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┤
│ A    │ S    │ D    │ F    │  G   │   │  H   │ J    │ K    │ L    │ '    │
│ GUI  │ ALT  │ CTRL │ SHFT │      │   │      │ SHFT │ CTRL │ ALT  │ GUI  │
├──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┤
│  Z   │  X   │  C   │  V   │  B   │   │  N   │  M   │  , < │  . > │  / ? │
╰──────┴──────┴──────┼──────┼──────┤   ├──────┼──────┼──────┴──────┴──────╯
                     │ TAB  │ENTER │   │SPACE │ BSPC │
                     │      │  L2  │   │  L1  │      │
                     ╰──────┴──────╯   ╰──────┴──────╯
```

### Layer 1 — Symbols

Brackets use vertical pairing: same finger for open (home row) and close (bottom row).

```
╭──────┬──────┬──────┬──────┬──────╮   ╭──────┬──────┬──────┬──────┬──────╮
│  !   │  @   │  #   │  $   │  %   │   │  ^   │  &   │  *   │  _   │  =   │
├──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┤
│  -   │  +   │  €   │  "   │  '   │   │  ;   │  (   │  {   │  [   │  <   │
├──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┤
│  ~   │  `   │  \   │  |   │  /   │   │  :   │  )   │  }   │  ]   │  >   │
╰──────┴──────┴──────┼──────┼──────┤   ├──────┼──────┼──────┴──────┴──────╯
                     │      │ ESC  │   │      │      │
                     ╰──────┴──────╯   ╰──────┴──────╯
```

### Layer 2 — Numbers & Navigation

```
╭──────┬──────┬──────┬──────┬──────╮   ╭──────┬──────┬──────┬──────┬──────╮
│  1   │  2   │  3   │  4   │  5   │   │  6   │  7   │  8   │  9   │  0   │
├──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┤
│ CWRD │  .   │ UNDO │ REDO │  -   │   │ ESC  │  ←   │  ↓   │  ↑   │  →   │
├──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┤
│ INS  │SEL A │ CUT  │ COPY │PASTE │   │ MENU │ HOME │ PGDN │ PGUP │ END  │
╰──────┴──────┴──────┼──────┼──────┤   ├──────┼──────┼──────┴──────┴──────╯
                     │      │      │   │      │ DEL  │
                     ╰──────┴──────╯   ╰──────┴──────╯
```

### Layer 3 — Tri (hold both layer keys)

F-keys, mouse, media, and Bluetooth profile management.

```
╭──────┬──────┬──────┬──────┬──────╮   ╭──────┬──────┬──────┬──────┬──────╮
│  F9  │ F10  │ F11  │ F12  │ RCLK │   │ BRI- │ BRI+ │ MUTE │ VOL- │ VOL+ │
├──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┤
│  F5  │  F6  │  F7  │  F8  │ LCLK │   │CLS W │ M ←  │ M ↓  │ M ↑  │ M →  │
├──────┼──────┼──────┼──────┼──────┤   ├──────┼──────┼──────┼──────┼──────┤
│  F1  │  F2  │  F3  │  F4  │ MCLK │   │CLS T │ BT 0 │ BT 1 │ BT 2 │BT CLR│
╰──────┴──────┴──────┼──────┼──────┤   ├──────┼──────┼──────┴──────┴──────╯
                     │ BOOT │      │   │      │ BOOT │
                     ╰──────┴──────╯   ╰──────┴──────╯
```

## Display — nice!view with nice-view-gem

Both halves use [nice!view](https://nicekeyboards.com/docs/nice-view/getting-started/) displays running the [nice-view-gem](https://github.com/M165437/nice-view-gem) custom widget.

### What each half shows

- **Left (central):** Battery percentage, BLE profile status, active layer, and WPM chart. The dots at the bottom are BLE profile indicators (matching `BT 0`/`BT 1`/`BT 2` on the tri-layer), not switchable tabs.
- **Right (peripheral):** A gem crystal animation (currently disabled via `CONFIG_NICE_VIEW_GEM_ANIMATION=n` to save battery). With animation off, it shows a static frame.

### Display configuration (`config/urchin.conf`)

| Setting | Value | Purpose |
|---------|-------|---------|
| `CONFIG_ZMK_DISPLAY` | `y` | Enable display |
| `CONFIG_ZMK_DISPLAY_STATUS_SCREEN_CUSTOM` | `y` | Use nice-view-gem instead of the stock widget |
| `CONFIG_NICE_VIEW_GEM_ANIMATION` | `n` | Disable peripheral animation (saves battery) |
| `CONFIG_ZMK_WIDGET_BATTERY_STATUS_SHOW_PERCENTAGE` | `y` | Show battery as `%` instead of icon |
| `CONFIG_ZMK_WIDGET_WPM_STATUS` | `n` | Disable WPM widget |

### Creating a custom animation

The nice-view-gem animation is 16 monochrome bitmap frames cycled by LVGL. Replacing it with a custom animation is straightforward — the challenge is the pixel art, not the code.

**Frame specs:**
- 16 frames, each 69 x 68 pixels
- 1-bit color (black and white only, `LV_COLOR_FORMAT_I1`)
- ~620 bytes per frame, stored as C byte arrays

**Workflow to create a custom animation:**

1. Design 16 frames (69x68px, monochrome) in a pixel art editor (Aseprite, Piskel, GIMP, etc.)
2. Export each frame as a PNG
3. Convert PNGs to C arrays using the [LVGL image converter](https://lvgl.io/tools/imageconverter) with format `I1` (1-bit indexed)
4. Fork nice-view-gem and replace the frame data in `boards/shields/nice_view_gem/assets/crystal.c`
5. Update `config/west.yml` to point to your fork
6. Rebuild the firmware

**Key files in nice-view-gem:**

| File | Purpose |
|------|---------|
| `assets/crystal.c` | 16 frame bitmaps as C byte arrays |
| `widgets/animation.c` | Animation playback logic (~30 lines) |
| `widgets/screen_peripheral.c` | Peripheral screen layout, calls `draw_animation()` |
| `Kconfig.defconfig` | Animation toggle, frame selection, and timing |

**Animation Kconfig options:**

| Option | Default | Description |
|--------|---------|-------------|
| `CONFIG_NICE_VIEW_GEM_ANIMATION` | `y` | Enable/disable animation |
| `CONFIG_NICE_VIEW_GEM_ANIMATION_FRAME` | `0` | Static frame index (0-15) when animation is off |
| `CONFIG_NICE_VIEW_GEM_ANIMATION_MS` | `960` | Total animation duration in ms (960ms / 16 frames = 60ms per frame) |
