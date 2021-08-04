We talked about using the CLI in-depth in the last module. We've seen how it can
make our tests quicker when we modify files and folders. Now, we're going to
start using commands to help us with other tasks on our system. Imagine you're
working as an I.T. support specialist at a company and your boss asks you to
check all the user information on 10 machines, to make sure that the local
administrator account is not enabled. Sure you could search computer management
in the search bar, click computer management local, look under system tools,
click on local users and groups, then double click on the username of the
computer to ensure that their local administrator account is enabled. Now, you
just have to do that nine more times. There's a much faster way. You can just
use the CLI to quickly see the list of users on the computer using the command
Get-LocalUser. As you can see, it lists my user account, a few other users and a
couple of other default accounts that are part of Windows. Here you can see that
my local administrator account isn't enabled. That's way easier. What about
groups? I bet you can guess, Get-LocalGroup will list the groups on the local
machine. There are a whole bunch of groups but don't worry, these are all
built-in groups. Each of them are important, but we aren't likely to make
changes to most of them. One that we will make changes to is the administrators
group. Remember, this group controls who has administrative access to the
machine. It's important to know who's in this group since anyone in this group
can make any change they want to the machine. We just saw in the GUI that we're
in this group, but I wonder who else is? Let's see who's in this group with
Get-LocalGroupMember, and I want to check the administrators group. We can see
that the administrator user and my user are in the administrators group but no
one else. Looks good to me. One last note, these local user and group PowerShell
commands require that your running PowerShell 5.1 or newer. You may have noticed
that I keep saying local accounts and local users. If your organization has a
lot of Windows machines, it's very common to use active directory to manage user
accounts in a central directory service. We'll learn more about active Directory
accounts in our next course on system administration and I.T. infrastructure
services. But let's focus on local accounts for now.