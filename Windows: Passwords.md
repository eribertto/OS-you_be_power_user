In this video, we're going to talk about an important part of having users on a
machine, and that's working with passwords. Passwords add security to our user
accounts and machines, they make it so that only Marty knows the magic secret to
access her account and no one else's, not even the admin of the computer. When
setting up a password, you want to make sure that you and only you know that
password. Remember, if you're managing other people's accounts on a machine, you
shouldn't know what their password is. Instead, you want the user to enter the
password themselves. To reset a password in the gooey, let's go back to our
computer management tool. Under local users and groups, we're going to right
click on a username like this account Sarah. Let's click on properties. Then
from here, we're just going to check this box that says "user must change
password at next log on", then apply and hit "OK." Then, when the user logs into
the account, they'll be forced to change their password. If they forgot their
password, you have the option to set a password for them manually, by right
clicking and selecting set password. This has some caveats though, like losing
access to certain credentials. You can read more about this option in the
supplemental reading right after this video. To change a local password in power
shell, we're going to use the DOS style net command. There's a native power
shall command that can be used to set the password, but it's a little more
complicated. It requires a bit of simple scripting to use. For now, we'll stick
to the simpler, the less powerful net command. net does lots of different
things, changing local user passwords is just one of them. If you want to learn
more about what the net command can do, take a look at the documentation in the
supplementary reading for the command. Since this is an old DOS style command,
you can also use the slash question mark parameter to get help on the command
from the CLI. To change a password for a user, the command is net user then the
username and password. The best way to use this command, is to use an asterisk
instead of writing your password out on the command line. If you use an
asterisk, knit will pause and ask you to enter your password like so. Why is
this approach better? Imagine you're changing your password and right at that
moment someone walks behind you and glances over your shoulder. Your password
isn't a secret anymore. You should also know that in many environments, it's
common that the commands that folks run on the machines they use are recorded in
a log file that's sent to a central logging service. So it's best that passwords
of any kind are not logged in this way. Do you notice a problem with the
asterisk approach though? That's right. If I change passwords for someone else
using this command, I would know their password, and that's not good. Instead,
we're going to do what we did in the GUI and force the user to change the
default password on their next log on using the /logonpasswordchg:yes. So I'm
just going to force Victor to change his password on the next log on. So, net
user victor /logonpasswordchge:yes. The slash log on password change yes
parameter means that the next time that Victor logs into this computer, he'll
have to change his password. Sorry Victor.