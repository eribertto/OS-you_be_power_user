You may remember that we introduced
the concept of a filesystem in the Technical Support Fundamentals course. Here's a refresher. A filesystem is used to keep track
of files and file storage on a disk. Without a filesystem, the operating system
wouldn't know how to organize files. So when you have a brand new disk or
any type of storage device, like a USB drive,
you need to add a filesystem to it. There are lots of file systems out there,
but the two that we'll talk about in this course are recommended as
default filesystems for Windows and Linux. For Windows, we use the NTFS filesystem,
and for Linux, it's recommended to use ext4. Filesystems have different
compatibilities with different OSes. Most of the time, cross operating
system support is minimal at best. Let's say you have a USB drive
that's using an NTFS filesystem. Both Windows and Linux's Ubuntu can
read and write to the USB drive. But if you have an ext4 USB drive,
it'll only work on Ubuntu and not on Windows, at least without
the help of third party tools. It's pretty likely that you'll encounter
this situation in an IT support role. Let's say you have some important files on
that same USB drive that you want to copy over to your Windows, Linux, and
Mac OSes, what would you do then? This is a pretty common situation. You'd have to reformat or
wipe the USB drive and add a filesystem that's compatible
with all three operating systems. Luckily, there are filesystems like
FAT32 that support reading and writing data to all three
major operating systems. FAT32 has some shortcomings though. It doesn't support files
larger than 4 gigabytes, and the size of the filesystem can't
be larger than 32 gigabytes. This might be enough for a small USB
drive, but it's not really great for anything else. You can learn more about FAT32 in
the next supplemental reading. This still begs the question, what if you
wanted to be able to share files between multiple OSes and don't want to
deal with filesystem limitations? Don't worry, we've got you covered. In the next course on
system administration and IT infrastructure services, we'll
discuss another filesystem type called network filesystems that
solves this exact problem. All right, now that you've got
a quick refresher on filesystems, let's spend the next few lessons
discussing how you actually set them up.