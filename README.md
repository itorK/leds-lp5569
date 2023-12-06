# leds-lp5569
This is experimental module as a LED driver for NBG7815 device.

Usage:
1. Put module in the openwrt path -> /openwrt/package/kernel

2. make menuconfig and add a support for this driver as a module

3. Compile openwrt distro or just module(and send to the router):
```
make V=sc package/kernel/leds-lp5569/compile
```

4. Play fun with leds as example:


   original Zyxel Armor G5 router ready pattern
```
root@OpenWrt:~# echo 17 > /sys/devices/platform/soc/78b6000.i2c/i2c-0/0-0032/led_pattern
root@OpenWrt:~# echo 1 > /sys/devices/platform/soc/78b6000.i2c/i2c-0/0-0032/run_engine
root@OpenWrt:~# echo 17 > /sys/devices/platform/soc/78b6000.i2c/i2c-0/0-0035/led_pattern
root@OpenWrt:~# echo 1 > /sys/devices/platform/soc/78b6000.i2c/i2c-0/0-0035/run_engine
```


