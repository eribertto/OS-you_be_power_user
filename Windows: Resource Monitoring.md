You've been doing a great job and we're almost done with this module. Now that
we spent all this time learning about processes, like how to read them and how
to manage them, when are we ever going to use these newfound skills? Well,
pretty much all the time. But an IT support role, managing processes comes in
handy the most when processes become a little unruly. Our systems usually have
some pretty good ways of monitoring processes and telling us which processes
might be having issues. In Windows, what are the most common ways to quickly
take a peek at how the system resources are doing is by using the Resource
Monitoring tool. You can find it in a couple of places, but we will launch it
right from the start menu. Once it opens, you'll see five tabs of information.
One is an overview of all the resources on the system. Each other tab is
dedicated to displaying information about a particular resource on the system.
You'll also notice that Resource Monitor displays process information too along
with data about the resources that the process is consuming. You can get this
performance information in a slightly less detailed presentation from process
explorer. Just like the process you are interested in, right click and choose
properties. From there, pick the performance graph tab. You can see quick
visualizations of the current CPU memory indicated by private bytes and disk
activity indicated by I/O. But how can we get this information from the command
line? I am glad you asked. There are several ways to get this information from
the command line but we will focus on a PowerShell centric one, our friend
Get-Process. We know that if we run Get-Process without any options or flags, we
get process information for each running process on the system. If you check out
the column headings at the start of the output, you'll see things like NPM(K)
values in this column represent the amount of non paged memory the process is
using. And the K stands for the unit, kilobytes. You can see Microsoft's
documentation for a full write up of each column in the next supplemental
reading. This is useful but it is a lot of information. It can be really helpful
to filter down to just the data you are interested in. Let's say you wanted to
just display the top three processes using the MOS CPU, you could write this
command. Get-Process| Sort CPU -descending | Select -first 3 -property ID,
ProcessName and CPU. And just like that, we get the top three CPU hogs on the
system. This command might be a little hard to understand, so let's go through
it step by step. First, we call the Get-Process Commandlet to obtain all that
process information from the operating system. Then, we use a pipe to connect
the output of that command to the sort command. You might remember pipes from
some Linux examples earlier. We sort the output of Get-Process by the CPU column
descending to put the biggest numbers first. Then, we pipe that information to
the select command. Using select, we pick the first three rows from the output
of sort and pick only the property ID, name, and CPU amount to display. Now that
you've got some knowledge about both the command line and graphical tools
Windows provides for investigating resource usage, let's have a look at Linux
Resource Monitoring.