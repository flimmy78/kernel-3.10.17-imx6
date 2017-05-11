Linux kernel 3.10.17 for Advantech i.MX6 SMARC board (ROM5420-B1 2G).

1. Config and Build kernel

```
# source /opt/poky/1.5.3/environment-setup-cortexa9hf-vfp-neon-poky-linux-gnueabi
# make imx_v7_adv_defconfig
# make ARCH=arm menuconfig        // Configure kernel, you can skip if you want to use default config (imx_v7_adv_defconfig)
# make zImage LOADADDR=0x10008000 // You will find 'zImage' in arch/arm/boot/
# make uImage LOADADDR=0x10008000 // You will find 'uImage' in arch/arm/boot/
```

2. Compile dtb

```
# make imx6q-rom5420-b1.dtb       // The name of board is 'rom5420-b1', and you will find 'imx6q-rom5420-b1.dtb' in arch/arm/boot/dts/
```
