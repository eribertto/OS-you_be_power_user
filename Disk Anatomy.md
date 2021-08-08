Before we start adding a filesystem to a
disk, let's do a rundown of the components of the disk that allow you to store and
retrieve files. A storage disk can be divided
into something called partitions. A partition is just a piece of
the disk that you can manage. When you create multiple partitions,
it gives you the illusion that you're physically dividing a disk
into separate disks. To add a filesystem to a disk,
first you need to create a partition. Usually, we just have a single
partition for our OS, but it's not uncommon to have multiple
partitions for different uses. Let's say you want to have two
partitions on a disk, one for a Windows OS and one for a Linux OS. Instead of using two machines
to use both operating systems, you can just use one machine and
switch between the two OSs on boot-up. You can also add different filesystems on
different partitions of the same disk. Partitions essentially act as
their own separate sub-disks, but they all use the same physical disk. One thing to call out is that, when you format a filesystem on
a partition, it becomes a volume. Volume and partition are sometimes
mistakenly used synonymously, but we want to make sure that you
understand this distinction. The other component of
a disk is a partition table. A partition table tells the OS
how the disk is partitioned. The table will tell you which
partitions you can boot from, how much space is allocated to partition,
etc. There are two main partition table
schemes that are used, MBR, or Master Boot Record, and GPT,
or GUID Partition Table. These schemes decide how to structure
the information on partitions. MBR is a traditional partition table,
and it's mostly used in the Windows OS. MBR only lets you have volume
sizes of 2 terabytes or less. It also uses something
called primary partitions. You can only have four
primary partitions on a disk. If you want to add more,
you have to take a primary partition and make it into something known
as an extended partition. Inside the extended partition, you can then make something
called a logical partition. It's a little odd to get at first, but that's just how the partition
table was created. MBR is an old standard, and
it's slowly being faded out by the next partition table
scheme we'll talk about, GPT. GPT is becoming the new standard for
disks. You can have a volume size
greater than 2 terabytes, and it only has one type of partition. You can make as many of
them as you want in a disk. In an earlier lesson, we learned
about a new BIOS standard called UEFI that's become the default BIOS for
newer systems. To use UEFI booting, your disk has
to use the GUID Partition Table. Now that you know what you need
to do to make a partition, let's partition an actual disk. In the next few lessons,
we're going to learn how to partition and format a USB drive for each respective OS.