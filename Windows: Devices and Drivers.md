An important piece of software
that we've talked about, but haven't really seen in action,
is a driver. Remember that a driver is used to help
our hardware devices interact with our operating system. In this lesson, we're going to talk about
device drivers and how to manage them. First, let's talk about how to manage
the devices that our computer sees, and then we'll go over how we
install drivers for them. In Windows, Microsoft groups all of
the devices and drivers on the computer together in a single Microsoft management
console called the Device Manager. You can get to the Device Manager
in a couple of different ways. You can open up the Run dialog box and
type in devmgmt.msc. Or you can right-click on This PC,
select Manage, and click on the Device Manager option
in the left-hand navigation menu. I'm just going to open it up from here. Most devices you've got on your computer
will be grouped together according to some broad categories by Windows. So any displays you might be using
with your computer would show up under the Monitors section
in the Device Manager. Like so. This grouping usually happens
automatically when you plug in a new device. It's part of the plug and play system that Windows uses to automatically detect
new hardware plugged into your computer. It then recognizes and installs
the appropriate software to manage it. If you're interested, you can read more about the PnP
system in the supplementary reading. We'll give you an overview of how this
works too, so you can get a feel for it. When you plug a new device, like a mouse
or keyboard, into your computer, the Windows operating system will
go through a few steps to try and get it working. Most vendors or computer hardware
manufacturers will assign a special string of characters to their
devices called a hardware ID. When Windows notices that a new device has
been connected, the first thing it'll do is ask the device that's been
plugged in for its hardware ID. Once Windows has the new device's
hardware ID, the OS uses it to search for the right driver for the device. It looks for it in a few places, starting
with a local list of well-known drivers. Then it goes on to Windows Update or the driver store if it
needs to expand the search. Sometimes the device will come
with an installation disk, which contains custom driver software and
you can tell Windows to look there too. Finally, Windows will take
the driver software it found and install it so you can use your new device. Although this process mostly
happens automatically and behind the scenes, you can interact
directly with the Windows drivers through the Device Manager console
we mentioned earlier. You can expand any of the categories in
the Device Manager to view the devices inside them, like so. You can also use the all-powerful Windows
right-click to open up a menu with options to work with them. You can uninstall, disable, and
update a device driver from this menu. You can also tell Windows to look for hardware changes like
a newly plugged in device. Finally, if you choose Properties
from the right-click menu, you can see some details about
the device and its driver. Like its manufacturer and
the driver version being used. If you're interested in accessing
drivers through Windows CLI, check out the following reading for
more info.