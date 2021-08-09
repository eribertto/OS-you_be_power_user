To begin interacting with the disk, we need to mount the file system to the
directory. You might be thinking, why can't we just cd into /dev/sdb? That's the
disk device, isn't it? It is, but if we try to cd into /dev/sdb like this We'd
get an error saying the device is not a directory, which is true. To resolve
this, we need to create a directory on our computer and then mount the file
system of our USB drive to this directory. Let's pull up where our partition is
with sudo parted -l. Okay, I can see that partition that we want to access is
/dev/sdb1. I've created a directory already under root called my_usb. So let's
give this a try. So sudo mount /dev/sdb1 /my_usb/. Now if we go to my_usb, we
can start reading and writing to the new file system. We actually don't need to
explicitly mount a file system using the mount command. Most operating systems
actually do this for us automatically, when we plug in a device like a USB
drive. File systems have to be mounted one way or the other, because we need to
tell the OS how to interact with the device. We can also unmount the file system
in a similar way using the umount command. Unmounting is the opposite of
mounting a disk. So now let's unmount the file system. I can either use sudo
umount /my_usb, or sudo umount /dev/sdb1. Both will work to unmount a file
system. When you shut down your computer, disks that were mounted manually are
automatically unmounted. In some cases, like if we were using a USB drive, we
just want to unmount the file system for the USB drive without shutting down.
Always be sure to unmount a file system of a drive before physically
disconnecting the drive. In the case of the USB drive, we can run into some
interesting file system errors if we don't do this. We'll talk more about this
in the upcoming lesson. Also, keep in mind that we when we use the mount command
to mount a file system to a directory, once we shut off the computer, the mount
point disappears. We can permanently mount a disk though if we needed to
automatically load up when the computer boots. To do this, we need to modify a
file called /etc/fstab. If we open this up now, you'll see a list of unique
device IDs, their mount points, what type of file system they are, plus a little
more information. If we want to automatically mount file systems when the
computer boots, just add an entry similar to what's listed here. Let's go ahead
and do that really quickly. The first field that we need to add for /etc/fstab
is the UUID or universally Unique ID of our USB Drive. To get the UUID of our
devices we can use this command, sudo blkid. This will show us the UUID for
block device IDs, aka storage device IDs, and that's it. We've covered a lot of
essential disk management tasks. So far we've partitioned a disk, added a file
system, and mounted it for use. If you're curious and want to learn more about
the /etc/fstab file and its options, check out the next supplemental reading.
Otherwise, let's move on