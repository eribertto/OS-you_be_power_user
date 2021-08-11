Imagine you're starting up a video
game that's taking a while to render its graphics. You decide that you don't
want to play anymore, which leaves you with a few options. You can wait for it to finish loading and
then quit the game from the menu, or you can interrupt the process altogether,
telling it to quit at the system level. This is just one example of a time
you might find yourself wanting to close a process before it fully completes. To tell a process to quit at the system
level, we use something called a signal. A signal is a way to tell a process
that something's just happened. You can generate a signal with special
characters on your keyboard and through other processes and software. One of the most common signals
you'll come across is called SIGINT, which stands for signal interrupt. You can send this signal to a running
process with the CTRL+C key combination. Let's say you start up the DiskPart
tool we looked at in our discussion on partition formatting. I'm just going to open up command
prompt and then launch DiskPart. If you decide you don't want
to actually format any disks, you can hold down the CTRL key and press C at the same time to send
the SIGINT signal to the DiskPart process. You'll see that the window that the
DiskPart program was running in closes and the process terminates. There are a few other Windows signals
that processes can send and receive. But unlike in Linux,
there isn't an easy way for an end user to issue
arbitrary signal commands. If you're interested in learning
more about Windows signals, check out the signal reference
link in the supplementary reading.