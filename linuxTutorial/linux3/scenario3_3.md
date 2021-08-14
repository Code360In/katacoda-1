Most of the examples we’ve looked at so far use relative paths. That is, the place you end up at depends on your current working directory. Consider trying to `cd` into the “etc” folder. If you’re already in the root directory that will work fine:
> ```
> cd /
> pwd
> cd etc
> pwd
> ```{{execute}}

But what if you’re in your home directory?
> ```
> cd
> pwd
> cd etc
> pwd
> ```{{execute}}
