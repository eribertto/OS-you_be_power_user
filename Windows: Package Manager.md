Now that we know a bit about installing software and dependencies from
individual executables or package files, let's take a look at a different way to
manage software installations using tools called package managers. You've
actually already seen a package manager in action. Remember the apt or advanced
package tool we talked about in earlier video? Well, the advanced package tool
is actually a package manager for the Ubuntu operating system. We'll talk about
apt in a little bit. But you might be curious about what options you have for
Windows package management. A package manager makes sure that the process of
software installation, removal, update, and dependency management is as easy and
automatic as possible. Think about the normal way you might install a new
program on your Windows computer. You might search for it in a search engine, go
to the program's website, download the installer, then run it. If you wanted to
update the software, you might open up the program and use whatever mechanism it
provides for you to install the new version. Lots of programs give you a way to
perform automatic updates and Microsoft takes care of the ones it writes through
Windows update. But you might even need to go back to the website you downloaded
the software from originally to grab another installer for the new version.
Finally, if you wanted to remove the software, you might use the windows
Add/Remove programs utility. Or maybe run a custom uninstaller if it provides
you with one. Some installation technologies like the Windows installer can take
care of dependency management. But they don't do much to help you install
software from a central catalog of programs or perform automatic updates. This
is where a package manager like Chocolatey can come in handy. Chocolatey is a
third party package manager for Windows. This means it's not written by
Microsoft. It lets you install Windows applications from the command line.
Chocolatey is built on some existing Windows technologies like PowerShell, and
lets you install any package or software that exists in the public Chocolatey
repository. I've included links to both in the next reading. You can add any
software that might be missing to the public repository. You can even create
your own private repository if you need to package something like an internal
company application. Configuration management tools like SCCM and Puppet, even
integrate with Choclatey. That helps make managing deployments of software to
the Windows computers in your company, automatic and simple. We've talked about
a few ways we can install packages in earlier videos. Let's add Chocolatey to
the mix, which supports several methods of software installation itself. First,
you can install the Choclatey command line tool and run it directly from your
PowerShell CLI. Or you can use the package management feature that was recently
released for PowerShell. Just specify that the source of the package should be
the Choclatey repository. Remember this from our talk about installing software?
We use this command to locate the Windows Sysinternals package after adding
Choclatey as a software source. Just a refresher, the command was Find-package
sysinternals include dependencies. That's all well and good. But how do we
actually go about installing this package? Well, that's where the
Install-Package command-let comes into play. We can use this tool to install a
piece of software and its dependencies. Let's get installing that sysinternals
package we found earlier shot. I'm just going to go install, package-name
sysinternals. Yep, I'm just going to confirm. And just like that, we've got our
package. We can verify it's in place with the Get-Package command-let.
Get-Package -name sysinternals. You can also uninstall a package using the
Uninstall-Package -Name sysinternals.