Have you ever tried sending a file over to a coworker? What methods do you use?
Do you attach it to an email and send it, or do you copy the file to a USB drive
and then transfer the file that way? There are lots of ways to transfer files.
In this lesson, we're going to talk about a method that uses remote connection.
SCP, or secure copy, is a command you can use in Linux to copy files between
computers on a network. It utilizes SSH to transfer the data. So just like you
would SSH into a machine you can send a file that way. Let's see this in action.
Let's say you want to copy over a file from our computer to another computer. To
do this, we can run the SCP command with a few flags. So SCP, Desktop, myfile,
over to cindy@, In this command, we run the SCP command with the path of the
file we want to transfer to the user account, hostname, and path of where we
want to copy the file to. Now, it prompts us for the login information of the
computer we want to send the file to. After we enter this, we can verify that
the file successfully copied over. And there it is. The SCP command is a super
useful tool if you need to copy files to and from computers in a network. You
can read more about the command by checking out the Manpage.