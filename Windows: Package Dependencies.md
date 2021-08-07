Packages of software usually rely on
other pieces of code in order to work. Let's say you're installing
a game on your Windows computer. The program might need to do some
calculations to make the physics of the game work properly and render the results in the form
of graphics on the screen. To perform these tasks, the game might have a dependency on a
physics engine to do the calculations and a rendering library to show
the sweet graphics on the screen. In order for the game to work, you'll have to have all that
software available to the game. Counting on other pieces of software to
make an application work is called having dependencies since one bit of code
depends on another in order to work. In our example, the game depends
on both the physics engine and a rendering library to run. But wait, what do we mean
when we refer to a library? You can think of the library as a way
to package a bunch of useful code that someone else wrote. This code is bundled
together into a single unit. Programs that want to use the
functionality that the code provides can tap into it if they need to. In Windows, these shared libraries are called
dynamic-link libraries, or DLL for short. You can find out more details
about dynamic link libraries in the next reading. One super useful feature of a DLL
is that the same DLL can be used by lots of different programs. This means all that shared code doesn't
need to be loaded into memory for each application that wants to use it,
so less memory overall is used. Windows applications typically
have many dependencies all located together in
a single installation package. Along with something called an MSI file
that tells the Windows Installer how to put it all together. This means that a given installation
package will have all the resources and dependencies like DLLs,
right there in the package. The Windows Installer will also handle
managing those dependencies and make sure they are available
to the program. In the old days,
things weren't always so great. Imagine this scenario. A video player you've been using to
play movies on your computer uses a graphics DLL to display
films on your screen. A new game just came out that you
want to play, so you install that too. The game comes along with a new
version of that graphics library. So the game installer updates
the existing version with the new DLL. All of a sudden,
your video player stops working. It turns out the video player doesn't know
how to use the new version of the DLL, which is a pretty big bummer. On modern Windows Operating Systems
though, DLL hell is a problem of the past. To fix it, most shared libraries and
resources in Windows are managed by something called
side-by-side assemblies or SxS. Most of these shared libraries are stored
in a folder at C:\Windows\WinSxS. If an application needs to use
a shared library to perform a task, that library will be specified
in something called a Manifest. This tells Windows to load the appropriate
library from the SxS folder. The SxS system also supports access
to multiple versions of the same shared library automatically. So when you install software, you don't pull the rug out from underneath
the programs you've already got. In addition to manifest,
the SSX system and installers bundling dependencies
together in their installation packages. You can use a Windows Package Manager to
help install and maintain the libraries and other dependencies that your
installed software needs to use. We'll talk about this in more detail in
our lesson on Windows package managers. We'll give you preview using the Windows
package management feature for PowerShell. Using a Windows package management
cmdlet called Find-Package, you can locate software, along with its
dependencies right from the command line. By the way, a cmdlet is basically the name
we give to Windows PowerShell commands that use the verb-noun format. We've already used lots of cmdlets
such as get-help, select-string etc. There are hundreds of cmdlets built into
Windows and you can even write your own. Okay, back to my task at hand. Let's say you wanted to install
the Sysinternals package. Which is a set of tools released by
Microsoft that can help you troubleshoot all sorts of problems on
your Windows computers. You could download the Sysinternals
package from the Microsoft Website or you could use the package
management feature. First we'll need to open up a PowerShell
terminal by typing in PowerShell from the start menu. Then we can try to locate the sysinternals
package by executing this command. Find-Package
sysinternals-IncludeDependencies. An error. No match found. What's that all about? This exception was generated because the
default source of packages in PowerShell is the PowerShell gallery, which doesn't
contain the Sysinternals package. Luckily, all we need to do
is tell PowerShell about a place where it can find
the Sysinternals package. And that's a package
repository called Chocolatey. We'll dip into more about Chocolatey
in the package manager video. But for now, just know it's a place where all kinds
of windows software packages live. So, before we can install any packages,
we need to add a package source that tells our computer where it can find
the packages we want to install. Since we want to use Chocolatey
to find our packages, we need to add it as a package source. We're going to do that with the PowerShell
command Register-PackageSource. Let's go and type Register-PackageSource-Name chocolatey-ProviderName
Chocolatey-Location, .org/api/v2. We can verify both sources of
software are now good to go with the Get-PackageSource command. And then, try to locate our package and its dependencies again with Find-Package, sysinternals-includeDependencies. Sweet! Now that we know that’s
the package we want, we can use a cmdlt called Install-Package
to actually install Sysinternals and its corresponding dependencies. We’ll do that in a later lesson. Now it's time for snack break. All this Chocolatey talk made me hungry.