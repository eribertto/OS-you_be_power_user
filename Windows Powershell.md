So far in this course we have been
using command aliases in PowerShell. PowerShell is a complex and powerful command language,
that's also super robust. We've been able to use common aliases, that are exactly the same as
their Linux counterparts. But from here on out, we'll need to deploy
some advanced command line features, so we'll need to look at
real PowerShell commands. You've already seen an example of
a real PowerShell command, Get-Help, which is used to see more
information about commands. There's another PowerShell command that
we can use to look at one of our aliases, that we've been using
as our list directory. To see what the actually PowerShell
command is that gets executed, we can use the PowerShell command,
Get-Alias. Interesting when we call LS, we are calling the PowerShell
command Get-ChildItem, it gets or lists the children which are the files and
sub directories of the given item. Let us actually run this Get-ChildItem
command with the item C:\. You'll see this is the same output as,
ls C:\. Cool. PowerShell commands are very long and descriptive, which makes
them easier to understand. But it does mean a lot of extra typing, when you're working
interactively at the CLI. Aliases for common commands are a great
way to work more quickly in PowerShell. We've been using them up to this point
to help us hit the ground running with the command line. In Windows, you pretty much have three
different ways you can execute commands. You can use real PowerShell commands,
or the relatable alias names. Another method that we've mentioned, but haven't really talked about yet
is cmd.exe commands. Cmd.exe commands are commands from
the old MS-DOS days of Windows. But they can still be run do
to backwards compatibility. Keep that in mind, that they aren't
as powerful as PowerShell commands. An example of a cmd.exe command is dir. Which coincidentally points to
the PowerShell command Get-ChildItem, which is also where,
ls Alias gets pointed to. Remember the PowerShell command Get-Help,
well there's a command parameter that you can use to get
help with command.ext commands, /?. Keep the difference in mind,
Get-Help is used for PowerShell commands like Get-Help ls, and
/?, is used for other commands like dir/?. If I tried to use, ls/?,
it will return nothing, because the PowerShell command
that ls is an alias of, doesn't know how to handle to
the parameter /?, and vice versa. You're free to use whatever
commands you feel comfortable with. But in this course we're going to use
common aliases, and PowerShell commands.
