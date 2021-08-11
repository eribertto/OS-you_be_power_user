Okay, now let's talk about how to view the processes running on our system in
Linux. We'll be using the ps command, so let's just go ahead and run that
command with the dash X flag, and see what happens. This shows you a snapshot of
the current processes you have running on your system. The ps output can be
overwhelming to look at at first, but don't worry, we'll walk through how to
read this output. Let's start from right to left here. P-I-D or PID is the
process ID, remember processes get a unique ID when they're launched. TTY, this
is the terminal associated with the process, we won't talk about this field but
you can read more about it in the manpages linked right after this video. STAT
this is the process status, if you see an R here it means the process is running
or it's waiting to run. Another common status you'll see is T for stopped,
meaning a process that's been suspended. Another one you might see is an S for
interruptible sleep, meaning the task is waiting for an event to complete before
it resumes. You can read more about the other types of process statuses in the
manpages. TIME, this is the total CPU time that the process has taken up. And
lastly, command, this is the name of the command we're running. Okay, now we're
going to enter hard mode here. Run this command, PS-EF. The E flag is used to
get all processes, even the ones run by other users. The dash F flag is for
full, which shows you full details about a process. Look at that, we have more
processes and even more process details. Let's break this down. UID is the user
ID of the person who launched the process. PID is the process ID, and PPID is
the parent ID that we discussed in earlier lesson which launched the process. C
is the number of children processes that this process has. STime is the start
time of the process. TTY is the terminal associated with the process. TIME is
the total CPU time that the process has taken up. And CMD or command is the name
of the command that we're running. What if we wanted to search through this
output? It's super messy right now, can you think of a way we can see if a
process is running? That's right, with the grep command, I told you we were
going to use it all the time. This will give us a list of process that have the
name Chrome in them. There's another way to view process information, remember
everything in Linux has a file, even processes. To view the files that
correspond to processes we can look into slash proc directory. There are a lot
of directories here for every process that's running. If you looked inside of
one of the subdirectories it'll give you even more information about the
process. Let's look at a sample process file for PID 1805. This tells us even
more information about a process state than what we saw in PS. While the slash
proc directory is interesting to look at, it's not very practical when we need
to troubleshoot issues with processes. For now stick with the PS-EF command to
look at process information. As you can see, we can learn a lot about the
processes running on our machine with just a few key strokes. In an upcoming
lesson we'll talk about how to use process information to our benefit when
figuring out which processes are taking up too many resources. For now, feel
free to learn a little more about the processes that you're running, I'll be
waiting for you in the next video.