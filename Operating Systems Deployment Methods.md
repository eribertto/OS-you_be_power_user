One tool we can use to image computer is a disk cloning tool. It makes a copy of
an entire disk and allows you to back up a current machine or set up a new one.
There are lots of discloning tools out there to help you complete this task. The
benefit of disk cloning over a standalone installation media is that you can
also install settings and folders that you might need. One of the many disk
cloning tools out there is the open source software Clonezilla. It can be used
to backup and restore a single machine or many machines simultaneously. A
popular commercial imaging tool is Symantec Ghost. To read more about other disk
cloning software, check out the supplemental reading right after this video.
With disk imaging lots of tools offer different ways you can clone a disk. One
option is disk-to-disk cloning where you connect an external hard drive to the
machine you want to clone. You can connect a hard drive like your HDDs and SSDs
into something known as an external hard drive dock. These devices are great IT
tools that kind of look like toasters. Once you connect your external hard
drive, you can use any disk cloning tool of your choice. We're going to show you
a really quick example of how disk cloning works. Let's use the Linux command
line tool dd to copy files. Dd is a lightweight tool that's also used to clone a
drive. Again, you can use any tools you want to clone your disks, but right now
we're just going to use dd. Let's make a copy of the USB drive I have connected
in my laptop then save it as an image file. First, we want to make sure we have
this drive unmounted. Then, we want to run dd. You don't have to know how dd
works to use this command. Actually, you should check out the final supplemental
reading to learn more about this tool. This just says, I'm going to copy the
contents of /dev/SDD which is the USB drive and save it to the desktop in an
image file. Once the image file is saved, if we open it up we should see the
exact same contents as the USB drive. You can use dd for larger disks like hard
drives and it'll function the same way. Pretty cool, right? Another method you
can use to image a machine is to request the images directly from the network.
Lots of operating system manufacturers today offer network initiated
deployments. This means no more smessy standalone installation media. Instead,
you can just download and install an operating system through the network. If
you want to use your own images and not the built in network boot options for
your computers, there are other options for that too. We don't discuss the
specifics of them here but they require a bit of automation to get going. It
doesn't matter if it's a laptop, desktop, Windows OS, Linux OS e.t.c. If you're
managing the operating system deployment for a company, you want to keep some
aspects of hardware standardization in mind. Imagine if your company has a
different laptop with different drivers that needed to be installed. This can
get tedious to maintain. It's usually a good idea to try and standardize what
type of hardware you use in a company to make your job of deploying operating
systems a little easier. Okay, you're so close to finishing this course. We've
got a final pair of assessments for you where you'll use logs to help you track
down some issues.