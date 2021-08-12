Hi, I'm Rob. I'm Candace. Congrats on making it through this course. Now that
you've made it this far, we're here to give you a sneak peek into what an
interview on the technical subjects covered by this course might look like. We
hope this will help you have a better idea of what to expect in your next
interview. Just remember to keep learning and keep practicing. All right. So for
this scenario, let's say that you stopped by to see a user at their desk and
they reported some kind of application issue. When you get there, they show you
the problem. They're trying to launch an application from a shortcut on their
desktop and every time they double-click on it, they get this generic error
message that says, "There was an error launching the application." Start
troubleshooting that for me. What OS are you using and what's the name of the
application? Say it's Linux desktop and it's a custom application. We'll say
that I built it in-house. Let's call it Application X. Okay. Do you remember the
last time this worked? Sure. We can say it worked on Friday and today is Monday.
Okay. Do you know if there's any other users that's having this issue? So this
is the first report of it but it's still early on a Monday. Okay. Are you aware
if there is any type of updates that happened over the weekend? Not that I'm
aware but is there any way we can check? So we can check the Apt log. What is
Apt? Apt is pretty much a utility that we use in installing applications and
updates. Great. Cool. So where were we? Can you walk me through where we can
find the logs for Apt? I'm actually not sure where the logs for the application
would be at. Great, and how might you find it out if this was a real-world
scenario? We can probably check the main page or search online. Okay. Great,
that's a good idea. So, let's say that you're able to find out that the log is
in slash var, slash log, slash apt, and the file that we're looking for is
history.log. Now that you've got that file, we've got a hundred different
entries in here. How do we find what we're looking for specifically just for
this application? We can use the grep command with the application name. Okay.
Let's say we do that and we find that there was an update done just over this
past weekend. So it's actually possible that the update could have caused this
issue. There could be a missing dependency or the application could have gotten
corrupted. So we can also check permissions, too. So where do we start? So I
want you to run a few updates just to make sure everything's installed and
there's no missing dependencies. So first, I want you to run sudo apt get update
and then sudo apt get upgrade. Okay. Great. So let's say that those both run,
they complete successfully, what do we do now? So let's try and launch the
application. So it still fails, same exact error. So I think now, we should
probably check the permissions. All right. How do we do that? So first, you want
to get the location. So we can probably get the location by right clicking on
the shortcut and then seeing what the command section says. Okay. So we do that
and let's say it says application dash x as the command. So now, you want to use
the which command with the location that provide it. Okay. We'll say it's
located in slash usr, slash bin. So now, you want to navigate with cd to the
directory of that application. Okay. Say we're there. Okay. So now, you want to
list out all the permissions. So you want to do ls space hyphen L? Okay, so
here's what I see. Dash RWX, R dash X, dash dash dash, then it says root, space,
root. Can you explain to me what this all means? R stands for read, W stands
here write, X stands for execute. The first [inaudible] three is associated with
the owners of the application, the second set of three is associated with the
groups of the application, and then the last set of three is associated for
other or users. Root is associated with the owner and then the second root is
associated with the group. Okay. So after looking at all that, does anything
stand out as wrong here? Yes. So since the last [inaudible] three is associated
with users and other, I'm noticing that there's no read or execute permissions
for this application. Okay. How do we correct that? So we can use a change
modify command, ch mod, to update the permissions. Okay. So now it's fixed for
me, we tried the application, everything works. Any follow up that we need to
do? Yes. I would want to notify the owners of the application because it's going
to affect a lot of users and this will also help prevent reoccurring issues from
happening. Okay. Good. Thank you. In this scenario, we saw a lot of back and
forth which is very common for troubleshooting interviews. The initial
description was very broad and the candidate used several follow-up questions to
better scope the problem. Since the error message wasn't clear, there were
several possible causes of the problem. Eliminating the most likely culprits
first allowed us to keep trying until we found the actual cause. We also showed
that it's okay if you don't know everything. The candidate didn't know where the
log for apt is stored but she explained how she would find that out if this were
a real-life issue she we're trying to address. When you do that, it shows that
you're resourceful and a good problem solver. It's impossible to know everything
but knowing where to find answers is a critical skill for an IT support
specialist. That's it for now. See you again at the end of our next course.