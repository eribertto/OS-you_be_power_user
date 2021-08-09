Now that we've gone a few practical things out of the way with disk partitioning
and file system creation, we can talk about concepts for a bit. Remember when we
talked about how our OS handles files? It actually manages the actual file data,
file metadata, and file systems. We've already covered file systems. In this
video, we're going to cover the file data and file metadata. When we talk about
data, we're referring to the actual contents of the file; like a text document
that we saved to our hard drives. The file metadata includes everything else,
like the owner of the file, permissions, size of the file, it's location on the
hard drive, and so on. Remember that the NTFS file system is the native file
system format of windows. So how exactly does NTFS store and represent the files
we're working with on our operating system? NTF uses something called The Master
File Table or MFT to keep everything straight. Every file on a volume has at
least one entry in the MFT, including the MFT itself. Usually, there's a
one-to-one correspondence between files and MFT records. But if a file has a
whole lot of attributes, there might be more than one record to represent it. In
this context, attributes are things like the name of a file, it's creation time
stamp, whether or not a file is read-only, whether or not the file is
compressed, the location of the data that the file contains, and many other
pieces of information. When you create files on an NTFS file system, entries get
added to the MFT. When files get deleted, their entries in the MFT are marked as
Free so they can get reused. One important part of a file's entry in the MFT is
an identifier called the file record number. This is the index of the files
entry in the MFT. A special type of file we should mention in Windows is called
a shortcut. A shortcut is just another file and another entry in the MFT. But it
has a reference to some destination, so that when you open it up, you can get
taken to that destination. You can create a shortcut by right-clicking on the
target file and selecting the Create Shortcut option. There it is. Besides
creating shortcuts as ways to access other files, NTFS provides two other ways
using hard and symbolic links. This might get a little weird but stay with me.
Symbolic links are kind of like shortcuts but at the file system level. When you
create a symbolic link, you create an entry in the MFT that points to the name
of another entry or another file. This might seem like just another way to make
a shortcut but symbolic links have a key difference. The operating system treats
them like substitutes for the file they're linked to in almost every meaningful
way. This is the part that sounds strange. So, let's demonstrate. Let's create a
directory on the desktop called Links. Inside of it, we'll create a text file
called file_1. And inside of that, let's add the word, Hello! And then, let's
make a shortcut that points this file called file_1 - Shortcut. Next, let's open
up a command prompt and navigate to this directory. Let's try to open up file_1
through its shortcut with Notepad. What do you think will happen? If you expect
the Notepad to display, Hello! Then you'd be disappointed. Instead, notepad
opened up the shortcut file which has some text in there that isn't readable by
us. Instead of a shortcut, let's create a symbolic link. You can create symbolic
links with the Make Link program from the command prompt. Let's make one called
file_1_symlink with the following command and then open it up a Notepad and see
what happens. All right, let's open it up in Notepad. This is what we mean when
we say the operating system treats the symbolic link just like the original
file. There's another type of link worth mentioning called a hard link. When you
create a hard link in NTFS, an entry is added to the MFT that points to the
linked file record number, not the name of the file. This means the file name of
the target can change and the hard link will still point to it. You can create
hard links in a way that's similar to symbolic links, but with the /H option. So
mklink /H file_1_hardlink file_1. Since a hard link points out the file record
number and not the file name, you can change the name of the original file and
the link will still work. Next, we'll have a look at how Linux organizes files
and the way it treats hard links and symbolic links. Onward and upward.