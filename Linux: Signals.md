In Linux, there are lots of signals that we can send the processes. These
signals are labeled with names starting with sig. Remember the sigint signal, we
talked about before. You can use sigint to interrupted process and the default
action of this signal is to terminate the process that's interrupting. This is
true for Linux 2. You can send a sigint signal through the keyboard combination
Ctrl+C. Let's see this in action. I'm going to do the same thing as we did in
Windows and start a program like sudo parted. We can see that we're in the
parted tool now. Let's interrupt his tool and say we want it to abort the
process with the Ctrl+C keyboard combination. Now, we can see that the process
closed and we're back in our shell. We were able to interrupt our process midway
and terminate it. Success. There are lots of signals used in Linux, and we'll
talk about the most common ones in the upcoming lessons.