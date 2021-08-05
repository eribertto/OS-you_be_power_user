In Linux, we change permissions using
the chmod, or change mode, command. First, pick which permission
set you want to change. The owner, which is denoted by u,
the group the file belongs to, which is denoted by a g, or
other users, which is noted by an o. To add or remove permissions,
just use a plus or minus symbol that indicate
who the permission affects. Let's take a look at some examples. So that's chmod u+x my_cool_file. This command is saying that we
want to change the permission of my_cool_file by giving executable or
x access to the owner or u. You can do the same thing if you
wanted to remove a permission. So, chmod u-x my_cool_file. Instead of a plus, we just minus. Pretty simple, right? If you wanted to add multiple
permissions to a file, you could just do something like this. This is saying we want to add read and
execute permissions for the owner of my_cool_file. And you can do the same for
multiple permission sets. You do chmod ugo+r my_cool_file. Now, this says we want to add
read permissions for our owner, the group the file belongs to,
and all other users and groups. This format of using rwx and
ugo to denote permissions and users in chmod is known
as symbolic format. We can also change permissions
numerically, which is much faster and simpler, and
lets us change all permissions at once. The numerical equivalent of rwx is 4 for
read or r, 2 for write or w, and 1 for execute or x. To set permissions,
we add these numbers for every permission set we want to affect. Let's take a look at an example. The first number 7,
is our owner's permission. The second number, 5, is our group
permissions, and the third number, 4, is the permission for all other users. Wait a minute,
where are we getting 5 and 7? Remember, you have to add
the permissions together. If you add 4, 2, and 1 together,
you get rwx, which equals 7. So our owner permission is able to read,
write and execute this file. Can you guess what 5 would stand for? That's right? 4 plus 1 is read and execute. So now, you can see how numeric format
is quicker than symbolic format. Instead of running something like this, We can run chmod 754
my_cool_file to update them all. Either way, you can change permissions
using the symbolic or numerical format. Just pick whichever is easiest for you. You can also the owner and
the group of a file. The chown or change owner command allows
you to change the owner of a file. Let's go ahead and
change the owner to Devan. Awesome. And Devan is the owner of this file. And to change the group of file
belongs to, you can use a chgrp or change group command. Awesome. Now, the best group ever is
the group owner for this file. It may take a while for you to get the
hang of reading and changing permissions. You can practice changing the permissions
on a few files until you get it down. Permissions are an essential building
block to computer security, and you'll be using it throughout your
work as an IT Support Specialist.