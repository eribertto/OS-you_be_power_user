In Linux, user management access works just like it
does in Windows. Different user types have
different privileges and they can be grouped together
with various access levels. There are a few differences in how Linux does labeling though. There are standard
users and there are also administrators in Linux. There's also a special
user called the root user. Don't get this confused with
the root directory or slash. The root user is
the first user that gets automatically created when
we install a Linux OS. This user has all the
privileges on the OS. They are the super user. There's technically only one
superuser or root account. But anyone that's
granted access to use their powers can be
called a superuser too. Now, let's try and view the contents of a
root restricted file. The file path has etc sudoers. We're getting an error, cat/ etc/ sudoers
permission denied. The sudoers file is a protected file that can
only be read by root. We can log in as root and then run this command, no problem. But it can be really dangerous
to always be in root. Since root, like our local
administrator account on Windows has unrestricted
access on the machine. If we make even one mistake, we could delete or
modify something important, and that's not good. So instead of
logging in its root, we can tell the shell
that we want to run this one command as root. So I'm so much to
the Windows UHC feature. That's because it is. On Linux, we can do this with the sudo command or superuser do. So sudo cat /etc/ sudoers. Now, we're able to see
the contents of this file. If you don't want to run sudo
every time you need to run a command that requires
root privileges, you can just use the su command
or substitute user. This will allow you to
change to a different user. If you don't specify user,
it defaults to root. Now, you can see my prompt
says root@cindy-nyc. Again, it's generally not a good guideline to stay logged
in as root all the time. There are lots of
critical services and files that can be
mistakenly changed. If you need to log in as root, it's okay. But just be careful. Just going ahead and
exit out of root for now and go back to
my normal user. You can view who has
access to run sudo by viewing the /etc/group file. This is also how you view
memberships for all groups. This looks a bit different
from the windows GUI. But you can see there are some similarities
to the Windows CLI. It's actually pretty
simple to read this file, even if you're not an expert yet. Each line represents
a different group. Let's look at the seudo line. There are four fields
here, separated by colons. The first field is
the group name. In this case, it's seudo. Second field is the
group password. We don't really need to specify a group password so it
defaults to the root password. The X here means that the
password has been encrypted and store in a separate
file that we'll talk about in a later lesson. The third field is the ID
of the group or group ID. When our operating system runs a task that involves a group, it uses a group ID
instead of group name. Finally, the last field is
lists of users in the group. What if you wanted to view
the users on our machine? What do you think
the file would be that stores that information? Unfortunately, it's
not /etc/user. The file that contains user
information is /etc/password. Wow, there's a lot
more information on here and a lot more users. Most of these accounts aren't actually humans
using the computer. They are a bunch of processes
that are constantly running on a computer that we need
to associate with a user. So our system has
lots of users with different permissions that are needed to run these processes. Let's look at
this first line here, which is an actual user
we can log into root. We won't talk about all the fields since
they aren't important. But the first three are relevant. The first field is the username and the second field
is the user password. The password isn't actually
stored in this file. It's encrypted and stored
in a different file, just like our group ID password. The third field here
is the user id or UID. Similar group IDS, user IDs or how our system
identifies a user, not by the username. Root has a UID of zero. That's basically how you view
users and groups in Linux.