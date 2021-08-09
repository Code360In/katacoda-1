When the output of `git log` is too long to fit in your screen, `git` uses a program to split it into pages of the size of your screen. When this “pager” is called, you will notice that the last line in your screen is a :, instead of your usual prompt.

To get out of the pager, press <kbd> Q </kbd>.
To move to the next page, press <kbd> Spacebar </kbd>.
To search for `some_word` in all pages, press <kbd> / </kbd> and type `some_word`. Navigate through matches pressing <kbd> N </kbd>.

<br/>

# Limit Log Size
To avoid having `git log` cover your entire terminal screen, you can limit the number of commits that Git lists by using `-N`, where `N` is the number of commits that you want to view. For example, if you only want information from the last commit you can use:

> ## Bash
> `git log -1`{{execute}}

> ## Output
> ```
> commit 005937fbe2a98fb83f0ade869025dc2636b4dad5
> 
> Author: Vlad Dracula <vlad@tran.sylvan.ia>
> 
> Date:   Thu Aug 22 10:14:07 2013 -0400
>
>
>    Discuss concerns about Mars' climate for Mummy
> ```

<br/>

You can also reduce the quantity of information using the `--oneline` option:

> ## Bash
> `git log --oneline`{{execute}}

> ## Output
> ```
> 005937f Discuss concerns about Mars' climate for Mummy
> 
> 34961b1 Add concerns about effects of Mars' moons on Wolfman
> 
> f22b25e Start notes on Mars as a base
> ```

<br/>

You can also combine the `--oneline` option with others. One useful combination adds `--graph` to display the commit history as a text-based graph and to indicate which commits are associated with the current `HEAD`, the current branch `main`, or [other Git references](https://git-scm.com/book/en/v2/Git-Internals-Git-References):

> ## Bash
> `git log --oneline --graph`{{execute}}

> ## Output
> ```
> * 005937f (HEAD -> main) Discuss concerns about Mars' climate for Mummy
> 
> * 34961b1 Add concerns about effects of Mars' moons on Wolfman
> 
> * f22b25e Start notes on Mars as a base
> ```

<br/>
