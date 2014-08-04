local_manifest
==============

local_manifest for CM11.0 u8800pro compiling.
This is still a work in progress. Not ready for normal use.

Big thanks to herna, szezso, Ivan, desalesouche, SpaceKiller, CrysisLTU,Pikachhuki, Dazzzozo and many many others that I forgot to mention. Without these people we wouldn't have KitKat on this device!



Steps to follow

1. Setup your system for building android
2. install repo tool
3. init repo as below - so as to exclude groups which are not needed while building from linux

   repo init -u https://github.com/CyanogenMod/android.git -b cm-11.0 -g all,-notdefault,-darwin,-x86,-mips,-device
   
   NOTE : "-g all,-notdefault,-darwin,-x86,-mips,-device" - will hep you to save ~1GB of source download as these project groups are not needed in general
   
4. sync this code as below
   
   repo sync -j16 -c --no-clone-bundle
   NOTE: "--no-clone-bundle" again to reduce download size
