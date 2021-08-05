At Linux, we also have special permissions. What if I want a user to be able to
do something that requires root privileges, but I don't want to give them these
privileges? What's the use case for this? Glad you asked. There are certain
commands that need to change files that are owned by root. Normally, if you need
to change a file owned by root, you'd have to use sudo. But we want it to be
able to have normal users change the files without giving them root access.
Let's check out an example. Let's say I want to change my password. I would use
a password command like we've learned. Pretty simple, right? Now I just enter in
my new password and my password is changed. We know that the password command
secretly scrambles up our passwords then add them to this etc shadow file. Let's
dive a little deeper into this file. Oh, it says this file's owned by root. How
are we able to write or scramble passwords in this file, it's owned by root.
Well, thanks to a special permission bit known as setuid we can enable files to
be run by the permission of the owner of the file. In this case, when you run
the password command, it's being run as root. Let's verify this. We see the
permissions on this file look a little odd. There's an S here where the x should
be. The s stands for setuid. When the s is substituted where irregular bit would
be, it allows us to run the file with the permissions of the owner of the file.
To enable the setuid bit, you can do it symbolically or numerically. The
symbolic format uses an s while the numerical format uses a 4, which you prepend
to the rest of the permissions like this. Similar to setuid, you can run a file
using group permissions with setgid or set group ID. This allows you to run a
file as a member of the file group. Under our group permissions, we can see that
the setgid bit was enabled, meaning that when this program is run, it's run as
group tty. To enable the setgid bit, you can do something similar to setuid. The
only difference is the numerical format uses a two. So, I can do something like
this or something like this. There's one last special permission bit we should
cover and that's the sticky bit. This bit sticks a file or folder down. It makes
it so anyone can write to a file or folder, but they can't actually delete
anything. Only the owner of root can delete anything. Let's look at permissions
for slash tmp directory or a lot of programs write temporary files to and you'll
see what I mean. I added the d flag to show information just for the directory
and not the contents. But as you can see, there's a special permission but at
the end here t, this means everyone can add and modify files in the slash tmp
directory, but only root or the owner can delete the slash tmp directory. You
can also enable the sticky bit using a numerical or symbolic format. The
symbolic bit is a t and the numerical bit is a one. So, sudo chmod plus t my
folder or sudo chmod 175 my folder. Works. So let's verify. That was a lot of
information on special bits. You usually won't have to deal with these
permission bits in a practical day-to-day manner but it's important to know they
exist in case you ever want to allow users to either share folders or even run
commands with escalated privileges. User access, group access, passwords, and
permissions are all core concepts in security. Right now, you're only working
with permissions and access on a single computer scale. Eventually, you'll learn
about access on multi-user levels across different networks and more in the next
course on system administration and IT infrastructure services. For now,
congratulations, you've just taken your first step toward building a foundation
of computer security knowledge. In the next module, we're going to switch gears
and talk about our OS and how it manages software. Next, we've got two
assessments for you covering Windows and bash permissions. Once you've finished,
you're granted permission to take a break before we hit the ground running in
the next module.