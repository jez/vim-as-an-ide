# Vim as an IDE

This repository is the result of a tech talk that I gave at Carnegie Mellon
University on February 25, 2015. Its central motivation is this: students who
have been instructed or told to use Vim to complete programming assignments
while ssh'ed are missing out on the vast power that lies within Vim.

There are two fronts to having an amazing Vim experience:

1. knowing how to manipulate text using Vim's built in keyboard shortcuts
2. having plugins that make Vim behave like users would expect from a modern
   text editor.

In my experience as a TA and fellow student, learning the former requires
the latter and vice versa, leading to a vicious cycle of Vim peril. With this in
mind, this repository aims to cure the latter, so that the vicious cycle can
end.

## How to use this repository

This repository contains a sample vimrc that walks you through the changes at
each step so that you can gain an understanding of what's going on (rather than
just copying someone's vimrc!).

Each commit in this repository corresponds to __a step from the actual
workshop__. Use the __[list of all commits][master]__ to browse the steps.
You'll see a (sometimes lengthy) explanation of what happened, and then the
diff(erence) of exactly what changed from step-to-step.

[master]: https://github.com/jez/vim-as-an-ide/commits/master

This is what you should do:

- start at the [first commit](https://github.com/jez/vim-as-an-ide/commit/0673f0c)
- read the commit message and GitHub comments
- copy the changes
- repeat

It's that simple. Depending on how fast you read and how in-depth you want to
go, you could easily have a fully-configured\* Vim setup in about an hour.

Once you've done this, the hard part is learning to use what you just installed!
I went back through and added some usage information and links to references on
the GitHub comments, so be sure to check them out.

### Table of Contents

*  [Create vimrc file](https://github.com/jez/vim-as-an-ide/commit/0673f0c)
*  [Add some general settings](https://github.com/jez/vim-as-an-ide/commit/dff7da3)
*  [Enable the mouse](https://github.com/jez/vim-as-an-ide/commit/fc77b04)
*  [Set up Vundle boilerplate](https://github.com/jez/vim-as-an-ide/commit/1186be2)
*  [Make Vim look good](https://github.com/jez/vim-as-an-ide/commit/457f2e2)
*  [Plugins NERDTree and NERDTree Tabs](https://github.com/jez/vim-as-an-ide/commit/b7ff90c)
*  [Plugin Syntastic](https://github.com/jez/vim-as-an-ide/commit/144f979)
*  [Plugins vim-easytags and tagbar](https://github.com/jez/vim-as-an-ide/commit/fd2c49c)
*  [Plugin ctrlp](https://github.com/jez/vim-as-an-ide/commit/80db74f)
*  [Plugin A.vim](https://github.com/jez/vim-as-an-ide/commit/8d4223f)
*  [Plugins vim-gitgutter and vim-fugitive](https://github.com/jez/vim-as-an-ide/commit/1e5757e)
*  [Plugin delimitMate](https://github.com/jez/vim-as-an-ide/commit/2fe0507)
*  [Plugin vim-superman](https://github.com/jez/vim-as-an-ide/commit/b185e9f)
*  [Plugin vim-tmux-navigator](https://github.com/jez/vim-as-an-ide/commit/44f5225)
*  [Syntax plugins](https://github.com/jez/vim-as-an-ide/commit/5ba534e)
*  [Add all the extra plugins that I use](https://github.com/jez/vim-as-an-ide/commit/9089a95)

As you're following along these steps, if you want to check whether what you see
matches up with what my setup looks like after a given step, jump over to [this
post](http://blog.jez.io/2015/03/03/vim-as-an-ide/).


## Installation Instructions

If you just want to use this file as your vimrc, no questions asked,

1. Move your ~/.vimrc file and ~/.vim folder somewhere else for now.
2. [Download Vundle](https://github.com/jez/vim-as-an-ide/commit/1186be2)
3. [Change your terminal colorscheme to solarized](https://github.com/jez/vim-as-an-ide/commit/457f2e2)
4. [Install a patched font](https://github.com/jez/vim-as-an-ide/commit/457f2e2)
5. Download the file [vimrc.vim](/vimrc.vim) and rename it to ~/.vimrc
6. Run `vim +PluginInstall +qall`
7. ???
8. Profit!

But you should really look through the steps for more information about what went down. Remember: every time you add a new `Plugin ...` line, you'll have to run

```
vim +PluginInstall +qall
```

## Now that I'm a plugin master, I want to...

- find more plugins!
    - <http://vimawesome.com/>
- learn how to actually use Vim!
    - `vimtutor`
    - [Learning Vim in 2014][1]
        - In particular, [Vim as Language][2]
- customize my Vimrc!
    - Look at these examples
        - <https://github.com/jez/dotfiles/blob/master/vimrc>
        - <https://github.com/bezi/dotfiles/blob/master/vimrc>
    - See the [first][1] and [last][3] links
- write my own Vim plugin!
     - [Learn Vimscript the Hard Way][3]

[1]: http://benmccormick.org/learning-vim-in-2014/
[2]: http://benmccormick.org/2014/07/02/learning-vim-in-2014-vim-as-language/
[3]: http://learnvimscriptthehardway.stevelosh.com/

__In order to teach people plugins, I had to sacrifice teaching people how to
tap into the power of editing in Vim, which comes from using the keyboard over
the mouse.__ Please, take a little time to learn how to actually use Vim!

\* When I say _fully-configured_, I mean _actually usable_. It can be argued that
Vim is never fully-configured: everyone's preferences are different, and
circumstances change. Configuring your text editor is really a continuous
process!
