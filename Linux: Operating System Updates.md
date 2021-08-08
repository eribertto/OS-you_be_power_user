In Linux, you've already learned how to update and upgrade software on your
machines. When using the apt update and apt upgrade command, they may already
install security updates for you. But when you run apt upgrade, it doesn't
upgrade the core operating system. In windows, our OS package is Windows 10. In
Linux, It's the kernel along with other packages. The kernel controls the core
components of our operating system. Like our word processors, the kernel is just
another package. The kernel developers regularly include security patches, new
features, and fixes for bugs in their updates. If you want to get all these
things, you should be running a new kernel. To first view what kernel version
you have, we going to learn a new command called uname. The uname command gives
us the system information. If you use the dash r flag for kernel release, you'll
see what kernel version you have. You can see that I have kernel Version four
point one on here. To update the kernel and other packages, we use our nifty apt
command with the option full dash upgrade. Before running this command, remember
to update your application sources with APT update. Sudo apt update. Now, we can
run sudo apt full upgrade. If there's a new version of the kernel Available it
will install it for us. Once you reboot the computer, you can start using it.
You can verify the latest kernel is being used with the uname dash r command. We
left out a few details about kernel installations and security updates, but this
is a good start updating your system. If you're curious about learning the
intricate details of kernel and Linux updates, check out the supplemental
reading. With that, we've covered all the essentials to help you hit the ground
running with software installation and maintenance. Great work. You learned how
to install standalone packages, use package managers, and work with archives,
device drivers, and core operating system updates. These skills will be super
useful as an IT support specialist. Next, we're testing you again on both
bashing Windows. When you finished, I'll see in the next module.