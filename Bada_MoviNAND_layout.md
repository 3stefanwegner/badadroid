#Bada MoviNAND partition layout.

# Basic info on Bada default partition layount on /dev/block/mmcblk0 #

/dev/block/mmcblk0p1: Bada systemfiles/mountpoints, and/or messages/email storage? < about 500MB ish

/dev/block/mmcblk0p2: contains the 400MB allocated user storage space that appears on a computer in mass storage mode

/dev/block/mmcblk0p3: appears to be where applications are installed? < about 1GB total

android kernel seems capable of mounting any of them using vfat


# Details #
**contents of /dev/block/mmcblk0p1:**

SystemFSISO
SystemFSMedia
SystemFSMediaSet
CSC
SystemFSPowerOnOff
Mass

**contents of /dev/block/mmcblk0p2:**

Images
Others
Sounds
Themes
Videos
SamsungNavigator

Galaxyboot  << our galaxyboot folder

**contents of /dev/block/mmcblk0p3:**

appex
bada