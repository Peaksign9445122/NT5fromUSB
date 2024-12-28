# NT5fromUSB
A Repository for Running Windows NT 5 from a USB Flash Drive Natively.


The goal of this project is to integrate USB drivers into as many NT 5 based Windows versions as possible.

This includes Windows XP (and its various editions), Windows Server 2003 (and its various editions), and Windows Embedded POSReady 2009.

Windows 2000 would normally also be included, but because of how it has different driver configurations, it may prove more difficult to slipstream.

Why would this be helpful in the first place? Well, as old hard drives from the '90s and 2000s start to fail, booting Windows from a USB may prove to be a reliable solution without having to spend money on another drive. The intended result is to use any old USB 2.0 Flash Drive that one may have lying around.

## How It Works
It's not actually that difficult to get Windows to boot off a USB Drive. I won't go into the technical details here, but all the information you need can be found in the link at the bottom of this page.

Essentially, the only things changed are that of the USB driver configurations. Normally the USB drivers are loaded in a separate phase of the system, but instead, we just move when the drivers load so Windows can use it as a installation and boot disk.

## Warnings
Because of the nature of how the drivers are reconfigured, they invalidate the original Windows Logo Driver Testing checksum, so during setup there will be many warnings on unsigned USB drivers. These can be ignored, but if you want 100% security, this isn't for you. In fact, don't use this old kernel base for anything seriously important. 

As another warning, because of how Windows would treat the USB drive as a normal hard drive, I am not responsible if the USB drive wears itself out and stops working. HDDs have significantly longer lifespans than USBs, after all.

## Current Builds Status
| Symbol | Status |
|:-----:|-----------------------|
| 🟩 | Completed and Available |
| 🟨 | Completed, but in Testing |
| 🟧 | Currently Under Development |
| ⬛ | Development Not Yet Begun |
| 🟥 | Not Possible |

<br>

⬛ Windows 2000 Professional SP4, x86

⬛ Windows XP Home Edition SP3, x86

⬛ Windows XP Professional SP3, x86

⬛ Windows XP Media Center Edition 2005 SP3, x86

🟨 Windows Server 2003 Standard SP2, x86

⬛ Windows Server 2003 Datacenter SP2, x86

⬛ Windows Embedded POSReady 2009 (details in progress)



<br>This will be continuously updated as more builds are integrated with the USB drivers.

Last Updated 28 December 2024

## Credits
This project wouldn't be possible without the work of <ins>Emanuel Schleussinger</ins> and <ins>Andrew Illarionov (Enderman)</ins>. They essentially found the necessary configurations necessary to make NT 5 run off a USB Drive.
I just simply implement their changes into Windows, all the credit goes to them.

All their details and discoveries can be found in the link here (currently hosted by Enderman): https://files.enderman.ch/documents/runwindowsxponusb.html
