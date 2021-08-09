Now that we've taken a good, hard look at files in different file systems, let's
turn our attention to how we can monitor the number and size of those files in
Windows. You seen how there are loads of third party programs out there to
partition and format discs on Windows. Well, there are also lots of applications
you can download that can check and visualize disk usage on a Windows machine.
But you can use the disk management council we examined in an earlier lesson to
get a sense of your disk capacity usage. To check disk usage, you can open up
the computer management utility. Then head to the disk management console. From
there, right click on the partition you're interested in and select properties.
This will bring up the general tab where you can see the used and free space on
the drive. In addition to using this graphical user interface to check the disk
usage, Windows provides a command line utility called disk usage as part of it
system internal tool offering. That DU utility can print out the usage of a
given disk and tell you how many files it has. It can be useful for creating
scripts which might need text based output instead of visual reports like the
pie chart in disk management. You can find a link to the DU tool in the next
supplemental reading. On the same tab in the disk management console, you might
notice a button that says disk cleanup. If you press this button, Windows will
launch a program called CleanManager.exe which will do a little housekeeping on
your hard drive to try and free up some space. This housekeeping includes things
like deleting temporary files, compressing old and rarely used files, cleaning
up logs and emptying the recycle bin. Another task related to disk health is
called defragmentation. The idea behind disc defragmentation is to take all the
files stored on a given disk and reorganize them into neighboring locations.
Having files ordered like this will make life easier for rotating hard drive
disks that use an actuator arm to write to and read from a spinning disk. The
head of the actuator arm will actually travel less to read the data it needs. I
should call out that this is less of a benefit for solid state drives since
there's no physical read write head that needs to move around a spinning disk.
For these kinds of drives, the operating system can use a process called Trim to
reclaim unused portions of the solid state disk. We won't go into details of how
trim works but it's good to know that exists. I've included a link to more
information on trim in the reading right after this video. Defragmentation in
windows is handled as a scheduled task. Every so often the operating system will
defragment the drive automatically and you don't need to worry about it but you
can manually defragment a drive in Windows if you want to. To kick off a manual
defragmentation, open up the disk defragmenter tool bundled with the OS. Type
disk defragmenter. When it launches, you'll be given a list of disks which can
be defragmented along with buttons to analyze the potential gains from running a
defrag or defragmentation and to run the defrag itself.