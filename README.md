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
