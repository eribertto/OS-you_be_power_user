Okay. Now, to talk about the package manager used in Ubuntu called the APT or
Advanced Package Tool. We've actually already used APT in an earlier course, so
hopefully, this won't look new. The APT package manager is used to extend the
functionality of the package. It makes package installation a lot easier. It
installs package dependencies for us, makes it easier for us to find packages
that we can install, cleans up packages we don't need, and more. Let's see how
we will install the open source graphical editor, Gimp, using APT. And if you
want to follow along on your own machine, I've included a link to the Gimp
download in the next reading. So, sudo apt install gimp. Let's take a look at
what this command is doing. APT grabs the dependencies that this package
requires automatically and asks us if we want to install it. You can see this
line here, 0 upgraded, 18 newly installed, 0 to remove, and 16 not upgraded.
This gives us a good overview of what we're doing to the packages on our
machine. Now, let' s remove this package. It's sudo APT remove gimp. You can see
that it removes dependencies for us that we're not using anymore because we
don't need Gimp. You also noticed that when installing this package, we didn't
have to download the gimp package. It was just on our system. How is that
possible? Well, thanks to something known as a package repository, we don't have
to manually search for each and every software we want online. We've already
seen the chocolatey package repository in action. Repositories are servers that
act like a central storage location for packages. Lots of software developers
and organizations host their software on the internet, and give out a link to
where that location is. You can add that link to your own machine, so it
references that package or list of packages. You've already seen this with The
Register-PackageSource commandlet where we added this location of the chocolatey
repository. So on Linux, where do you add a package or repository link? The
repository source file in Ubuntu the /etc/APT/sources.list. Your computer
doesn't know where to check for software if you don't explicitly add the package
or repository links to this file. Let's just open this up real quick and take a
peek. There's some extra information in here that isn't important. But you can
see here that there are links here. If you navigate to those links, you'll see a
directory that holds lots of packages. Ubuntu already includes several
repository sources in here to help you install the base operating system
packages, and other tools too. If you work in a Linux environment, there are
also special repositories called PPAs or personal package archives. PPAs are
hosted on Launchpad servers. Launchpad is a website owned by the organization,
Canonical Limited. It allows open source software developers to develop,
maintain, and distribute software. You can add PPAs like you would a regular
repository link, but be a little careful when using a PPA instead of the
original developer's repositories. PPA software isn't as vetted as repositories
you might find from reputable sources like Ubuntu. They can sometimes contain
defective, or even malicious software. One more thing to call out about
repositories is that the repository managers update their software pretty
regularly. If you want to get the latest package updates, you should update your
package repositories with the APT update, and then, APT upgrade commands. The
APT update command updates the list of packages in your repositories, so you get
the latest software available. But it won't install or upgrade packages for you.
Instead, once you have an updated list of packages, you can use APT upgrade, and
it will install any outdated packages for you automatically. Before installing
new software, it's good to run APT update to make sure you're getting the most
up-to-date software in your repositories. You'll also want to run APT upgrade to
install any available updated packages on your machine. You can use the
apt--help command to learn more about the commands available with APT. We won't
cover them all, but you can list packages, search packages, get more information
about packages, and more. There are lots of different package managers you can
use with Ubuntu. We chose APT because it's a popular package manager, but you
can read up on an alternative package manager in Ubuntu, in the next
supplemental reading. Awesome. Now that you've entered the APT command to your
toolkit, your ready to maintain packages in Linux. This is a skill you'll be
using a whole lot in the IT support world. We'll talk about that more in the
next lesson.