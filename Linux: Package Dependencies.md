Let's see what a package dependency would look like and Linux. We learned how to
install a standalone package in Linux using dpkg in the last lesson. Let's
install one more package. I downloaded the Google Chrome browser here in my
desktop and I want to install it with sudo dpkg -i google - chrome. Wait a
minute, what's this error I'm getting? Dependency problems prevent configuration
of google chrome stable. This is saying it can't install Google Chrome because
it's dependent on another package that isn't currently installed on this
machine. So before we can install Chrome, we have to install this package lib
app indicator one. While a standalone package installer like dpkg may be quick
to use, it doesn't install package dependencies for us. In Linux, these
dependencies can be other packages or they could be something like shared
libraries. Linux shared libraries similar to Windows dlls are libraries of code
that other programs can use. So what do you do if you're stuck with a dependency
error? You could install the dependencies one by one. Sure. But in some cases,
you might see more than just one dependency. You might even see 10. This is
especially true in Linux. It's not that fun to continually install programs just
so you can get one program to work. Luckily for us, that's where package
managers come in. Package managers come with the works to make package
installation and removal easier, including installing package dependencies.
We'll talk about package managers in the next lesson but for now, it's enough to
know that if you install a standalone package, you won't automatically install
its dependencies.