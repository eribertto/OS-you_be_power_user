In Linux processes have a parent child relationship. This means that every
process that you launch comes from another process. Lets check out this command.
The less command would be the parent process to our grep process. If all
processes come from another process, there must be an initial process that
started this all, right? Yes, there is, when you start up your computer, the
kernel creates a process called a nit, which has a pit of one. A nit starts up
other processes that we need to get our computer up and running. There are more
nuances to process creation than this, but I wanted to introduce the parent
process concept, since you'll see them when we start managing processes. What
about what happens when we're done with our processes? When your processes
complete their task, they'll generally terminate automatically. Once a process
terminates, it'll release all the resources it was using back to the kernel, so
that they can be used for another process. You can also manually terminate a
process, which we'll discuss how to do in an upcoming lesson.