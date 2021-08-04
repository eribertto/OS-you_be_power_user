To change your password in Linux,
all you need to do is run the PASSWD or password command. Let's try changing my password. When you set a password it's
securely scrambled then stored in a special privileged file
called slash etc slash shadow. This file can only be read by Root,
to keep away prying eyes. Even if you did have access, you wouldn't be able to descramble
passwords found in here. If you're managing a computer, and
you want to force a standard user to change their password, like we did in
Windows, you can use the dash e, or expire flag with password, like this. This will immediately
expire a users password and then make them set a new password
the next time they log in.