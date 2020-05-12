# ASRock B450M Pro4 Hackintosh

This is a repository for the required kext and files to get a fully working Hackintosh on a ASRock B450M Pro4 motherboard.

**DISCLAIMER** I will not provide any support, use the Discord invite linked below. I am not responsible for any damage, you house blowing up or the unexpected divorce papers from your wife. I made this for my own convenience, but might be useful for other people using the same motherboard. Credit to the people who created 99% of the things in this repo.

**Todo:**
*Note:* I'm currently using a R3 2200g, which as audio issues under macOS and the iGPU is not compatible, so DRM and audio patching is pointless right now. I will be getting a R5 1600 Zen+  Refresh and a MSI RX560 2GB in the coming month.
 - [ ] DRM patch
 - [ ] Audio Patching
 - [ ] Update Opencore to 0.5.8
 - [ ] I'm likely missing other things

**Requirements:**
- macOS Catalina 10.15.4
- Opencore 0.5.7
- iMacPro1,1 SMBIOS
- macOS Catalina compatible graphics card
- A fully working brain
- ASRock B450M Pro4 motherboard (Pretty obvious)
- 3.90 BIOS (Should not matter which BIOS version your on, but a different version can affect your hack, I recommend updating if you have not done so) 

**How to use:**
 1. Download/clone the repo and unzip
 2. Replace your current OC folder with the one provided in this repo
 3. Open the config.plist with ProperTree and go to PlatformInfo > Generic
 4. Use GenSMBIOS to create a iMacPro1,1 SMBIOS and paste it accordingly into the config.plist then save
 5. Boot and install like a normal Mac. Then follow the Post-Install guide linked below
 
 **Useful Links:**
- [GenSMBIOS](https://github.com/corpnewt/GenSMBIOS), used the gernarate a iMacPro1,1 SMBIOS.
- [Opencore Desktop guide](https://dortania.github.io/OpenCore-Desktop-Guide/), guides you to create your hackintosh. 
- [ProperTree](https://github.com/corpnewt/ProperTree), a simple python based tool to edit and create .plist files such as your Opencore's config.plist.
- [AMD OS X Discord](https://discord.gg/EfCYAJW), the people here will help you with anything you need if you are having issues creating you hackintosh.

**Known Issues:**

- ~~USB 2.0 ports do not work under macOS. The USB 3.0 ports will work just fine. This only affects this motherboard. I will be finding a fix.~~ Thank you DhinakG for mapping the USB ports. All USB ports work as they should. Including the front panel USB and the USB 3.1 port.
- Any AMD APU (e.g Ryzen 3 2200g or Athlon 200GE) have severe audio issues in macOS. This affects all motherboards, not just this one. A workaround is to use a USB DAC or any audio device that uses it's own chipset.
- AMD APU's iGPU will not have graphics acceleration, this also affects all motherboards, since macOS does not have working drivers for it.
- Nvidia graphics cards will not work on Catalina or Mojave. This affects anyone using those cards. You must use High Sierra instead. RTX/16xx series cards will not work with any version of macOS.   
- No 32 Bit Support. This affects all AMD hacks. 
