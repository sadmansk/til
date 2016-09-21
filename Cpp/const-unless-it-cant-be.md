`const` unless it can't be
==========================

Everything should always be const unless it can't be. This includes both function
parameters as well as functions themselves. This improves readability and self-
documentation of the code. It will also save a lot of headaches and frustrations
when debugging the program(s).

> I am a full const nazi nowadays, and I chide any programmer that doesn’t const
> every variable and parameter that can be. - [John Carmack, 2013](http://kotaku.com/454293019)

On that note, always pass objects as const reference when possible. All of these
would help greatly towards inference of what a function does.