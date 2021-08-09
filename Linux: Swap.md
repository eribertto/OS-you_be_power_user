In Linux, the dedicated area of the hard drive used for virtual memory is known
as swap space. We can create swap space by using the new disk partitioning tools
that we learned. A good guideline to use to determine how much swap space you
need is to follow the recommended partitioning scheme in the next supplementary
reading. In our case, since we just have a USB drive which doesn't need swap,
we're just going to partition the rest of it as swap to show you how this works.
In practice, you would create swap partitions for your main storage devices like
hard drives and SSDs. Okay. Let's make swap space. First, go back into the
parted tool and select /dev/sdb, where our USB is. We're going to partition it
again this time to make a swap partition. And then we'll format the Linux dash
swap file system on it. So, mkpart primary Linux swap 5 gibibytes 100 percent.
You'll notice that the end point of the drive says 100 percent which indicates
that we should use the rest of the free space on our drive. We're not done yet.
Swap isn't actually a file system, so this command won't be enough. I know I'm
sorry, I just lied to you like five seconds ago. If you think about it, it makes
a lot of sense since pages go into swap and not file data. Anyways, to complete
this process, we need to specify that we want to make it swap space with the
mkswap command. Let's quit out of parted and run this command on a new swap
partition. So, sudo mkswap dev, and our new swap partition is on dev sdb2.
Finally, there's one more command to run to enable swap on the device, swapon.
So, sudo swapon dev sdb2. If we want to automatically mount swap space every
time the computer boots up, just add a swap entry to the /etc fstab file like we
did earlier.