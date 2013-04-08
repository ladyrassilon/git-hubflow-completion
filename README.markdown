git-hubflow-completion
===================

Bash, Zsh and fish completion support for [git-hubflow](http://datasift.github.io/gitflow/).

The contained completion routines provide support for completing:

 * git hf init and version
 * feature, hotfix and release branches
 * remote feature, hotfix and release branch names

This is a fork of bobthecow's git-flow completions

Installation for Bash
---------------------

To achieve git-hubflow completion nirvana:

 0. [Install git-completion](http://github.com/bobthecow/git-flow-completion/wiki/Install-Bash-git-completion).

 1. Install `git-hubflow-completion.bash`. Either:

    1. Place it in your `bash_completion.d` folder, usually something like `/etc/bash_completion.d`,
       `/usr/local/etc/bash_completion.d` or `~/bash_completion.d`.

    2. Or, copy it somewhere (e.g. `~/.git-hubflow-completion.sh`) and put the following line in the `.profile` or
       `.bashrc` file in your home directory:

            source ~/.git-hubflow-completion.sh

 2. If you are using Git < 1.7.1, you will need to edit git completion (usually `/etc/bash_completion.d/git` or
    `git-completion.sh`) and add the following line to the `$command` case in `_git`:

        _git ()
        {
                [...]
                case "$command" in
                   [...]
                   flow)        _git_hf ;;		
                   *)           COMPREPLY=() ;;
                esac
        }


Installation for Zsh
--------------------

To achieve git-hubflow completion nirvana:

 0. Update your zsh's git-completion module to the newest verion --
    [available here](http://zsh.git.sourceforge.net/git/gitweb.cgi?p=zsh/zsh;a=blob_plain;f=Completion/Unix/Command/_git;hb=HEAD).

 1. Install `git-hubflow-completion.zsh`. Either:

    1. Place it in your `.zshrc`.

    2. Or, copy it somewhere (e.g. `~/.git-hubflow-completion.zsh`) and put the following line in
       your `.zshrc`:

            source ~/.git-hubflow-completion.zsh

    3. Or, use this file as an oh-my-zsh plugin. #This is entirely untested


Installation for fish #Todo - Needs testing and updating
--------------------------------------------------------

To achieve git-hubflow completion nirvana:

 1. Install `git.fish` in your `~/.config/fish/completions` folder.


The Fine Print
--------------
Forked by [Gemma Hentsch](https://github.com/ladyrassilon)

Copyright (c) 2011 [Justin Hileman](http://justinhileman.com)

Distributed under the [MIT License](http://creativecommons.org/licenses/MIT/)
