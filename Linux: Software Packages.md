In Linux, there are lots of different distributions and each might have
different package types. For example, in the Linux distribution or Distro, Red
Hat, the packages that are used are.rpm or Red Hat Package Manager packages. We
won't cover how to work with RPM packages, but just be aware that packet types
can change when you're working with different Linux distributions. If you're
interested in learning more about RPM packages, I've included a link in the
supplementary reading right after this video. In this course, we'll be working
with Debian packages which Ubuntu uses. A Debian package is packaged as a.deb
file for Debian. You've already learned how to install a Linux package using the
help of a package manager in the first course on technical support fundamentals.
We'll dive deeper into this in a later video, but let's focus now on how to
install a single standalone Debian package. You'll have to work with standalone
Debian packages, especially when developers package and release their software
on different websites. To install a Debian package, you'll need to use the D
package or Debian package command. There is a standalone package here for the
open source text editor, atom. Let's go ahead and install it using D package. We
have to use the iFlag for the install, and that's it. Now it's installed on this
computer. How about if we wanted to remove a package? To do that, we use the R
or remove flag. And that's how you install and remove a standalone Debian
package. Pretty simple, right? You can also list the Debian packages that are
installed on your machine with a D package dash L. The L is for list. There are
lots of programs on here. It looks kind of messy. Can you think of another
command that we've used before that would help us search if a certain package is
installed? That's right. The grep command. Let's say we want to search for the
atom package we just installed. Keep in mind I just uninstalled it, so am just
going to install it really quickly. Now let's run D package dash L grep atom.
Here, we have the D package dash L command that's been piped to grep. Remember,
the pipe command takes the standard output of one command which in this case is
the output of the D package dash L. Then, it sends it to the standard input of
the command it pipes to. In this case, grep. If we run this command, it shows us
that atom is definitely in the list of packages here. Just remember that when
using grep, it lists other results that have the search terms in the name. Just
like that, we've learned how to install any Debian package in Linux. We're
really cooking now. Great work.