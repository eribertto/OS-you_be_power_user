All righty, now that we've
learned how to list, create, and move around files in directories,
let's start removing them. In the Windows GUI,
if you wanted to remove a file or folder, just right-click and delete. The file ends up in the recycle bin,
which you can find on your desktop. If you wanted to restore a file here,
you could just right-click and Restore. If you empty your bin for any reason you
won't be able to retrieve those files. In PowerShell, the command to remove
files and directories is rm or remove. Take caution when using remove because
it doesn't use the recycle bin. Once the files and directories
are removed, they're gone for good. Let's remove a file called
text1.txt in my home directory. We can see, There it is. I'm just going to remove it. And now it's gone. The remove command might seem like
a dangerous weapon in the wrong hands. Fortunately, there are safety
measures in place that only give this ability to users that
are actually authorized to use it. We'll talk more about file
permissions in a different lesson. But let's take a quick
look at what I mean. Let's remove a file called
important_system_file. I get an error message saying that I don't
have permission to delete this file. In some cases like this one, it's because
it's been marked as a system file. In other cases, it might be because
I don't have enough permissions in the file system to remove the file. I do have the right permissions this time,
but since it is an important file, PowerShell wants to make sure
that I meant to do this. If I repeat the command with the -Force
parameter, remove will go ahead and remove the file. Let's take a look. -Force, And you can see the file's gone. If the file belongs to someone else,
or if I'm not an administrator, then I might not have the right
permissions to remove the file. In that case I'll need to access an
administrative account to remove the file. Okay, let's try removing
a directory with remove next. Here we go. Here's another place where PowerShell is
going to ask us if we really meant to do this. Since this is in a directory,
it contains other files. And we did not use the -Recurse parameter. We see a prompt asking us to confirm if we
really want to remove the directory and all its contents. We can say Yes or Yes to All to continue. We can also cancel this command and
run it again with the -Recurse parameter. That way, PowerShell knows that we
understand the consequences of what we're doing. So let's go ahead and
cancel this and try again. -Recurse. Yeah, now it's gone. And that's the remove
command in a nutshell. Again, because of
the nature of this command, you'll want to be extra careful
when removing files or directories.
