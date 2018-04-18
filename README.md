# Sunvell R69
Stuff for running linux on the Sunvell R69 TV box

# legacy kernel

Factory Android "config_sys.bin"-file:

```sunvell_r69.original.fex```

FEX-file adapted for armbian (www.armbian.com):

```sunvell_r69.armbian.fex```

# mainline kernel 

Kernel device tree:

```sun8i-h2-plus-sunvell-r69.kernel.dts```

u-boot device tree:

```sun8i-h2-plus-sunvell-r69.u-boot.dts```

# supported features (mainline)

- Ethernet
- WLAN
- HDMI (works with 4.15, currently not with 4.16!)
- eMMC, boot from eMMC works
- both USB-ports configured as hosts
- audio deactivated by default, can be activated via DT-overlay
- IR deactivated by default, can be activated via DT-overlay
- blue LED as power-on indicator

# build instructions using armbian (www.armbian.com)

See https://docs.armbian.com/Developer-Guide_Build-Preparation/ for details on kernel building with armbian (as of 12.2017).
```
# apt-get -y -qq install git
# git clone --depth 1 https://github.com/armbian/build
# cd build
# ./compile.sh BOARD=sunvell-r69
```


