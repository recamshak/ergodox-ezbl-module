# ErgoDox EZBL

A drop-in board for the ErgoDox EZ keyboard, using a Nice!Nano V2 running [ZMK](https://zmk.dev), giving you Bluetooth connectivity without any modifications to the case.

## Features

- Drop-in replacement for the original ErgoDox EZ PCB, no modifications to the case needed
- Bluetooth wireless via Nice!Nano V2
- [ZMK Studio](https://zmk.studio) support for real-time keymap editing

## Usage

Add this module to your ZMK config's `west.yml`:

```yaml
manifest:
  remotes:
    - name: ergodox-ezbl
      url-base: https://github.com/recamshak/ergodox-ezbl-module
  projects:
    - name: zmk
      remote: ergodox-ezbl
      revision: main
      import: app/west.yml
  self:
    path: config
```

Then reference the `ergodox_ezbl_left` and `ergodox_ezbl_right` shields in your build configuration.
