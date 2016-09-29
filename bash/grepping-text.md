`grep`ping text
===============

> Although I have learned about `grep`'s usage a while ago, I have started extensibly using it during
> my time at my current company and my appreciation for the tool has gone up by a lot.

`grep` can be used to narrow down massive bodies of texts in order to look at only part(s) of interest.
For example, if I'm looking for a specific process that I want to `SIGTERM` or `SIGKILL` and I want to
know it's `pid` (process ID), I have to use `ps aux` to list all the processes running on the system.
But by *piping the output* to `grep`, I can specify to only show me the lines that has the text `java`
in them:
```
ps aux | grep java
```
Now one of the things I absolutely love about bash is output piping. `grep` can also be used to look for
text in a specified directory tree. So, combining those two, we can `grep` the `grep` output:
```
grep -r SEARCH_STRING | grep EXT
```
As an example, this will allow to find the `SEARCH_STRING` in files containing `EXT`, which could be the
extension, or just a part of the file name.

