In Linux, software installations are a little bit more clear. We mentioned in an
earlier lesson that you can install software directly from source code. This
method changes depending on the software because different programming languages
are compiled differently. We won't go in-depth about software development, but
let's say we had an archive with a simple package we want to install. This is my
Flappy app package. I've already extracted it, so you can see there's a setup
script. This is a script file that will run a bunch of tasks on the computer in
order to set up the package. And then flappy_app_code, this is the actual
software code. The README is a pretty standard file contained in source archives
that has information about the archive. It not so subtlety asks you to read it
before you do anything. The set of script is what we're concerned with since it
tells us how to install our package. A sample setup script can contain program
instructions like compile flappy_app_code into machine instructions, copy
compiled flappy app binary to slash bin directory, or create a folder to slash
home slash, whatever the username for flappy app is. This is a very simple
overview of what happens when you install a simple package. In the end, the
software developers decide what their software needs to work and runs tasks to
get it working. It's up to the developer whether those tasks are creating files
or updating directories. If you knew the programming languages used, you could
read these instructions yourself. But that's a bit out of scope for this course.
Anyways, that's how software installation works on Linux in a nutshell.