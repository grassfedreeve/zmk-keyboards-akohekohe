# ʻākohekohe ZMK Module

This repository contains the shield files for the ['ākohekohe](https://github.com/grassfedreeve/akohekohe/) to allow users to build firmware. This can be done by adding the module to the west.yml found in your zmk-config's config directory. There is a full guide available for this here: [ZMK Modules Doc](https://zmk.dev/docs/features/modules)

## Usage

Edit your west.yml file found in your zmk-config's config directory to add the akohekohe module. Example:

```
manifest:
  remotes:
    - name: zmkfirmware
      url-base: https://github.com/zmkfirmware
    - name: caksoylar
      url-base: https://github.com/caksoylar
    - name: grassfedreeve
      url-base: https://github.com/grassfedreeve
  projects:
    - name: zmk
      remote: zmkfirmware
      revision: main
      import: app/west.yml
    - name: zmk-rgbled-widget
      remote: caksoylar
      revision: main
    - name: zmk-keyboards-akohekohe
      remote: grassfedreeve
      revision: main
  self:
    path: config
```
Once you have the module added to your west.yml you can then build firmware as if it was in your config's shield directory or in ZMK main.

# Default Keymap

The default keymap is provided in the module, here is a visual guide made using caksoylar's great [keymap-drawer](https://github.com/caksoylar/keymap-drawer)
![keymap](https://github.com/grassfedreeve/akohekohe/blob/main/img/example_keymap.svg)


# Extra Notes 

I would highly recommend anyone using bluetooth enable caksoylar's [zmk-rgbled-widget](https://github.com/caksoylar/zmk-rgbled-widget), which is so fantastic that anyone using a xiao ble should use it. I included it in the example west.yml for that very reason.
