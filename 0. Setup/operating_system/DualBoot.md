# If you want to switch to Ubuntu
## We recommend Dual booting or using a Virtual Machine given that you will still need Zoom

## Creating an Ubuntu Virtual machine
Here is a [great tutorial](https://www.lifewire.com/install-ubuntu-linux-windows-10-steps-2202108)

## DualBoot Steps

### Backup your data

It's **very** important that all your data are backed-up before going further. Normally, things go well, but as we'll handle partitions on the hard drive, we might have difficulties. Better safe than sorry.

### Shrink Volume to prepare some space for Linux

We will take off 20GB from your hard drive to give it to Linux. You need to access [Disk Management](http://pcsupport.about.com/od/windows-8/a/disk-management-windows-8.htm). Then, right click on the **biggest** partition and select **Shrink Volume**. You want to get `30000` MB of space.

For this step, there is a [full tutorial](http://www.everydaylinuxuser.com/2015/11/how-to-shrink-windows-10-to-make-space.html) you can follow.

### Turn off Fast Startup

If you are running Windows 8+, you need to disable Fast Startup:

1. Right click -> Download this: [turn_off_fast_startup.bat](https://raw.githubusercontent.com/lewagon/setup/master/utils/turn_off_fast_startup.bat).
1. Right click on the downloaded file and click **Run as administrator**

**OR**

Go to **Energy Settings** -> **Power Button**. Click on "Change settings that are currently unavailable** if needed then you should be able to **disable FastBoot** or untick the **Turn on fast startup (recommended)** option (depends on the Windows version).

### USB stick

**One of the teacher or TA** should give you a bootable USB stick with [**Ubuntu 18.04 LTS 64 bits**](https://www.ubuntu.com/download/desktop). If not, you can create one yourself with [Etcher](https://etcher.io/).

### Install Ubuntu

1. Plug-in the USB stick, and restart your computer **holding the shift key**. A blue screen wil appear. If this does not work, follow [this procedure](https://support.microsoft.com/en-us/instantanswers/f40a95aa-1e34-4907-98ba-a308fd10a786/get-to-safe-mode-and-other-startup-settings-in-windows-10) to get to the "Other startup" setting.
1. Once the computer has restarted, you need to select the startup mode. Choose **Other options**
1. Choose **Use a Device**. You should see the USB stick in the list (EFI USB Device). Select it, this way, Windows will restart using the Linux key.

Ubuntu should boot in live mode. Time to install it!

1. Install Ubuntu in **english** and alongside with Windows. **Do not** tick **Third-Party** and **do not** tick **Update ...**.
1. **Keyboard** settings: press <kbd>@</kbd> <kbd>#</kbd> <kbd>/</kbd> to check they are working correctly.
1. Fill in **User Information**.
1. Restart your machine and unplug the USB stick.

When it's done, **check you can still boot on Windows**. The idea is that every time you boot your computer, you now have a menu to choose if you want to boot Windows **or** Linux.

Once again, restart the computer, boot on ubuntu, and follow [the UBUNTU setup guide](UBUNTU.md) to install Ruby & all the software we need!

Here are some tracks to solve issues when installing Ubuntu:

### No Devices choice at reboot

Make sure Windows FastBoot is disabled and restart in **Advanced Mode**.

### No OS choice at reboot

Disable Windows FastBoot **&** Bios FastBoot (see below).

**OR**

Access the Bios and change Boot option **ONE by ONE** <=> choose an option, save, reboot, if your problem persists, come back to default Boot option, choose another option and move on.

### Disable Bios FastBoot

1. Restart your machine in default mode and keep pushing on <kbd>F2</kbd> or <kbd>F11</kbd> or <kbd>Suppr.</kbd> to access the Bios.
2. Look for the boot options to disable the Bios FastBoot

## Verify
- Log into Ubuntu. Everything OK? Shut it down
- Log into Windows. Everything OK? Shut it down.
- Log into Ubuntu again. Everything OK? Congratulation, you have succesfully performed a **dual boot**. 

## Now, follow the installation steps on the [ubuntu.md tutorial](https://github.com/Strive-School/ai_setup/blob/master/operating_system/ubuntu.md)
