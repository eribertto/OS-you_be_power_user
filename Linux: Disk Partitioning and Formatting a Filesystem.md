In Linux, there are a few different partitioning command line tools we can use.
One that supports both MBR and GPT partitioning is the parted tool. Parted can
be used in two modes. The first is interactive, meaning we're launched into a
separate program, like when we use the less command. The second is command line,
meaning you just run commands while still in your shell. We're going to be using
the interactive mode for most of this lesson. Before we do that let's run a
command to show what disks are connected to the computer using the command line
mode. We can do this by running the parted - l command. So sudo parted - l. This
lists out the disks that are connected to our computer. We can see that the disk
/dev/sda is 128 gigabytes. I've also plugged in a USB drive and you can see
that, /dev /sdb is around 8 gigabytes. Let's quickly go through what this output
says. Here we can see the partition table is listed as gpt. The number field
corresponds to the number of partitions on the disk. We can see that there are
three partitions. Since this disk is /dev/sda, the first partition will
correspond to /dev/sda 1 and the second will correspond to /dev/sda 2 et cetera.
The start field is where the partition starts on the disk. For this first
partition we can see that it starts at 1,049 kilobytes and ends at 538
megabytes. The field after that shows us how large the partition size is. The
next field tells us what file system is on the partition. Then, we have the name
and finally, we can see some flags that are associated with this partition. You
can see here that /dev /sdb doesn't currently have any partitions, we'll fix
that in a minute. Let's select our /dev/sdb disk and start partitioning it. We
want to be super careful that we select the correct disk when partitioning
something so we don't accidentally partition the wrong disk. We're going to use
the interactive mode of parted by running sudo parted /dev/sdb. Now we're in the
parted tool. From here, we can run more commands. If we want to get out of this
tool and go back to the shell then we just use the quit command. I'm going to
run print just to see this disk one more time. It says we have an unrecognized
disk label. We'll need to set a disk label with the mklabel command. Since we
want to use the gpt partition table let's use this command. Mklabel gpt. Let's
look at the status of our disk again to do that we can use a print command. Here
we can see the disk information for the selected /dev/sdb disk. Now it says we
have the partition table gpt. All right. Let's start making modifications to the
disk. We want to partition the /dev/sdb disk into two partitions. Inside the
parted tool we're going to use the mkpart command. The mkpart command needs to
have the following information, what type partition we want to make, what file
system we want to format, and the start of the disk and the end of the disk like
this. The partition type is only meaningful for mbr partition tables. Remember,
the mbr uses primary, extended, and logical partitions. Since we are formatting
this using gpt, we're just going to use primary as the partition type. The start
point here is one mebibyte and the endpoint is five gibibytes. So our partition
is essentially five gibibytes. Remember from the earlier course, that data sizes
have long been referred to in two different ways, using the exact data
measurement and the estimated data measurement. Remember that one kibibyte is
actually 1,024 bytes while one kilobyte is 1,000 bytes. We haven't really had to
care about this distinction before. Some operating systems sometimes measure one
kilobyte as 1,024 bytes which is confusing, but when dealing with data storage
we want to make sure we're using the precise measurements so we don't waste
precious storage space. Let's opt to use mebibyte and gibibyte in our partition.
Next, we're going to format the partition with the file system using mkfs. So
I'm just going to quick, sudo mkfs type is ext4. And I want to format the
partition, so sdb1. We also left the rest of the disk unpartitioned because
we're going to use it for something else later. With that, we've created a
partition and formatted a file system on a USB drive. Remember to always be
careful when using the parted tool. It's very powerful and if you modify the
wrong disk on here it could cause a pretty big mess. Even though we've
partitioned our disk and formatted a file system on here, we're not actually
able to start reading and writing files to it just yet. There's one last step to
get a usable disk in Linux. We have to mount the file system to a directory so
that we can access it from the shell. Spoiler alert, you'll learn how to do that
in the next video.