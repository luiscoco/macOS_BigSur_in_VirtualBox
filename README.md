# How to install macOs Big Sur in VirtualBox

How to install Mac **Big Sur 11** in VirtualBox on a PC:

https://www.youtube.com/watch?v=vQJrM7HqezQ

## 1. MacOS Big Sur download

Download the Mac Big Sur iso immage from this URL: 

https://archive.org/download/macos_iso

This is the direct link to the iso: 

https://archive.org/download/macos_iso/BigSur_11.7.1.iso

## 2. Virtual Machine download

https://www.virtualbox.org/wiki/Downloads

## 3. Commands for the installation

```
----------- Disable Hyper-V -------------

bcdedit /set hypervisorlaunchtype off



----------- Patch Virtual Machine ----------


# Intel Processor

cd "C:\Program Files\Oracle\VirtualBox\"

VBoxManage.exe modifyvm "VM Name" --cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff

VBoxManage setextradata "VM Name" "VBoxInternal/Devices/efi/0/Config/DmiSystemProduct" "iMac19,3"

VBoxManage setextradata "VM Name" "VBoxInternal/Devices/efi/0/Config/DmiSystemVersion" "1.0"

VBoxManage setextradata "VM Name" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Iloveapple"

VBoxManage setextradata "VM Name" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc"

VBoxManage setextradata "VM Name" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 0

VBoxManage setextradata "VM Name" "VBoxInternal/TM/TSCMode" "RealTSCOffset"


# AMD Processor

cd "C:\Program Files\Oracle\VirtualBox\"

VBoxManage.exe modifyvm "VM Name" --cpuidset 00000001 000106e5 00100800 0098e3fd bfebfbff

VBoxManage setextradata "VM Name" "VBoxInternal/Devices/efi/0/Config/DmiSystemProduct" "iMac19,3"

VBoxManage setextradata "VM Name" "VBoxInternal/Devices/efi/0/Config/DmiSystemVersion" "1.0"

VBoxManage setextradata "VM Name" "VBoxInternal/Devices/efi/0/Config/DmiBoardProduct" "Iloveapple"

VBoxManage setextradata "VM Name" "VBoxInternal/Devices/smc/0/Config/DeviceKey" "ourhardworkbythesewordsguardedpleasedontsteal(c)AppleComputerInc"

VBoxManage setextradata "VM Name" "VBoxInternal/Devices/smc/0/Config/GetKeyFromRealSMC" 0

VBoxManage modifyvm "VM Name" --cpu-profile "Intel Core i7-6700K"

VBoxManage setextradata "VM Name" "VBoxInternal/TM/TSCMode" "RealTSCOffset"



------------- Increase Display Resolution & Memory ----------------

cd "C:\Program Files\Oracle\VirtualBox\"

VBoxManage setextradata “VM Name” VBoxInternal2/EfiGraphicsResolution 1920x1080


Choose a Resolution:
  1280x720 | 1920x1080 | 2560x1440 | 2048x1080 | 3840x2160
    HD         FHD          QHD         2K          4K


VBoxManage modifyvm "VM Name" --vram 256
```







:
