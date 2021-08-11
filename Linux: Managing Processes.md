Let's talk about how to use signals to manage processes in Linux. First up,
terminating processes. We can terminate a process using the kill command. It
might sound a bit morbid, but that's just how it is in the dog-eat-dog world of
terminating processes. The kill command without any flags sends a termination
signal or SIGTERM. This will kill the process, but it'll give it some time to
clean up the resources it was using. If you don't give the process a chance to
clean up some of the files it was working with, it could cause file corruption.
I'm going to keep a process window open so you can see how our processes get
affected as we run these commands. So, to terminate a process we'll used to kill
command along with the PID of the process we want to terminate. Let's just go
ahead and kill this Firefox process. And if we check the process window, we can
see that the process is no longer running. The other signal that you might see
pop up every now and then is the SIGKILL signal. This will kill your process
with a lot of metaphorical fire. Using a SIGTERM is like telling your process,
''Hey there process, I don't really need you to complete right now, so could you
just stop what you're doing?'' And using SIGKILL is basically telling your
process, ''OK, it's time to die.'' The signal does its very best to make sure
your process absolutely gets terminated and will kill it without giving it time
to clean up. To send a SIGKILL signal, you can add a flag to the kill command
dash kill for SIGKILL. So, let's open up Firefox one more time. So, kill dash
kill 10392, and now you can see that Firefox has been killed. These are the two
most common ways to terminate a process. But it's important to call out that
using kill dash kill is a last resort to terminating a process. Since it doesn't
do any cleanup, you could end up doing more harm to your files than good. Let's
say you had a process running that you didn't want to terminate but maybe you
just want to put it on pause. You can do this by sending the SIGTSTP signal for
terminal stop, which will put your process in a suspended state. To send this,
you can use the kill command with the flag dash TSTP. I'm going to run PS dash X
so you can see the status of the processes. We're just going to put this process
in a suspended state. So, kill dash TSTP. Now you can see the process 10754 is
now in a suspended state. You can also send the SIGTSTP signal using the
keyboard combination, Control Z. To resume the execution of the process, you can
use the SIGCONT for continued signal. Let's go and look at the process table
again. I'm going to go ahead and use that command on this process. Now, if I
look at the process again, you'll see that the process status turned from a T to
an S. SIGTERM, SIGKILL, and SIGSTP are some of the most common signals you'll
see when you're working with processes in Linux. Now that you have a grasp on
these signals, let's use them to help us utilize hardware resources better.