File permissions are an important concept in computer security. We only want to
give access to certain files and directories to those who need it. While we
think about how we want users to access files and folders, we should also think
about how the concept of permissions carries over to other areas of your life.
Maybe you've locked down your social media post to only people you trust, or
giving a copy of your house key to a relative in case of an emergency. You'll
learn more about security principles in the last course of this program. For
now, we're going to focus on one small building block, file permissions. In
Windows, files and directory permissions are assigned using Access Control Lists
or ACLs. Specifically, we're going to work with Discretionary Access Control
Lists or DACLs. Windows files and folders can also have System Access Control
Lists or SACLs assigned to them. SACLs are used to tell windows that it should
use an event log to make a note of every time someone accesses a file or folder.
This is a more advanced topic which you can read up on in the next supplementary
reading. You can think of a DACL as a note about who can use a file and what
they're allowed to do with it. Each file or folder will have an owner and one or
more DACLs. Let's take a look at an example. In windows explorer, I have opened
up my home directory. If we right click on desktop and select properties, we can
see the properties dialog for our desktop directory. And if we go to a security
tab, we can see the permissions window here. The top box contains a list of
users and groups. And the bottom box has a list of the permissions that each
user group has been assigned. What do each of these permissions do? It changes a
bit depending on whether the permission is assigned to a file or a directory.
Don't worry, it all makes sense soon. Let's do a rundown of these permissions.
Read, the Read permission lets you see that a file exists, and allows you to
read its contents. It also lets you read the files and directories in a
directory. Read and Execute, the Read and Execute permission lets you read
files, and if the file is an executable, you can run the file. Read and Execute
includes Read, so if you select Read and Execute, Read will automatically be
selected. List folder contents, List folder contents is an alias for Read and
Execute on a directory. Checking one will check the other. It means that you can
read and execute files in that directory. Write, the Write permission lets you
make changes to a file. It might be surprising to you, but you can have write
access to a file without having read permission to that file. The write
permission also lets you create sub directories and write two files in the
directory. Modify, the Modify permission is an umbrella permission that include
read, execute and write. Full control, a user or group with full control can do
anything they want to the file. It includes all of the permissions of Modify,
and adds the ability to take ownership of a file and change its ACLs. Now, when
we click on my username, we can see the permissions for Cindy, which show that
I'm allowed all of these access permissions. If we want to see which ACLs are
assigned to a file, we can use a utility designed to view and change ACLs called
ICACLs or Improved Change ACLs. Let's take a look at my desktop first. ICACLs,
Desktop. Well, that looks useful. But what does it mean? I can see the user
accounts that have access to my desktop, and I can see that my account is one of
them. But what about the rest of this stuff? These letters represent each of the
permissions that we talked about before. Let's take a look at the Help for
ICACLs, I bet that'll explain things. So ICACLs, slash, question. All right.
There's a description of what each one of these letters means. The F shows that
I have full control of my desktop folder. ICACLs causes full access, and we saw
this in the GUI earlier as full control. These are the same permission. What are
these other letters mean? NTFS permissions can be inherited as we saw from the
ICACLs help. OI means Object Inherit, and CI means Container Inherit. If I
create new files or objects inside my Desktop folder, they'll inherit this DACL.
If I create new directories or containers in my desktop, they'll also inherit
this DACL. If you'd like to understand more about ACL inheritance and NTFS,
check out the next supplemental reading.