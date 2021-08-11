It might feel like we're starting to get into the weeds here. So let's take a
step back and think about what processes really are and what they represent in
the context of an operating system. You can think of processes as programs in
motion. Consider all the code for your Internet browser. It sits there on your
hard drive quietly waiting for its time to shine. Once you start it up, the
operating system takes that resting code then turns it into a running,
responding, working application. In other words, it becomes a process. You
interact with launch and halt processes all the time on computers, although the
OS usually takes care of all that behind the scenes. By learning about
processes, you're taking a peek behind the curtain at how operating systems
really work. This knowledge is both fascinating and powerful, especially when
applied by a savvy IT support specialist to solve problems. Keep all that in
mind as we take a look at how you can pull back the curtain even further. Next,
we'll learn about the different ways you can investigate which processes are
running on a Windows computer and more methods of interacting with them. On the
Windows operating system, the task manager or task mgr.exe is one method of
obtaining process information. You can open it with the control shift escape key
combination or by locating it using the start menu. If you click on the
processes tab, you should see a list of the processes that the current user is
running along with a few of the system level processes that the user can see.
Information about each process is broken out into columns in the task manager.
The task manager tells you what application or image the process is running
along with the user who launched it and the CPU or memory resources it's using.
To kill a process, you can select any of the process rows and click the end task
button in the lower right corner. We can demonstrate this by launching another
notepad.exe process from the command line, then switching over to the task
manager, selecting the notepad.exe process and ending it. I already have Notepad
open so I'm going to click on it, click end task. In an earlier lesson, we
talked about starting and ending Windows processes. Remember that we used the
task kill command to stop a process by its identification number or PID. So how
do we get that PID number? While in task manager, you can click on the details
menu option and here, you can see a whole bunch of other information you can get
the task manager to display, including the PID. You can also see this
information from both a command prompt and PowerShell. From the command prompt,
you can use utility called TaskList to show all the running processes. From a
PowerShell prompt, you can use a Commandlet called Get-Process to do the same.
There are lots of ways you can get process information from the Windows
operating system. We've included links to the documentation of both TaskList and
Get-Process in the supplementary reading in case you want to dive deeper into
either of these tools.