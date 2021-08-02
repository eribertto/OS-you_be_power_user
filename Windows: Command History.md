Picking right up from the last video,
let's say we want to make a couple of directories, my_cool_folder2 and
my_cool_folder3. We could just type mkdir my_cool_folder2,
and then type again mkdir my_cool_folder3, but instead we're going to use another cool
PowerShell feature called history. Each and every time you enter in
a command, it gets saved into memory and added to a special file. You can go through the previous commands
you used with the history command. I'm now showing a list of
commands that I entered earlier. This information alone isn't very useful. Instead, there's a better use of
the history that lets us quickly scroll through these commands and
use them again. We can scroll through these commands with
the up or down keys on our keyboard. I'm going to go up to my previous command, and I should see that I
have mkdir my_cool_folder. Instead of typing the whole
thing to make a new folder, I'm just going to append
the number 2 to my command. And boom, a new file is created without
having to type everything over again. Cool, right? You can even search through your
previously used commands using the history shortcut Ctrl+R. From here you can start typing bits and pieces of the command you want to
look for, and it'll show you matches. Let's search for the word folder. I should see the mkdir
commands I was using before. Pretty neat. If you're using an older
version of PowerShell, it may not have the Ctrl+R feature. If that's the case you can type the #
symbol followed by some part of your old command, and then use Tab completion to
cycle through the items in your history. The history feature,
along with Tab completion and get-help, will be your best friends
while you work in PowerShell. Keep them close to you and
get to know them super well. Hmm, our shell is looking
a little cluttered. It's kind of hard to see where I'm at, so
let's clean up our shell a little bit. We can do that with the clear command. This doesn't wipe your history,
it just clears the output on your screen. It looks a little better.
