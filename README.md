# SunvellR69
Stuff for running linux on the Sunvell R69 TV box

# legacy kernel

Factory Android "config_sys.bin"-file:

```sunvell_r69.original.fex```

FEX-file adapted for armbian (www.armbian.com):

```sunvell_r69.armbian.fex```

# mainline kernel - headless (no hdmi/TV-out)

Kernel device tree:

```sun8i-h2-plus-sunvell-r69.headless.kernel.dts```

u-boot device tree:

```sun8i-h2-plus-sunvell-r69.headless.u-boot.dts```

# mainline kernel - hdmi-support

Kernel device tree:

```tbd```

u-boot device tree:

```tbd```

# supported features (mainline)

- Ethernet
- WLAN
- eMMC
- both USB-ports configured as hosts
- audio deactivated by default, can be activated via DT-overlay
- IR deactivated by default, can be activated via DT-overlay
- blue LED as power-on indicator
- HDMI deactived by defaul (headless-version)

# build instructions using armbian (www.armbian.com)

See https://docs.armbian.com/Developer-Guide_Build-Preparation/ for details on kernel building with armbian (as of 12.2017).
```
# apt-get -y -qq install git
# git clone --depth 1 https://github.com/armbian/build
# cd build
# ./compile.sh BOARD=sunvell-r69


