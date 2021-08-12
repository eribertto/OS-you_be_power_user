Logs in Linux are stored in the /var/log directory. Remember that /var directory
stands for variable, meaning, files that constantly change are kept in this
directory, and it turns out that logs are constantly changing. If we look at the
/var/log directory with an LS, it might seem a little intimidating. Don't worry.
Each of these log files store specific information that we can figure out by
their file names. Let's check out some of the common ones you'll look at,
/var/log/auth.log, authorization and security-related events are logged here.
/var/log/kern.log, kernel messages are logged here. /var/log/dmesg, system
startup messages are logged here. If you encounter an issue at, let's say, boot
up, this is a good place to check for information. It might get a little
tiresome to open up each of these log files to find information about events.
Luckily, there are also log files that combine the information of other log
files. The downside is that these files are usually very large. If you have a
pretty good idea of where a problem might lie, you might want to opt for the
smaller and more specific log file. The one log file that logs pretty much
everything on your system is a /var/log/syslog file. The only thing that sys log
doesn't log by default are off events. When troubleshooting issues with user
machines, /var/log/syslog will usually contain the most comprehensive
information about your system, so that should be your first stop. Log files
output a lot of events. By that logic, they take up a lot of data that has to be
stored on our machine somewhere. We generally just want to see the latest events
on our system, so we don't need to overload or disk with all this information.
Luckily, our systems also do a good job of cleaning out log files to make room
for new ones. They use something called log rotation to do this. In Linux, the
utility rotate logs is called log rotate. You might want to investigate an event
that happened a month ago, so you can change your log rotation settings to make
sure not to delete events that are that old. We won't discuss how to work with
log rotation, but you can read more about it in the supplemental reading. We've
talked about logging in the context of a single machine, but if you find
yourself managing many systems and want to be able to parse their logs in one
central location, you can use something called centralized logging. We won't
talk about how to do this, but if you're interested in setting up a centralized
server, check out the next supplemental reading. Okay, enough talk about what
logs are. Let's actually look at some real ones. Whoa, this looks super
intimidating. But don't worry, we're not going to be reading all of this. In the
next lesson, we'll teach you how to troubleshoot using logs. But for now, let's
just read one line in sys log and parse what it says. The first field here is
the time stamp when the event occurred. Pretty straightforward. But depending on
the log, you might see a time format you aren't familiar with like a long string
of numbers such as 1501538594. Time stamps found in a format like this are
referred to as Unix or epoch time. At first, you might be baffled by this. Why
would you represent time in this way? And just what exactly is the Unix epoch?
The Unix epoch time is used to represent, then, it's the number of seconds since
midnight on January first, 1970, a sort of zero hour for Unix based computers to
anchor their concept of time. This means that 1501538594 represents the date,
time, Monday, July 31st. 30314 Pacific Standard Time. Why midnight on January
first, 1970? Is that date the birthday of Unix? Or does it mark some other
significant event? The actual answer is much simpler. The original engineers of
Unix at Bell Labs just picked it because it was convenient. So, don't be caught
off guard if you see a time stamp like this. The next field is the host name of
the machine the event occurred on. Next up is the service that the log event is
referring to. And last is the event that occurred. In the next lesson, we'll
show you some common troubleshooting tactics when using logs.