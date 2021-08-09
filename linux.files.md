In Linux, metadata and files are organized into a structure called an inode.
Inodes are similar to the Windows NTFS MFT records. We store inodes in an inode
table and they help us manage the files on our file system. The inode itself
doesn't actually store file date or the file name, but it does store everything
else about a file. In the last lesson, we learned how to create file shortcuts,
symbolic links, and hardlinks in Windows. Well in Linux we have the same
concept. Shortcuts in Linux are referred to as softlinks, or symlinks. They work
in a similar way symbolic links work in Windows, in that they just point to
another file. Softlinks allow us to link to another file using a file name.
They're great for creating shortcuts to other files. The other type of link
found in Linux are hardlinks. Similar to Windows, hardlinks don't point to a
file. In Linux, they link to an inode which is stored in an inode table on the
file system. Essentially, when you're creating a hardlink, you're pointing to a
physical location on disk or more specifically on the file system. But if you
deleted a file of a hardlink, all other hardlinks would still work. Let's
actually see where hardlinks are referenced. If we did an ls-l on this file,
important_file, You'll notice the third field in the details, this field
actually indicates the amount of hardlinks a file has. When the hardlink count
of a file reaches zero, then the file is completely removed from the computer.
To create a softlink, we can run the command ln with the flag -s for softlink.
So ln-s important_file important_file_softlink. To create a hardlink, we can run
the ln command without the -s to specify a hardlink. So ln important_file
important_file_hardlink. Now, if we check ls-l important_file, we'll see that
the hardlink count was increased by one. Hardlinks are great if you need to have
the same file stored in different places, but you don't want to take up any
additional space on the volume. This is because all the hardlinks point to the
same space on the volume. You could use softlinks to do the same thing. But what
if you moved one file, broke the softlink, and forgot about all the other places
that you used it? Those would be broken too and may take some time to clean up.
You may not see a use for making your own softlinks or hardlinks right now, but
they are used all throughout your system, so you should be aware how they work.