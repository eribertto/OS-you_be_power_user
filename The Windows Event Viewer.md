Similar to how we can jot down our life events in a journal, events are also
logged on our machines. In Windows, the events logged by the operating system
are stored in an application called the Event Viewer. Whether you're trying to
figure out why a computer game keeps crashing, or troubleshooting login or
access problems, or just satisfying your curiosity about what's going on in your
system, the Event Viewer is a great first stop. Let's take a look at some of the
information it collects, and how you can use the Event Viewer to get answers
you're looking for. You can launch the Event Viewer either from the start menu
or by typing in eventvwr.msc from the run box. The default view of the Event
Viewer shows is a summary of potentially important recent events. In our case,
this isn't super interesting, since we're more concerned with any issues that
occurred. Instead, let's take a look at the left-hand pane, where we can see a
few different event groupings. The first group we see is called Custom Views.
The Event Viewer records a lot of information about the system. So it can
sometimes be a little difficult to tease out the signal, like recent events,
from the noise or the stuff you don't care about. This is where the concept of
custom views comes in handy. With a custom view, you can create a filter that
will look across all the event logs the Event Viewers know about and tease out
just the information you're interested in. Let's say we wanted to only see
events of error, severity or higher that we're logged in the last hour. To do
this, Google create custom view options in right-hand actions pane. This will
bring up a tab called Filter. From there, click the error and critical
checkboxes. We're going to change the logged drop down menu to last hour. In the
Event logs, we're going to select just are just the Windows Logs, then click OK.
Then we're going to give our view a new name. Click OK once more. Once you're
done, you'll see a new view come up under custom menus, where only the events
that matched your filter are displayed. The other two categories of logs you'll
see in the left-hand navigation page are Windows Logs and Application and
Services. The Windows Logs categories contain event logs that are generally
applied to the whole operating system. Let's say you're having an issue with a
driver failing during startup. The log called System would be a good place to
start. If you want to see whose been accessing the computer, then you begin
investigating the Security log. The other category is called Applications and
Services Logs. This category contains logs that track events from a single
application, or operating system component, instead of the system wide events of
the Windows logs category. For example, if you're having trouble with PowerShell
and wanted to get more information about it, checking out the PowerShell log
under Applications and Services log would be a great first step. Regardless of
its category, each line in a given log in the Event Viewer represents an event.
Each event contains information grouped in columns about the event like the
login level. Information is the lowest level and critical is the highest. You
could also find the Date and Time the event occurred. Selecting an event will
bring up more detailed information in the bottom pane of the Event Viewer. This
can help you dig into troubleshooting or even give you context for a bug report.
The Event Viewer is a super helpful tool for IT support specialists. It can
provide you with a lot of really detailed information about the problems any
software or hardware might be experiencing on your system. There's a lot of
information in there though. So don't forget about its custom views and
filtering capabilities. More importantly, don't hesitate to poke around the tool
and get used to finding things in its interface. You'll have fun and you'll
learn a lot. Next stop, the wild world of Linux logs.