The ability to make remote connections is equally useful on Windows computers.
PuTTY is a free open-source software that you can use to make remote connections
through several network protocols including SSH. You can visit the PuTTY website
to download the entire software package with a Microsoft installer. Those are
the MSI files we talked about earlier. Or you can choose a specific executable
which provides the functionality you're after, like putty.exe. The PuTTY
downloads page is linked in the next supplemental reading in case you want to
check it out. Once you've downloaded and installed PuTTY, you can use it by
launching the GUI. A window will appear showing you the basic options for your
connection. Make a note of the host name, port, and connection type options. By
default, the port is set to 22 which is the default port the SSH protocol uses
and the connection type is set to SSH. All you need to do is type in the host
name or IP address of the computer you want to connect to, then click open start
up a new SSH session. Now I've SSHed into a remote computer. Running PuTTY from
the GUI isn't your only option. You can also use it on the command line. Open a
PowerShell prompt and type out the application name like this, then tell it you
want to connect via SSH by adding the dash SSH option. You could also provide
the user an address in the form of user@IP address and specifying the port at
the end. Altogether, the command would look something like this. PuTTY also
comes with a tool called Plink or PuTTY link which is built into the command
line after PuTTY is installed. You can use Plink to make remote SSH connections
too. SSH can be super useful especially if you want to connect from a computer
running Windows to a Linux-based operating system running remotely. Microsoft
actually provides another way to connect to other Windows computers called the
Remote Desktop Protocol or RDP. There are also RDP clients for Linux and OS 10
too, like RealVNC and Microsoft RDP on Mac. We'll add some links to these
clients in the supplemental reading. RDP provides users with a graphical user
interface to remote computers, provided the remote computer has enabled incoming
RDP connections. A client program called the Microsoft Terminal Services Client
or mstsc.exe is used to create RDP connections to remote computers. You can
enable remote connections on your computer by opening up the start menu, right
clicking on "This PC", then selecting "Properties". From there, select "Remote
Settings", and then pick an option from the remote desktop portion of the panel.
There are some security implications that come with allowing people to remotely
connect to your computer. You should only let users who you trust do this.
Typically, in an industry setting, these kinds of settings are usually set by
the system administrator for the company's computers that connect to the
network. Once you've allowed connections on the remote computer and provided
you're on the list of users allowed to access it, you can use the Remote Desktop
Protocol client mstsc.exe to connect to it from anywhere else on the network.
You can launch the RDP client in a few ways. You can type "mstsc" at the run box
or look up Remote Desktop connections in the Start Menu. Once you've launched
the client, it'll ask for the name or IP address of the computer you want to
connect to. The Windows RDP client can also be launched from the command line,
where you can specify more parameters like slash admin if you want to connect to
the remote machine with administrative credentials. We've linked to the RDP
documentation in the supplementary reading in case you want to learn more.