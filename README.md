## Is very experimental

Hallo,

I have make a littel patch for Armbian_5.24_Orangepizero_Ubuntu_xenial_3.4.113 whith Upgrade and 
Edimax EW-7811UTC AC600 whith RTL8812 or RTL8821 chipset.
The driver is wihtout fully Support for iw, wavemoon, and etc.

Driver work for Networmanager "nmtui-connect" 

My Source is from gnab.

But why not work "sudo apt-get install rtl8812au-dkms"

# Work on Armbian

sudo apt-get install binutils-arm-none-eabi gcc-arm-none-eabi

mkdir wlan-utc

git clone https://github.com/fixsmo/arm-rtl8812au.git wlan-utc

cd wlan-utc

make

sudo make install

sudo reboot

sudo nmtui-connect or sudo nmtui

# fine

option 
change in Makefile
from  CONFIG_PLATFORM_ARM_RPI = y CONFIG_PLATFORM_ARM_SUNxI = n

to    CONFIG_PLATFORM_ARM_RPI = n CONFIG_PLATFORM_ARM_SUNxI = y


# Have a good Day

# Bay


