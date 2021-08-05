You might have noticed that we were
looking at permissions in the GUI before. There's a check box in the permission
list for special permissions. The permissions that we've
been looking at and setting so far are called simple permissions. Simple permissions are actually sets
of special, or specific permissions. For example,
when you set the re-permission on a file, you're actually setting
multiple special permissions. Let's take a look at the list of
special permissions available. I'm going to click on the advanced
tab under my permissions setting. When I click on a username, and
then go to Advanced Permissions, I can see a list of all the special
permissions enabled on that file. When we select a basic
permission like Read, we're actually enabling the special
permissions List folder / read data. Read attributes, read extended attributes,
read permissions, and synchronize, which are just
fine-tuned permissions. You can modify these permissions like
you would any other basic permission. Feel free to read more about the different
types of special permissions in the supplemental reading
I included after this video. In most cases, the simple permissions
are going to be all that you need. But sometimes,
you need to create a file or folder that doesn't quite
follow a simple pattern. Let's take a look at
an example in this CLI. To view special permissions
on a file in the CLI, we will simply use the icacls
command as before. Let's take a look at a more interesting
example than my desktop folder, icacls C:/Windows/Temp. This directory is used to hold temporary
files for all users in the system. We would like for everyone in the system
to be able to create files and folders here. You might think that we should use
modify or full control for this, but we don't want users to be able
to delete each others files. Let's take a look at some of
the DACLs assigned to this folder and figure out how to do this. First, local administrators and the
operating systems computer account have full permissions over this folder,
and all files and folders within it. We see a new descriptor, IO, which
indicates that this DACL is inherit only. That means that it will be inherited, but it is not applied to this
container C:\Windows\Temp. The users group includes all user
accounts on the local machine. We're going to let users WD,
or create files like data, AD, create folders and append data,
and S for synchronize. You can see in the next supplemental
reading that these special permissions are included in the modified
simple permission. Unlike the modify a simple permission, we are not granting users the ability
to delete files or folders. We do want users to be able to delete
their own files and folders, though, so how do we do that? So, if you see creator owner,
creator owner is a special user that represents the owner of
whichever file the DACL applies to. In this directory, and
all subdirectories, whoever owns a file or folder has full control of it. Nice, so I'm going to create a folder and file in C:\windows\temp and see what DACLs are applied. Let's use what we learned about
output redirection to record the output of the icacls in this file,
so icacls. Example for c:/Windows/Temp/example. Then we're going to use our redirector
output to give us icacls.txt. Okay, now let's look at the file we
created to view the output of icacls. Cool, I created the files, so
I have full control of them. And all of the other DACLs that we saw
in c:/windows/Temp have been inherited. You can see that using the specials
permissions in NTFS DACLs can be complicated, but it can also let you
create really powerful sets of permissions customized to your exact needs.