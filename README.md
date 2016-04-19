# gc2035_binary
compiled eabi and eabihf

Use eabihf if your kernel is build with hf.

## instructions
git clone https://github.com/avafinger/gc2035_binary
copy gc2035.ko to /lib/modules/3.4.39/kernel/drivers/media/video/sunxi-vfe/device and overwite gc2035.ko
sync
depmod -a

Loading the driver (manually):
modprobe gc2035 hres=1
modprobe vfe_v4l2

tip:
For the best result, load with: modprobe gc2035 hres=0 mclk=34
