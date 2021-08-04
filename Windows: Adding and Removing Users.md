Okay. Now that you know how to view information about users and the hierarchy of
user permissions, let's learn how to add and remove users on a machine. To add a
user, we're going to go back to our computer management tool. Under local users
and groups, we're going to right click and select New User. From here, it asks
us to set a username, a full name, and a password. Remember, that in order to
use good password setting practices, we set a default password and then make the
user change that password when they log in. So, we're going to go ahead and set
a default password, and make sure the box for, "user must change password at
next log on" is checked, and then click Create. So I'm just going to make a new
user account for Elizabeth and have the password, and then just make sure that's
checked, and hit Create. And that's how you create a new local user. To remove a
user, we simply right click and select Delete. This gives us a warning message
that says, user names are unique, and even if you delete the user and give them
the exact same username, they won't be able to access their old resources. Once
you confirm that you want to do that, just go ahead and click delete it. And
that's how you remove a local user account. Adding and removing local user
accounts from the CLI, is going to use the same net command that we use to
change passwords, just with different parameters. Like before, there's a native
power shell command, new dash local user, that requires a little bit of
scripting to use. If you want to use new dash local user, check out the
supplemental reading. Now, back to net. To add a new local user, we simply use
the slash add parameter. If we add the slash add parameter to the same command
we used before, it instructs net to create the account. We can still use the
asterisk for the password to be prompted to enter a password. Let's test this
out and create a new account for Andrea. So, net user andrea * / add. Now, let's
list the user accounts to be sure it worked. So, Get-LocalUser. Sweet. There it
is. Now, there's a small problem which you saw in the earlier lesson on
passwords. This account is for Andrea, but we know what the password is. We
don't want to know what the password is because that means we can log in as
Andrea. We want to make sure that Andrea changes her password to something that
we don't know. So, we're going to flag her account as requiring a password
change using the slash log on password change yes parameter. So, net user andrea
/ logonpasswordchg:yes. Now you all know whather password is. You can actually
combine these two commands that we ran to create a new account that requires a
password change at first login. Let's create an account for Cesar. So, net user
cesar pa5swOrd / add / logonpasswordchg:yes. Now, when we run the Get-LocalUser,
we should see both of our new accounts. Sweet. And there it is. Cesar's new
account has a password that you know and you can give it to him, but he'll have
to change the password the first time he logs in. All right. Now let's remove
these accounts that we just created. I'm going to show you how to do this using
net, and using Remove-LocalUser. Both of these commands will do the exact same
thing. So let's delete Andrea's account, net user andrea /del. This will delete
Andrea's account. And using the Remove-LocalUser cesar, we can remove Cesar's
account. Sweet, now it's gone. See how each of these options follows a pattern.
The net user example, looks just like it did to create a new user account,
except instead of adding an account, we deleted the account. In the second
example, instead of getting, setting, or creating a new dash local user, we
removed the account. As you continue to learn new CLI commands, you'll start to
notice these sorts of patterns. Being able to identify these patterns will help
you discover new things that you can do, and remember how to do things you
haven't done in a while.