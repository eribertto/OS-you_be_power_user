One type of package that
we haven't discussed yet isn't really a package at all,
it's an archive. An archive is comprised of one or more files that's compressed
into a single file. Package archives are basically the core or source software files that
are compressed into one file. When we install software
from a source archive, it's referred to as,
installing from source. Popular archive types you'll see are .tar,
.zip, and .rar. To install software found in an archive,
you first have to extract the contents of the
archive so you can see the files inside. Then, depending on what type
of code it was written in, you have to use a specific
method to install it. We won't discuss how to
install from source, since it changes depending on what
language the software was written in. But we'll discuss how to extract
the contents of an archive, which you'll have to do a lot
as an IT support specialist. It's not just software that's stored in
an archive, anything can be archived, like pictures or music files. You'll see these a lot in IT support. To make things more complicated, archive types have lots of different
way they can be extracted. Luckily, there's a very popular tools
in windows for file archiving and unarchiving different file types,
like .rar .zip and tar. This is the open source tool 7-zip. It's already installed on my computer. If you want to download it yourself, I've included a link in
the supplemental reading. There's an archive on my
desktop called colors.zip. Let's go ahead and extract this archive so
that we can see the files inside. I'm just going to right click,
7-Zip, extract, here. It looks like there are a bunch
of files inside of this archive. Besides unarchiving files,
you can also archive files. I'm going to make a new
folder called new colors. Then, I'm going to add this
new blue dot text file and the old colors in this folder. Then, I'm just going to archive
it with 7-Zip and Add to archive. Click OK. Pretty cool, right? Now, if you wanted to send someone
a bunch of files in an email, you don't have to send them one by one. Instead, you can combine them all in
one archive and send one single file. If you're using PowerShell version 5.0
of greater, you can actually extract and compress archives right
from the command line. Let's say you've got a bunch of files in a
folder called cool files on your desktop, that you'd like to add
to the new zip file. After you've opened up the PowerShell
command line interface, you can issue this command,
Compress-Archive.path. CoolFiles, and then we're just going to make a new archive in the desktop
called CoolArchive.zip. Now, if we check our desktop. There you should see it, CoolArchive.zip. This will take everything from
the desktop CoolFiles directory, and compress it into this CoolArchives.zip