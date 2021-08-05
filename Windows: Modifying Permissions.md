Now that we can read permissions, let's take it a step further and learn how to
change permissions in windows. Let's say we want to give access to another
person in my family to view a folder with family pictures on the computer. How
do I do that? On my Local Disk C, I have a folder called Vacation Pictures that
I want to share with another user on my machine, Devan. To do that, I'm going to
right click on this folder and go to Properties, then the Security tab. Now I
can see an option to Edit file permissions. I'm going to click on that. From
here, I can see that I can add a group or usernames to this ACL. I'm going to go
ahead and click Add. From here, it asked me to enter the username of the person
I want to add on this ACL. I'm going to enter devan and then click Check Names
to verify that I typed it in right. After it's been verified, I'm going to click
OK. Once devan's added to the ACL, I can click on his username, then check the
allow boxes for the permissions I want to give him. Let's give Devan modify
access, so you can add pictures to this folder too. That's it. We've kind of
been glossing over this other checkbox here Deny. You might have already guess
that Deny doesn't allow you to have a certain permission. But it's special
because it generally takes precedence over the allow permissions. Let's say
Devan is in a group that has access to this folder. If we explicitly check the
deny box for Devan's username, even if the group has access to the folder Devan
won't. Sorry, Devan. If you want to learn more bout permission precedence, you
can check out the supplemental reading. To modify a permission in the CLI, we're
going to return to the icacls command. In the examples I'm going to show you,
will be running icacls from PowerShell. The icacls command was designed for the
command prompt before PowerShell. And its parameters use special characters that
confuse PowerShell. By surrounding icacls parameters with single quotes, I'm
telling PowerShell not to try and interpret the parameter as code. If you run
these commands in command.exe, you'll need to remove the single quotes for them
to work. So let's look at this side by side with PowerShell.exe and command.exe.
In PowerShell, the command would be icacls 'C:\'Vacation Pictures\' /grant' with
single quotes, 'Everyone: (OI)(CI)(R). In command prompt, the command would be
icacls with double quotes "C\Vacation Pictures"/grant Everyone:(IO)(CI)(R).
We're going to see with this command does in just a moment. For now, let's take
a look at the difference in the quotes. In the PowerShell example, we add single
quotes to make PowerShell ignore the parentheses and because there's a space in
the path. In the command.exe example, we have to use double quotes for the path.
And we don't need the single quotes anymore to hide the parentheses. Got
it?Great. Now, let's take a look at the permissions that we just gave to Devan
with icacls. Cool. I see there's a new decal attach to the vacation pictures
directory for Devan, that gives him modify access. We can see that any new files
or folders that get created in vacation pictures will be inherited. So let's say
we want anyone with permission to use this computer to be able to see these
pictures. We don't want them to add or remove photos though. What permissions do
we want to give them? That's right. We want to give them read permission to the
Vacation's Picture folder. Let's use the special group Everyone to give read
permissions to the directory. So icacls 'C:\ Vacation Pictures' /grant
Everyone:(OI)(CI)(R). Success. The Everyone group includes, well, Everyone and
includes local user accounts like Cindy and Devan. Guest users: This is a
special type of user that's allowed to use the computer without a password.
Guest users are disabled by default. You might enable them in very specific
situations. Now anyone who can use this computer can browse the photos that
Devan and I have put together. Actually, maybe I didn't really want everyone to
look at my vacation photos. Maybe I just want the people that have passwords on
the computer to be able to see them. In that case, I want to use authenticated
users group. That group doesn't include guest users. So first, let's add a new
DACL. icacls 'C:\Vacation Pictures' /grant' Authenticated Users:(OI)(CI)(R).
Success. Now, let's remove the permissions for the Everyone group. icacls
'C:\Vaction Pictures' /remove Everyone. Success. Now, let's use icacls to verify
that the permissions are set away we intended. icacls 'C:\Vacation Pictures'.
Sweet. We can see the Authenticated Users were added and Everyone is removed.
Next, let's take a look at modifying permissions in Linux.