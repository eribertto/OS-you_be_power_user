We've talked a little bit about virtual machines before. We've also been using
virtual machines throughout the quick lab assessments. In this lesson, you're
going to learn how to install, manage and remove a virtual instance. A virtual
instance is just a single virtual machine. We're going to be using the popular
opensource virtualization software, Virtual Box, to manage virtual instances.
You'll find a link to download Virtual Box in the reading right after this
lesson. I'm currently using a Windows machine and in this lesson we're going to
set up and virtualize an ubuntu instance. I've already installed Virtual Box on
my machine. So let's go ahead and launch this application. We won't go through
all the menu items from Virtual Box, but we will talk about some of the main
ones. First step, how do we install a virtual instance? I've already
pre-downloaded an image of ubuntu from their website and saved it onto my
desktop but I have to install it somehow. Well, to install this, I'm just going
to click this new button here to create a new VM. I'm going to give my VM a name
and select the type and version of my OS. Just going to stick with the defaults.
Next it asks how much RAM I want to dedicate to this VM. One gigabytes is more
than enough for me so I'm just going to keep this and then continue. Now it asks
how much hard drive space I want to dedicate to this VM. I'm just going to keep
the default of 10 gigabytes and click Create. We're going to keep the default
values here and just skip through to the create. Awesome. You can read more
about these options in the supplemental reading. Now in my menu here I can click
Start and it'll start the VM. It will prompt me to select a media to launch
from, similar to booting a USB drive with the OS image on it. So I'm just going
to select the image I downloaded. And from, here the installation starts up.
That's pretty much it. Okay, what if we decide we want to use more than one
gigabyte for the OS? On a physical machine, we'd have to buy more RAM and
install it. But since we're using a VM, it's as easy as changing a setting. To
modify hardware resource allocation to a VM, all we need to do is right click on
the VM then click settings. From here, we'll be able to change how much RAM we
want along with other settings. We won't discuss the specifics of these
settings, but you can see how simple it is to modify a VM instance. Now, what if
we decide we don't want to use this VM anymore? If this is a physical machine,
we'd have to worry about where to store or recycle the hardware. For virtual
machines though, all we need to do is right click and select remove. From here,
it'll ask if we want to remove all files including the VM install itself or just
remove it from the list of VMs. Let's go ahead and delete all files. And that's
it in a nutshell. Super simple. If you want to learn more about how to use
Virtual Box or other virtualization software, don't forget to check out the
supplemental reading.