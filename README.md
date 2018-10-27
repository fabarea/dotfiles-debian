# dotfiles

Fabien Udriot' dotfiles for fish, git, and more.

Tested on macOS and Linux

## Installation

    $ git clone git@github.com:fabarea/dotfiles.git ~/.dotfiles
    $ cd ~/.dotfiles
    $ ./install.sh (todo test me!)

It will install [rcm] and use that to safely symlink the dotfiles, prompting you
if a file already exists (like if you already have `~/.zshrc`).

[rcm]: http://thoughtbot.github.io/rcm/rcm.7.html

We can also install it an more manual way after cloning:

```
cp .dotfiles/rcrc .rcrc

# Check what dot files will be "connected" (AKA linked)
lsrc

# Do the job
rcup
```

## Organization

`rcm` will symlink all files into place, keeping the folder structure relative
to the tag root. However, non-configuration files and folders like `system/`,
`Brewfile`, `README.md`, etc will not be linked because they are in the
`EXCLUDES` section of the [`rcrc`](/rcrc) file.

## A few commands

A few command that I run to create the dotfiles in this repository

```
# Will create a `tag-git` directory in the dotfiles repository
mkrc -t git .gitconfig
```

## TODO

Integrate more fish configuration from https://github.com/Netherdrake/dotfiles

## Attribution

Source of Inspiration [GABRIEL BERKE-WILLIAMS]

[GABRIEL BERKE-WILLIAMS]: https://github.com/gabebw/dotfiles
