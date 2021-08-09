The way that processes are created and stopped differs based on the operating
system you use. First, let's have a look at how Windows does things. When
Windows boots up or starts, the first non-kernel user mode that starts is the
Session Manager Subsystem or smss.exe. The smss.exe process is in charge of
setting some stuff up for the OS to work. It then kicks off the log-in process
called winlogon.exe appropriately enough, along with the Client/Server Runtime
Subsystem called csrss.exe, which handles running the Windows GUI and command
line council. We'll talk about a process called init in the next lesson, which
Linux uses as the first process. You might be tempted to think of smss.exe as a
Windows equivalent of init. Don't fall into that trap though. When it comes to
process creation mechanisms, they're all pretty different. In Windows, each new
process that's created needs a parent to tell the operating system that a new
process needs to be made. The child process inherit some things from its parent
like variables and settings, which we can collectively refer to as an
environment. This gives the child process a pretty good start in life, but after
the initial creation step, the child is pretty much on its own. Unlike in Linux,
Windows processes can operate independently of their parents. Let's take a look
at how this works by creating our own. First, let's launch the PowerShell
process to give us a Windows command prompt. From there, we can type in
notepad.exe to create a new process for the notepad program. So far, so good.
The parent process is PowerShell, and the child is the notepad application. What
happens if we kill the parent process though by clicking on the X button? Notice
that notepad keeps on running happily even though its parent has been
terminated. Those children are just in their own world. Clicking the X is just
one way to stop a process from running in Windows, but as you might expect,
there are other ways you can stop processes. You can use a command prompt
command by calling on the task kill utility. Task kill can find and halt a
process in a few ways. One of the more common ways is use an identification
number, known as the process id or PID to tell task kill which process you'd
like stopped. One way to do this is to kill notepad again by specifying the PID
using taskkill/pid and then the PID number. Taskkill/pid, this is the process id
of notepad. That's success. This will send the termination signal to the process
identified by the PID, which happens to be notepad in our case. This is useful,
but how do we get that PID in the first place? Glad you asked. We'll talk about
how to locate and view processes and other more detailed process information in
an upcoming lesson.