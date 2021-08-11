In earlier lessons, we talked about processes. We saw some examples of how to
manipulate them with signals. Let's expand on that idea, Process Management, by
looking at some of the things you can do to manipulate processes. In Windows,
we've looked up programs like Task Manager, the PowerShell command like Get-Desk
process, and the Task close utility, to name a few. We've also seen how to send
a running processor signal through Control C, but there's another Process
Management tool we haven't talked about which lets you do things like restart or
even pause processes. This tool is called Process Explorer. Process Explorer is
a utility Microsoft created let IT support specialists, systems administrators,
and other users look at running processes. Although it doesn't come built into
the Windows operating system, you can download it from the Microsoft website
which I've linked to in the supplemental reading right after this video. Once
you've downloaded Process Explorer and started it up, you'll be presented with a
view of the currently active processes in the top window pane. You'll also see a
list of the files a selective process is using in the bottom window pane. This
can be super handy if you need to figure out which processes use a certain file,
or if you want to get insight into exactly what the process is doing, and how it
works. You can search for a process easily in Process Explorer by either
pressing Control F, or clicking on the little binocular button. Let's go ahead
and do a search for the notepad process we opened up earlier. You should see
C\Windows\System32\notepad.exe listed as one of the search results. If you see
something that says notepad.exe.mui, don't worry. MUI stands for multilingual
user interface, and it contains a package of features to support different
languages. Anyways, once you've located the notepad.exe process, notice how it's
nested under the command.exe process in the UI. This indicates that it's a child
process of command.exe. If you right-click on the notepad.exe process, you'll be
given a list of different options that you can use to manage the process. Check
out the ones that say Kill Process, Kill Process Tree, Restart, and Suspend.
Kill Process is what you might expect. Say goodbye to notepad. Kill Process Tree
does a little bit more. It'll kill the process and all of its descendants. So,
any child process started from it will be stopped. Kill Process Tree takes no
prisoners. Restart is another interesting option. You might be able to guess
what it does just by its name. It will stop and start the process again. Let's
do that with the notepad.exe process. We started from command.exe. Interesting.
After the restart, notepad.exe doesn't appear as a child of command.exe anymore.
What gives? Well, if you'll search for notepad.exe again, we can see it's been
restarted as a child of the procexp.exe process. This is the process name for
Process Explorer. This makes sense since Process Explorer was a process in
charge of starting it again after we terminated it. But what about the Suspend
option? Instead of killing a process, you can use this option to suspend it and
potentially continue it at a later time. If we right-click, suspend the process,
we'll see that in the CPU column, the process explorer output, the word
suspended appears. While a process is suspended, it doesn't consume the
resources it did when it was active. We can kick it off again by right-clicking
and selecting the Resume option. Process Explorer can do a lot, and we'll take a
look at some of the monitoring information it can give us in an upcoming lesson.
We won't get into the details of all its features though. So, if you're curious,
you can check out the documentation on Microsoft's website. We put a link to it
for you and the supplementary reading.